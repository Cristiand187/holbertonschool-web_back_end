# 0x05. Personal data

## :books: Resources
Read or watch:
* [What Is PII, non-PII, and Personal Data?](https://intranet.hbtn.io/rltoken/FaZWPLxHKDZvFZEDZQV9nA)
* [logging documentation](https://intranet.hbtn.io/rltoken/xewrTdbrEf3oSp-a57a0fA)
* [bcrypt package](https://intranet.hbtn.io/rltoken/ra_k0Qm-tvET0t7_UrZY8A)
* [Logging to Files, Setting Levels, and Formatting](https://intranet.hbtn.io/rltoken/rhzX06XnvjLHUhUOGNUkAA)

---
## :bulb: Learning Objectives
What you should learn from this project:


*           mandatory
*         

---
## :computer: Task

### [0. Regex-ing](./filtered_logger.py)
Write a function called filter_datum that returns the log message obfuscated: 
 * Arguments:
	 * fields: a list of strings representing all fields to obfuscate
 * redaction: a string representing by what the field will be obfuscated
 * message: a string representing the log line
 * separator: a string representing by which character is separating all fields in the log line (message)
 * The function should use a regex to replace occurrences of certain field values.
 * filter_datum should be less than 5 lines long and use re.sub to perform the substitution with a single regex.


### [1. Log formatter](./filtered_logger.py)
Copy the following code into filtered_logger.py.


### [2. Create logger](./filtered_logger.py)
Use user_data.csv for this task


### [3. Connect to secure database](./filtered_logger.py)
Database credentials should NEVER be stored in code or checked into version control. One secure option is to store them as environment variable on the application server.


### [4. Read and filter data](./filtered_logger.py)
Implement a main function that takes no arguments and returns nothing.


### [5. Encrypting passwords](./encrypt_password.py)
User passwords should NEVER be stored in plain text in a database.


### [6. Check valid password](./encrypt_password.py)
Implement an is_valid function that expects 2 arguments and returns a boolean.

---

## Author
* **Cristian David Pineda Vargas** - [Cristiand187](https://github.com/Cristiand187)