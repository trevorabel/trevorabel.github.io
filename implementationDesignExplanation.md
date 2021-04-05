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

![Fig. 1](images/fileNotFound01.PNG)
Fig. 1 FileNotFound class that throws the Invalid File Location error when an improper path is entered while searching for a file.

![Fig. 2](images/cae01.PNG)
![Fig. 3](images/cae02.PNG)
![Fig. 4](images/cae03.PNG)
![Fig. 5](images/cae04.PNG)
![Fig. 6](images/des01.PNG)
![Fig. 7](images/des02.PNG)
![Fig. 8](images/des03.PNG)
![Fig. 9](images/des04.PNG)
![Fig. 10](images/des05.PNG)
![Fig. 11](images/des06.PNG)
![Fig. 12](images/des07.PNG)
![Fig. 13](images/aes01.PNG)
![Fig. 14](images/aes02.PNG)
![Fig. 15](images/aes03.PNG)
![Fig. 16](images/aes04.PNG)
![Fig. 17](images/main01.PNG)
![Fig. 18](images/main02.PNG)
![Fig. 19](images/main03.PNG)
![Fig. 20](images/main04.PNG)
![Fig. 21](images/main05.PNG)
![Fig. 22](images/main06.PNG)
![Fig. 23](images/main07.PNG)
![Fig. 24](images/main08.PNG)
![Fig. 25](images/main09.PNG)
![Fig. 26](images/main10.PNG)
![Fig. 27](images/main11.PNG)
![Fig. 28](images/main12.PNG)
![Fig. 29](images/main13.PNG)
![Fig. 30](images/main14.PNG)
![Fig. 31](images/main15.PNG)
![Fig. 32](images/main16.PNG)
![Fig. 33](images/main17.PNG)
![Fig. 34](images/main18.PNG)
![Fig. 35](images/main19.PNG)
![Fig. 36](images/main20.PNG)
![Fig. 37](images/main21.PNG)
![Fig. 38](images/main22.PNG)
![Fig. 39](images/main23.PNG)
![Fig. 40](images/main24.PNG)
![Fig. 41](images/main25.PNG)
![Fig. 42](images/main26.PNG)
![Fig. 43](images/main27.PNG)
![Fig. 44](images/main28.PNG)

