### [Back to Portfolio](index.md)

### [Back to Table of Contents](seniorproject.md)

### [View Full Report Here](fullReport.md)

Test Results
====================
For the test results of the File Encryptor project they were as expected with response on the user interface and the functionality of the project itself. In regards to the project's functionality the project worked in every aspect with the exception of the AES256 Decryption method. This was due to while running the program under one instance so the IV and the secret key would remain the same, when attempting to decrypt it would encounter three errors: base64 decoding error, and 2 invalid character errors. Resolving the base64 decoder error would cause one of the invalid character errors to pop up and resolving that error made the other one pop up. However, instead of resloving the issue after resolving the second illegal character error it would bounce back to a base64 decoder error at which point attempting to resolve that error would lead to a repeat of the order of the errors with no end to them.

Due to this issue within the program the program can operate fully as intended on the initial design. Additionally, it is different from the original design because I could not get the keys for DES and AES256 to be saveable to match against for decryption later on to encrypt multiple files at once. This was due to instancing and once a new instance is created there is currently no way to verify even if the key is saved accurately to decrypt the files later on. So, to solve this issue the step that was taken was to do encryption and decryption within once instance which means the program functions by encrypting then decrypting right after since the instance is the same and it can be verified for decryption. These two key issues aside the rest of the program functions as intended each supporting method for the main and individual classes fulfills its purpose and the Caesarean encryption method works with encrypting multiple files without having to decrypt right after encrypting like the original design of the project.

For the testing of the project I selected 5 individuals to test the functionality and user interface of the project. These were the two main foci of the project this is because the level at which I designed the product for is the average consumer who knows nothing about encryption or programming. However, this project can also cater to those who are versed in either encryption and or programming. Since this project was designed with the average user in mind the 5 individuals for the testing had little to no experience in programming or encryption. This was to achieve results that could reflect the interactions of the average user to better interpret the current design's effectivness on accomplishing the main goal of being usable by the average user.

For each individual they did a Caesarean and a DES encryption and decryption since both methods were fully functional unlike AES256 decryption. The file used for all of these tests was test.txt that contains the following:

![test file text here](images/testText.PNG)

Example ouput from Caesar encryption and decryption:

![cae1 pair](images/cae1dec.PNG)

Example output from DES encryption and decryption:

![des1 pair](images/des1pair.PNG)
