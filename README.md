### Gym Management System 1.0 suffers from an Unrestricted File Upload vulnerability allowing attackers to gain Remote Code Execution by uploading a malicious PHP file.

The /up.php page allows unauthenticated users to upload an image along with "name" and "ext" parameters and attempts to modify the image before saving it as \<name\>.\<ext\> in the root directory.

If the content type indicates that the file is not an image however, it is simply saved as <name>.<ext> immediately. This allows us to execute code by uploading and visiting a malicious PHP file.
