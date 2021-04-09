### [Back to Portfolio](index.md)

### [Back to Table of Contents](seniorproject.md)

### [View Full Report Here](fullReport.md)

Test Results
====================
For the test results of the File Encryptor project they were as expected with response on the user interface and the functionality of the project itself. In regards to the project's functionality the project worked in every aspect with the exception of the AES256 Decryption method. This was due to while running the program under one instance so the IV and the secret key would remain the same, when attempting to decrypt it would encounter three errors: base64 decoding error, and 2 invalid character errors. Resolving the base64 decoder error would cause one of the invalid character errors to pop up and resolving that error made the other one pop up. However, instead of resloving the issue after resolving the second illegal character error it would bounce back to a base64 decoder error at which point attempting to resolve that error would lead to a repeat of the order of the errors with no end to them.
