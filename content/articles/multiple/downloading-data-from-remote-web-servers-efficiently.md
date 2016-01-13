---
node_id: 101
title: Downloading Data From Remote Web Servers Efficiently
type: article
created_date: '2011-03-09 18:56:15'
created_by: RackKCAdmin
last_modified_date: '2011-08-17 14:5654'
last_modified_by: matt.wheeler
products: 'Cloud Servers,Cloud Sites'
body_format: tinymce
---

undefined&copy;2009 Adrian Otto
    //
    // This program is free software: you can redistribute it and/or modify
    // it under the terms of the GNU LESSER GENERAL PUBLIC LICENSE as published by
    // the Free Software Foundation, either version 3 of the License, or
    // (at your option) any later version.
    //
    // This program is distributed in the hope that it will be useful,
    // but WITHOUT ANY WARRANTY; without even the implied warranty of
    // MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    // GNU General Public License for more details.
    //
    // You should have received a copy of the GNU General Public License
    // along with this program.  If not, see <http://www.gnu.org/licenses/>.

    // Example Usage:
    $data = return_remote_data("http://www.yahoo.com/", "yahoo.html", 600);

    // How it works:
    // 
    // The example above downloads http://www.yahoo.com, saves it into 
    // a file named yahoo.html (you can use a full path here, if desired), and 
    // refreshes the content every 600 sec (10 min) as needed.

    // Function to return remote data from cache, or serial fetch a fresh one
    function return_remote_data($url,$file,$max_age) {
        $timeout = 5;
        $lock_filename = $file . ".lock";

        // First, check to see if we have fresh cached data to return
        $stat = @stat($file);
        if($stat) {
            $age = time() - $stat['mtime'];
            if($age < $max_age) { // The cached file is fresh!
                return get_file_contents_as_string($file);
            }
        }

        // Fetch data, because we don't have fresh data cached
        $lock_fh = fopen($lock_filename, "w"); // Create/Open a lock file
        if($lock_fh) { 
            if(flock($lock_fh, LOCK_EX | LOCK_NB)) {       // Locked okay, perform the remote fetch
                ini_set('default_socket_timeout', $timeout);
                $temp_filename = $file . ".temp." . $better_token = md5(uniqid(rand(), true) . @$_SERVER['REMOTE_ADDR']);
                $ch = curl_init($url);
                $temp_fh = fopen($temp_filename, "w");    // Open the temp file where we will store the output
                stream_set_timeout($temp_fh, $timeout);   // Set a sensible timout value
                curl_setopt($ch, CURLOPT_FILE, $temp_fh); // Indicate that we will download to the temp file
                curl_setopt($ch, CURLOPT_HEADER, 0);      // Don't save the response headers in the temp file
                curl_setopt($ch, CURLOPT_TIMEOUT, 30);
                curl_setopt($ch, CURLOPT_CONNECTTIMEOUT, $timeout);
                curl_exec($ch);
                curl_close($ch);
                fclose($temp_fh);
                
                $stat = @stat($temp_filename); 
                if($stat['size'] > 0) { // Output was downloaded
                    rename($temp_filename, $file); // Rename the file to the intended name (atomic)
                    flock($lock_fh, LOCK_UN); // Release the lock
                    return get_file_contents_as_string($file); // MISS, but refreshed successfully
                }
                else {
                    @unlink($temp_filename);
                    if(file_exists($file)) { // Refresh attempt failed, returning stale version
                        touch($file); // Mark it as fresh so that not every hit retries (retry once per expire interval)
                        return get_file_contents_as_string($file);
                    }
                    else { // There is nothing to return!
                        return;
                    }
                }
            }
        }
        // The file is already locked, lockfile create failed, so serve the existing file
        if(file_exists($file)) { // Returning stale version
            return get_file_contents_as_string($file);
        }
    }

    // Function to return the contents of a file as a string
    function get_file_contents_as_string($file) {
        $data = "";
        $f = fopen($file, "r");
        if($f) {
            while(!feof($f)) {
                $data .= fgets($f);
            }
            fclose($f);
            return $data;
        }
        else {
            error_log("Unable to open file: $file " . var_dump(debug_backtrace()));
        }
    }

    ?>

 

