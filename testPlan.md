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

How each element is to be tested
--------------------------------
- Element 1
  - Each run through the encryption and decryption process a proper file name is needed so it will be tested correctly through each use but alternatively an improper file path name will be used to ensure that for improper files that it makes the user try again. In this case, the term improper file path name means that the file does not exist on the specified file path name.
- Element 2
  - Each run is dictated by a series of switch statements where the user will select a number 1 through 3 to perform various tasks such as selecting a method, starting encryption, starting decryption, or simply exiting the program. The input will be validated by operating through the series of switch statements using the appropriate numbers but also by using numbers outside of the 1-3 bounds to test to make the program require another input from the user.
- Element 3
  - Every Caesarean shift requires a shift key and for the cipher in this program, the shift key is determined by the user so that they may be able to decrypt the text that they are encrypting. Testing of the functionality of the shift key will be done by having the user encrypt the contents of the original file then having them decrypt it. Using all three files the original, the encrypted file, and the newly created decrypted file three will be examined to determine if the shift key worked then the contents of all three files will match and the decryption will match to the original file.
- Element 4
  - This will be tested by taking the number that was selected by the user during decryption and run it against the original file to produce the proper or expected output of the shift to the cipher then it will be cross-examined against the encrypted text file.
- Element 5
  - To test this using the same shift key the encrypted file will be reversed using the shift key to produce a decrypted file that should match the original test file text.
- Element 6
  - This element will be tested automatically with the rest of the user's interaction with the program through the encryption and decryption processes. The way that this will be ensured to work is that the produced encrypted text file will have text in it because the buffered reader method will pull the text file and send it to be encrypted.
- Element 7
  - This will be tested by the user interacting with the program to complete the DES encryption by entering the file pathname so that DES can pull the file text and encrypt it and send it back to main to be output to a new file. The contents of that new file will be how this element is tested since the contents of that file are supposed to be encrypted with DES encryption formatting.
- Element 8
  - To ensure the functionality of this element the user will enter the file pathname of the DES-encrypted file and that file text contents will be passed to the decryption method so that it can be reverted to the original text and stored in a new decryption text file.
- Element 9
  - This element will be tested by the user's interaction with the program by having them use input so that they can generate the secret key for the encryption using AES256 format.
- Element 10
  - Through the verification of the original passphrases the identity of the individual decrypting will be identified and then the decryption proceeds and the success of the element will be when the text that is decrypted will match the original file text.
