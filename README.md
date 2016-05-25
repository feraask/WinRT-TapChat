Tap Chat
=================
####Secure Messaging for Windows Phone 8.1

**Created by:**  
Feraas Khatib  
Gustavo Frankowiak  

**Features:**  

* AES ECB PKCS7 Encryption
* Near Field Communication (NFC) Functionality
* Full user system with friend management
* Easily add friends by tapping phones together and get a random generated 256 character encryption key for a secure chat session
* All data is stored fully encrypted in a remote database
* All user data (usernames, passwords, friend requests etc..) is sent fully encrypted and over SSL
* Each friend has a different encryption key that is used for that session
* Start a secure chat session using the internet and get a unique key **or** for more security just tap 2 NFC enabled phones together and get a random generated key that is never sent over the internet  

**Compatible with:** Visual Studio 2013 or newer and Windows Phone 8.1+ only.  

**Project Notes:**

* Anything with .xaml extension is just the UI and its associated code file can be found by adding .cs to the file name (i.e. LoginPage.xaml is the UI with backend code LoginPage.xaml.cs)
* AppServices.cs has the universally used variables and functions including ones for encrypting and decrypting data and sending/receiving data
* In order to run the code on the Windows Phone 8.1 emulator on a computer Visual Studio 2013 RC2 or newer along with the Windows phone 8 SDK running on Windows 8.1 Pro or newer is required.
* 3 external libraries/API's where used in development. The .dll files can be found in the Tap Chat/Libs folder. If the code does not compile initially it is most likely because the references to these libraries need to be updated. They libraries used are:
    1. Newtonsoft JSON: Library for serializing data objects to and from JSON for easy sending and receiving of data.
    2. App42Windows: Back end service provided by [shephertz](http://www.shephertz.com) for managing user accounts and friends. This essentially handle's the back end database for storing user accounts and friend management.
    3. AppWarpWinRT: This is another back end service provided by [shephertz](http://www.shephertz.com) that is used to send the messages between users.
