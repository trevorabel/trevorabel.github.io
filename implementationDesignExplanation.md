### [Back to Portfolio](index.md)

### [Back to Table of Contents](seniorproject.md)

### [View Full Report Here](fullReport.md)

Implementation Description & Explanaiton
====================
Introduction
------------
This project, the text file encryptor project, is a culmination of all the information that has been presented in the Computer Science classes offered at Charleston Southern for the Bachelor's degree in Cyber Security. The project is in fulfillment of the requirements of graduation and is the focus of the senior project sequence where the Text File Encryptor was developed. This project was designed, coded, tested, and completed within the sequence of the senior project classes starting at CSCI 497, Senior Project Design, and going through CSCI 499 Senior Project Defense. 

Goals & Objectives
------------------
For the implementation of the file encryptor project, there are a few main goals. First, produce a fully working text file encryptor. Second, make this text file encryptor segmented in its respective areas so that the encryptor itself can be customized. Thirdly, have a working product that can be released for free to address the lack of free encryption choices for individual files and the lack of ability to choose the desired encryption method.
The objectives of this project include the following: develop a stronger understanding of Java-based security classes and structures, learn how to properly separate core functions of encryption from the rest of the program to create a program that is easier to modify, and produce a product that is a sufficient fulfillment of the senior project sequence for the requirements of graduating with a Bachelor's degree in Cyber Security from Charleston Southern University.

Tasks
-----
For this project, it is broken down into simple stages for the components that are necessary for this project to be fully functional.

1. Caesar Encryption
2. Caesar Decryption
3. DES Encryption
4. DES Decryption
5. AES256 Encryption
6. AES256 Decryption
7. Functionality for recursion to repeat encryption/decryption
8. Functionality for File input validation
9. Functionality for saving a file directly to the desktop/specific folder
10. Functionality for creating a new folder automatically for each new encryption and decryption
11. UI for navigating through the program
12. BufferReader for reading the original file and converting it to a string
13. Creating FileNotFoundException for invalid file location call

Implementation Schedule
-----------------------

- Feb. 28, 2020
  - Implemented System Baseline
    - Caesarean Encryption/Decryption
    - File Path Searching
    - Oupting encrypted or decrypted files to new files created files
    - Input validation for file path searching
    - BufferReader method to pass file contents into a string
    - FileNotFounException

- May 20, 2020
  - Completed encryption or decryption choice at the beginning of the program
  - Implement recursion within the program to encrypt/decrypt multiple files in one program run
  - Completed the rerouting of the program-created encrypted and decrypted files back to the desktop instead of the java project folder

- Nov. 20, 2020
  - Implemented DES encryption/decryption and tested for accuracy

- Jan. 11, 2021
  - Implemented AES256 and tested for accuracy

- Jan 12, 2021
  - Begin testing and collecting usability and bug case information for project defense

Code Screenshots
----------------
[Code Here](https://github.com/trevorabel/seniorproject)

![Fig. 1](images/fileNotFound01.PNG)

Fig. 1 FileNotFound class that throws the Invalid File Location error when an improper path is entered while searching for a file.

![Fig. 2](images/cae01.PNG)

Fig. 2 Caesarean Encryption global variables, constructor, passing file contents, and description methods.

This image shows the constructor for the Caesarean Encryption class, the method that passes only the text into the class, and the beginning of the description of the cipher.

![Fig. 3](images/cae02.PNG)

Fig. 3 The description of the Caesarean encryption method and the beginning of the actual encryption.


![Fig. 4](images/cae03.PNG)

Fig. 4 The rest of the Caesarean encryption method and the beginning of the decryption method.

For the encryption, it shows how when the file contents and the selected shift key are passed through that the for loop works one character at a time when switching to the shifted ciphertext. In the if loop within the for loop it shows that the way that the characters are determined is by their ASCII values so values 97 through 122 represent the lower case characters while 65 through 90 represent the upper case characters. For both upper and lower case, the process is similar so it takes character variable ch and pulls one character from the file text string variable that has the whole contents of the file. Next, the selected character is run through another if loop that checks to see what the current value is so that it can accurately loop back to the start of the alphabet for the respective case of that character. After that, the character is passed to the string variable called altered, this variable stores each character that has been changed until the original string has been completed changed by the shift key. Then the string is passed to be stored into a new file to mark the end of the encryption.

![Fig. 5](images/cae04.PNG)

Fig. 5 Decryption of Caesarean encrypted text and other methods to get and set information for the encryption.

For the decryption of the Caesarean encryption method, it is the same as described for Fig. 3 and Fig. 4 but instead of encrypting the contents, it decrypts it. So everything is the same until it gets to modify the character itself at which point it works backward or the opposite way that the encryption shifting works. Similarly, the character variable ch for the currently shifted or to be shifted variable is stored after being shifted into the string variable called decay. Then that string variable is returned to be stored into a new file to complete the decryption.
The methods getShiftKey and setShiftKey both deal with the value of the shift key for the instance of the Caesarean encryption class. The getShiftKey is useful if you forget the shift key and have not moved to another instance. While the setShiftKey is useful for adjusting the shift key if necessary for whatever reason.

![Fig. 6](images/des01.PNG)

Fig.6 Shown in this image are all the libraries necessary for the function of the DES encryption class.

![Fig. 7](images/des02.PNG)

Fig. 7 Displays all the global variables for the DES encryption class.

Fig. 6 and Fig. 7 show all the libraries and all of the global variables for the functionality of the DES encryption class. Some of these variables like selected and padding are not necessary they just save space when typing out their respective parts during the coding of the actual encryption. These variables are just prematurely declaring the type of encryption and the type of padding to use for the DES encryption and decryption.

![Fig. 8](images/des03.PNG)

Fig. 8 DES Encryption description and the encryption method for DES.

In the encryption of DES, it shows that the variables passed in are types input stream and output stream. Additionally, there is an exception that is thrown which is the IOExecption otherwise not throwing it will not allow the method to work. First, the KeyGenerator library is used to prepare to generate the secret key. The global variable sKey is used to store the key generated by the KeyGenerator library instance. With the encrypt cipher variable it is setting up for the type of padding being used for the DES encryption. Then the encrypt cipher variable is used to generate the DES encryption to be used to encrypt the file text.
Then an output stream is created so that the encryption can be written out to a new file. Then the methods write data is called using the is, input stream variable, which holds the contents of the file and os, the path of the new file.

![Fig. 9](images/des04.PNG)

Fig. 9 DES decryption and the write data method for sending the encrypted text out.

Similar to Fig. 8 the decryption uses the same structure to generate with padding and then the variable decryptCipher to create the decryption to be used against them is a variable that holds the file text. The write data method is responsible for pushing the encrypted or decrypted text out to the new file to mark the end of the encryption or decryption. 

![Fig. 10](images/des05.PNG)

Fig. 10 The desFileCreator method is used in the main class to create the new file for that encryption.

First, it catches everything into a while loop where the condition is !real which means not real, the real variable is a boolean variable that by default is set to false so once it is set to true it exits. The purpose of this is the real variable is the only variable controlling the loop until a file name is available. Then it steps into the if loop where the major condition is if the directory file exists if so then it enters a for loop where it goes up to 100 times per encryption or decryption, so up to a total of 200 times for the pairs of encryption and decryption.
Then the file path is broken down into parts so that an iterator can add one and keep the same name with a different number to be able to create new linkable files. Once a new file name is found it spits back information that lets the user know that the new path has been put into a string to be used for creating the file. Then says sets real to true which means that it has found a real file name. Then using the new file path string a file name is attached which is DESEncrypted.txt, all DES-encrypted files have this name but are separated by their folder number in the order they were made.

![Fig. 11](images/des06.PNG)

Fig. 11 Contains the final steps of desFileCreator in which the new path is passed so the file is created at that path and shows the start of the decryption version of the same file creator.


![Fig. 12](images/des07.PNG)

Fig. 12 Shows the end of the desFileCreatorDec which is the same as the encryption version just specialized specifically for decryption.

The above desFileCreatorDec is the same as the desFileCreator the only difference is instead of naming the files and folders DESEncrypted/DESEncryption# it is DESDecrypted/DESDecrypted#. Then using the new file path string a file name is attached which is DESDecrypted.txt, all DES decrypted files have this name but are separated by their folder number in the order they were made.

![Fig. 13](images/aes01.PNG)

Fig. 13 AES256 Encryption libraries that are necessary for functionality.


![Fig. 14](images/aes02.PNG)

Fig. 14 AES encryption method returns as a string to the main class.

This screenshot shows how the text is encrypted in AES256 format. First, the Cipher class is used to generate the AES padding instance to prepare for encryption. Then the cipher instance AESCipher is used to generate the AES256 encryption using the declared mode, secret key, and the IV. Finally, the text is encrypted with a base64 encoder and passed all the previous requirements for the AES256 encryption to occur.

![Fig. 15](images/aes03.PNG)

Fig. 15 AES decryption method and genSecretKey method.

Here is how the secret key is generated for AES256 encryption. Using the SecretKeyFactory class to generate the padding instance so that the secret key can be generated. Then the KeySpec class is utilized to make the next step in the secret key by taking the user inputted word, salting, and declaring bounds, and the type of AES. Next, the SecretKey class is used to generate half of the secret key, and finally, the SecretKeySpec class is used to make the full key.

![Fig. 16](images/aes04.PNG)

Fig. 16 AES256 genIV method to make the IV for encryption and decryption.

For AES256 the IV must be 16-bytes long and this was done using the random number generator as opposed to making the user do it, for stronger security. First, instantiate a new 16-byte array and a new instance of the Random class. Using the Random class fill the IV array and return that array for use in encryption and decryption.

![Fig. 17](images/main01.PNG)

Fig. 17 Main class and all the libraries needed for functionality.


![Fig. 18](images/main02.PNG)

Fig. 18 The main class is driven by one line which references the methods in the main class.


![Fig. 19](images/main03.PNG)

Fig. 19 AES256 encryption testing, IV array testing, and keygen testing for AES256 encryption commented out.


![Fig. 20](images/main04.PNG)

Fig. 20 Testing for a functional iterator-based file creator for making new files and folders.


![Fig. 21](images/main05.PNG)

Fig. 21 Start function that has blank lines and banners for displaying necessary text.

The twelve blank lines allow for all the comments at the start of a program in Netbeans to be moved out of view so it is just the banners that contain basic project information such as the project name and my name.

![Fig. 22](images/main06.PNG)

Fig. 22 Selection method where the user selects which encryption they wish to do.

With the current state of the project, there are two issues, one is that both DES and AES256 functionality on its current implementation does not allow for multi-encryption without decryption like Caesar's implementation so it must encrypt and decrypt or it can not be decrypted. Secondly, AES256 decryption is currently bugged and stuck in a base64 error loop with no solution currently the AES256 can encrypt but not decrypt.

![Fig. 23](images/main07.PNG)

Fig. 23 The top shows how the program operates where after a choice it calls another section or just exits and quits.


![Fig. 24](images/main08.PNG)

Fig. 24 How the program looks for the file that the user wants to encrypt.

At the end of Fig. 23, it shows the beginning of the searching that the program does to find a file name that the user wants to encrypt. This is trapped in a while loop like the file creator so it will repeat until the proper conditions are met and in this case, it is that the entered file path leads to an actual file. If it is miss-typed or it is a file that does not exist it will prompt the user to try again until they get it right and the file name matches an existing file.

![Fig. 25](images/main09.PNG)

Fig. 25 Switch statement for the encryption methods for Caesarean, DES, and AES256.

In this switch statement case 1 or Caesarean takes up much less room because compared to DES and AES256 it is a much simpler encryption method so it does not need as much to function. After each encryption is complete the program will recursively call back to the selection method to allow the user to make another encryption, do decryption, or simply exit the program. Additionally, in the lower half of the screenshot, it shows the warning statement that DES has limited capabilities where it must decrypt after encrypting or it can not decrypt it at all.

![Fig. 26](images/main10.PNG)

Fig. 26 DES encryption and DES decryption.

The scanner at the beginning of the screenshot is simply to make the user acknowledge by pressing a key that they are using a limited encryption method. Then the desEncryption class is instantiated with a blank string so that the instance is made, then the instance is used with calls to the file path from earlier and the desFileCreator method for the generation of its output file. After it is done encrypting it will spit a message out saying that it is starting the decryption process at which point the user will have to enter the location of the newly encrypted text file.

![Fig. 27](images/main11.PNG)

Fig. 27 File location validation for DES decryption.

Just like for the initial file validation when they need to enter the encrypted file path there is also file path validation just to ensure that they get the right file and do not have to restart the program and begin the process over again. After the file path is validated it is passed into the same instance of DES so the key remains the same which is vital for decryption. Then it is decrypted and the desFileCreatorDec method is used to generate the new file and it calls back to the selection method.

![Fig. 28](images/main12.PNG)

Fig. 28 Similar to DES the AES encryption and decryption starts with the warning.

This warning is the same as the one for DES since encryption and decryption must be done at the same time. Then the AES class is instanced so it can be used for encryption and decryption. First, the genIV method is called so the IV will be ready for encryption then the user is prompted for both a phrase for their secret key and their salt.

![Fig. 29](images/main13.PNG)

Fig. 29 AES256 encryption occurs then the decryption begins.

After the user enters both phrases for encryption the encryption is done and the decryption begins. Just like with the DES decryption there is file path validation for the AES256 decryption file input.

![Fig. 30](images/main14.PNG)

Fig. 30 AES256 file decryption with a time delay to mimic phrase validation.

Here the file is read in and there are cuts made to the file text so that it is readable for the decoding such as removing newline characters, \n, then it is requested for the user to enter the two phrases they used earlier. All of that information is passed to the decryption method to be decrypted, if the phrases do not match however there will be no decryption. After the decryption is complete it calls back to the selection method.

*Note: Currently due to a base64 error loop the decryption for AES256 does not function 04/05/2021*

![Fig. 31](images/main15.PNG)

Fig. 31 Decrypt method for Caesarean decryption.

First, the user must pass the file validation check before proceeding to the decryption of Caesar encrypted files.

![Fig. 32](images/main1601.PNG)

Fig. 32 Here is the statement and the switch for selecting decryption methods.

While DES and AES256 are listed as decryption methods currently they do not have a functional stand-alone decryption method but are still listed since future enhancements will have this functionality. Once the user selects cesarean decryption the encrypted file contents are passed and the user is asked for their shift key to decrypt it.

![Fig. 33](images/main17.PNG)

Fig. 33 The attempt at DES decryption.

These are the remnants of the attempt at making a separated DES decryption but since these are two different instances the secret key is different so it was commented out until a solution can be found. Same for AES256 since it also deals with instanced keys that are needed to decrypt.

![Fig. 34](images/main18.PNG)

Fig. 34 Caesarean encryption method.

The method takes a string variable that contains the contents of the file and turns it into a caesar encrypted text with the user input for the shift key. Then it has its file creator similar to the DES one so it has its file creating system.

![Fig. 35](images/main19.PNG)

Fig. 35 Caesar encryption file creator and time stamp for file.


![Fig. 36](images/main20.PNG)

Fig. 36 Caesar decryption method.

![Fig. 37](images/main21.PNG)

Fig. 37 Caesar decryption file creator and time stamp for file.

Same as in Fig. 34 and Fig. 35 however, it decrypts then creates its file to store the decryption.

![Fig. 38](images/main22.PNG)

Fig. 38 Main class DES encryption and decryption methods.

This is the remainder of the first attempt at creating the DES encryption and decryption before realizing that both methods had used two different instances at which point the transition was made to encrypt and decrypt right after.

![Fig. 39](images/main23.PNG)

Fig. 39 AES encryption file creator.

![Fig. 40](images/main24.PNG)

Fig. 40 AES encryption file creator (cont).

Similar to the DES and Caesarean encryption file creators but for the AES256 encryption method.

![Fig. 41](images/main25.PNG)

Fig. 41 AES decryption file creator.

![Fig. 42](images/main26.PNG)

Fig. 42 AES decryption file creator (cont).

Similar to the DES and Caesarean decryption file creators but for the AES256 decryption method.

![Fig. 43](images/main27.PNG)

Fig. 43 Password verification method for AES256 decryption.

This is a boolean method that checks to make sure that the entered key phrase and the entered salt phrase match so that decryption occurs when these are both matching as a method of verification that it's the same person.

![Fig. 44](images/main28.PNG)

Fig. 44 Password verification (cont) and bufferedReader method.

The password verification method shows what the check is for if one or both of the phrases is wrong. Then the buffered reader method is what is used to take the contents from the file path query and retrieve the text from inside the file and put it into a string so that it can be encrypted.
