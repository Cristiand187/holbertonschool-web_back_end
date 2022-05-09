# 0x06. Basic authentication

## :books: Resources
Read or watch:
* [REST API Authentication Mechanisms](https://intranet.hbtn.io/rltoken/Yx1Na2qEzCLnke8RnpACDw)
* [Base64 in Python](https://intranet.hbtn.io/rltoken/R2kTeyWl2ef19mdxQuffww)
* [HTTP header Authorization](https://intranet.hbtn.io/rltoken/5BfGd-_oV9Asi_Ymi_lRSA)
* [Flask](https://intranet.hbtn.io/rltoken/3ivma6PpGZfjzDrA2zLq7g)
* [Base64 - concept](https://intranet.hbtn.io/rltoken/8ckHTvJq00WnvgEmn6GGtg)

---
## :bulb: Learning Objectives
What you should learn from this project:

* What authentication means
* What Base64 is
* How to encode a string in Base64
* What Basic authentication means
* How to send the Authorization header

---
## :computer: Task

### [0. Simple-basic-API](./api/v1/app.py)
Download and start your project from this archive.zip


### [1. Error handler: Unauthorized](./api/v1/app.py)
What the HTTP status code for a request unauthorized? 401 of course!


### [2. Error handler: Forbidden](./api/v1/auth)
What the HTTP status code for a request where the user is authenticate but not allowed to access to a resource? 403 of course!


### [3. Auth class](./api/v1/auth/auth.py)
Now you will create a class to manage the API authentication.
 * Create a folder api/v1/auth
 * Create an empty file api/v1/auth/__init__.py
 * Create the class Auth:
	 * in the file api/v1/auth/auth.py
 * import request from flask
 * class name Auth
 * public method def require_auth(self, path: str, excluded_paths: List[str]) -> bool: that returns False - path and excluded_paths will be used later, now, you don’t need to take care of them
 * public method def authorization_header(self, request=None) -> str: that returns None - request will be the Flask request object
 * public method def current_user(self, request=None) -> TypeVar('User'): that returns None - request will be the Flask request object


### [4. Define which routes don't need authentication](./api/v1/app.py)
Update the method def require_auth(self, path: str, excluded_paths: List[str]) -> bool: in Auth that returns True if the path is not in the list of strings excluded_paths:


### [5. Request validation!](./api/v1/app.py)
Now you will validate all requests to secure the API:


### [6. Basic auth](./api/v1/auth/basic_auth.py)
Create a class BasicAuth that inherits from Auth. For the moment this class will be empty.


### [7. Basic - Base64 part](./api/v1/auth/basic_auth.py)
Add the method def extract_base64_authorization_header(self, authorization_header: str) -> str: in the class BasicAuth that returns the Base64 part of the Authorization header for a Basic Authentication:


### [8. Basic - Base64 decode](./api/v1/auth/basic_auth.py)
Add the method def decode_base64_authorization_header(self, base64_authorization_header: str) -> str: in the class BasicAuth that returns the decoded value of a Base64 string base64_authorization_header:


### [9. Basic - User credentials](./api/v1/auth/basic_auth.py)
Add the method def extract_user_credentials(self, decoded_base64_authorization_header: str) -> (str, str) in the class BasicAuth that returns the user email and password from the Base64 decoded value.


### [10. Basic - User object](./api/v1/auth/basic_auth.py)
Add the method def user_object_from_credentials(self, user_email: str, user_pwd: str) -> TypeVar('User'): in the class BasicAuth that returns the User instance based on his email and password.


### [11. Basic - Overload current_user - and BOOM!](./api/v1/auth/basic_auth.py)
Now, you have all pieces for having a complete Basic authentication.


### [12. Basic - Allow password with ":"](./api/v1/auth/auth.py)
Improve the method def extract_user_credentials(self, decoded_base64_authorization_header) to allow password with :.


---

## Author
* **Cristian David Pineda Vargas** - [Cristiand187](https://github.com/Cristiand187)