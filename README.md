### Gym Management System 1.0 - Unrestricted File Upload

#### Vendor Homepage: https://projectworlds.in/
#### Software Link: https://projectworlds.in/free-projects/php-projects/gym-management-system-project-in-php/

#### Exploit:
The /up.php page allows unauthenticated users to upload a file along with "name" and "ext" parameters, processes it further if the content type indicates it's an image, then saves it as "<name>.<ext>".
As we fully control the uploaded filepath we can now upload a file anywhere on the machine, so we can now upload our malicious PHP file to the current directory and access it from the page's root.

The /up.php page allows unauthenticated users to upload an image along with "name" and "ext" parameters and attempts to modify the image before saving it as \<name\>.\<ext\> in the project's root directory.

If the content type indicates that the file is not an image though, it is not modified but is still saved as <name>.<ext>. This lets us upload any file we want to the server.

As this is a PHP application, this can be used to upload a malicious PHP file that can then be executed by simply requesting it from the webserver. 
