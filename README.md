'credentialsCheck.py' will verify whether a login attempt is valid and successful.

The script requires a recent version of Python to run.
Additionally, the following will be required in the same directory:
- 'user_login.txt'
- 'loginAttempt.txt'
- 'credentialsCheckSrv.txt'

Optional files:
- 'authorizationResults.txt' (will be created if it does not already exist)

Before requesting data, ensure 'user_login.txt', the database of existing credentials, is updated.
Odd-numbered lines will have usernames and even-numbered lines will have the corresponding passwords.
'loginAttempt.txt' will have the credentials to be verified, with the username on line 1 and password on line 2.

To request data, place the credentials to be verified in 'loginAttempt.txt' (line 1: username, line 2: password).
Run 'credentialsCheck.py'; an example request via the MS Windows command line is as follows:
"python credentialsCheck.py"

'credentialsCheck.py' will import the credentials database. 'credentialsCheck.py' will check whether 'credentialsCheckSrv.txt' has 'run' in the file before returning whether the login attempt was valid via 'loginAttempt.txt'. Access this file to receive the text, which will include one of the following strings:
- "access granted" (login attempt was successful)
- "wrong username" (login attempt had the wrong username)
- "wrong password" (login attempt had the wrong password but a correct username)

![UMLsequence](https://github.com/knoowin/CS361-Project-JI/blob/master/UMLsequence_R1.jpg)

