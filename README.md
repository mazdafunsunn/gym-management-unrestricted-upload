### Gym Management System 1.0 - Unrestricted File Upload

#### Vendor Homepage: https://projectworlds.in/
#### Software Link: https://projectworlds.in/free-projects/php-projects/gym-management-system-project-in-php/

#### Exploit:

The /up.php page allows unauthenticated users to upload an image along with "name" and "ext" parameters and attempts to modify the image before saving it as \<name\>.\<ext\> in the project's root directory.

If the content type indicates that the file is not an image though, it is not modified but is still saved as <name>.<ext>. This lets us upload any file we want to the server.

As this is a PHP application, this can be used to upload a malicious PHP file that can then be executed by simply requesting it from the webserver. 
