### [Back to Portfolio](index.md)

### [Back to Table of Contents](seniorproject.md)

### [View Full Report Here](fullReport.md)

Test Plan
====================

Project Development Test Plan
-----------------------------
The attached test plan covers the attempts made while testing the features of the File Encryptor project to get each part functional for testing.

Note: The AES256 Decryption method was stuck between 3 different errors dealing with Improper array length, Base64 decoder error, and invalid character errors. While debugging and resolving the invalid character errors a Base64 decoding error occurred. After debugging and resolving the Base64 error the Improper array length error occurred and in attempting to solve it ended back at the invalid character errors. Attempting to solve all three errors lead to a continuous loop of errors with no clear exit to a finished decryption method.

*See attached excel document for the Test Plan for the development of the senior project.*

### [Link to Test Plan](File%20Encryptor%20Test%20Plan%20-%20Trevor%20Abel.xlsx)

Project Testing Plan
--------------------
For the testing of the project, it is important to hit the major components of the project to ensure that they are functional as they are supposed to be for the primary functionality of the project. The means that the following key elements are going to be tested in the participant testing phase to ensure accuracy and input validation.

1. Input validation for file pathnames
2. Input validation for method selection
3. Input validation for Caesarean cipher shift (only allows numbers 1 - 26)
4. Caesarean encryption cipher shift
5. Caesarean decryption reverse shift
6. BufferedReader method to pull text from the file
7. DES instanced encryption to encrypt file text
8. DES instanced decryption to decrypt the encrypted file text
9. AES 256 encryption generated IV and Secret Key for creating encryption
10. AES 256 decryption passing the ciphertext, IV, and Secret Key for decryption

The above elements are vital to the operation of the project, therefore, are the foci of the user testing phase to receive feedback and see the operation of these elements while being operated by someone with no background on the project.

Input validation is one of the most important features of this project so that the project can not be derailed and broken since for this project security is the key this needs to be a primary concern as to not leave holes in the project to be exploited. The secondary concern is focused on the success of the actual encryption and decryption methods since outside of the validity of the inputs they are the core of the project so they need to be properly functional. These two categories make up the vast majority of what is critically important to the success of this project which is why they have been chosen as the features to be tested in the user trial phase.
