Ksecret
=======

Project to learn more specific technical cryptography skill.

The algorithm is **Blowfish.**

This is the step to follow :

	1. Implementation of blowfish.
	2. Test a simple word encryption and decryption.
	3. Test a file encryption (32 bytes block encryption with a padding to 64).
	4. Creation of the main application.

The main application is a database of my passwords. It will encrypt and decrypt a file that contains my passwords. 

<u>The command syntax :</u>
	./Ksecret $key $mode $file

<u>Required :</u>
	**[$key]** The secret key used to decrypt and encrypt the file
	**[$file]** The path of the file. If no mode is specified, the application will load into memory the decrypted file with the key. If a mode is specified, the application will encrypt/decrypt the file to let the user manage the file. 

<u>Optional :</u>
	**[$mode]** The mode if used to encrypt (--e) or decrypt (--d) the specified file.

<u>Examples :</u>

	* ./Ksecret -D -k "MySecretKey" -f ./MyPasswordFile  // Decrypt the specified file
	* ./Ksecret -E -k "MySecretKey" -f ./MyPasswordFile  // Encrypt the speficied file
	* ./Ksecret -k "MySecretKey" -f ./MyPasswordFile     // Use the application to manage the specified file
