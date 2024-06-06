# python-password-manager/generator

 Basic phyton scripts for password genertor and password manager

 Here is a short recording of the python scripts function when excuted:

 

https://github.com/Hasnake84/Python-password-manager/assets/114637978/8e461813-c29a-4ad6-8418-5b6402b22708

- import hashlib - This line imports the hashlib library, which lets the script scramble information (like a password) into a unique code.

- import getpass - This line imports the getpass library, which allows the script to hide what you type for your password when prompted. 

- password_manager = {} - This line creates a dictionary called password_manager. This dictionary will store usernames and passwords, but in a secure way to hold usernames and passwords, 
  but instead of the passwords being written out, they are hidden codes.

- def create_account(): - This defines a function called create_account that lets you create a new account.

- username = input("Enter your username: ") - This line asks you to type in a username and stores it in a variable named username.

- password = getpass.getpass("Enter your password: ") - This line asks you to type in a password, but hides what you type using getpass. It stores the password in a variable named password. 

- hashed_password = hashlib.sha256(password.encode()).hexdigest() - This line uses the hashlib library to scramble the password you entered. It converts it into a code using a method called 
  sha256 and then stores that code in a variable named hashed_password.

- password_manager[username] = hashed_password - This line adds the username you entered (the label) and the scrambled password (the secret code) to the password_manager dictionary, 
  effectively creating your account.
- print("Account created successfully") - This line prints a message that your account has been created successfully.

- def login(): - This defines a function called login that lets you log in to an existing account.

- username = input("Enter your username: ") - This line asks you to type in your username and stores it in a variable named username. 

- password = getpass.getpass("Enter your password: ") - This line asks you to type in your password, but hides what you type using getpass. It stores the password in a variable named 
  password. 

- hashed_password = hashlib.sha256(password.encode()).hexdigest() - This line scrambles the password you entered for login using hashlib in the same way it did when creating an account. 

- if username in password_manager.keys() and password_manager[username] == hashed_password: - This line checks if the username you entered exists in the password_manager dictionary and if 
  the scrambled code you just created (hashed_password) matches the scrambled code stored for that username in the dictionary. If both conditions are true, it means you entered the correct 
  username and password.

- print("Login successful") - If the username and password match, this line prints a message that your login was successful.

- else: - If the username or password doesn't match what's stored in the dictionary, this block runs.

- print("Invalid username or password.") - This line prints a message that the username or password was invalid.






 this script is a simple password generator. It creates a password with a mix of uppercase and lowercase letters, numbers, and symbols, making it more secure. You can change the length of the password by modifying the number you provide when calling the generate_password function.
