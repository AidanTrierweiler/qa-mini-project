# Login Feature Test Cases

**Application / Website:** https://the-internet.herokuapp.com/login
**Environment:** Production / Test



## TC-01: Login with valid credentials

**Preconditions:**  
User is on the login page

**Steps:**
1. Navigate to the login page
2. Enter username "tomsmith"
3. Enter password "SuperSecretPassword!"
4. Click Login

**Expected Result:**  
User is logged in successfully and redirected to the secure area

**Actual Result:**  
A green success message is displayed stating "You logged into a secure area!".  
User is redirected to the Secure Area page with a welcome message and a Logout button.

**Status:**  
Pass


## TC-02: Login with invalid credentials

**Preconditions:**
User is on the login page

**Steps**
1. Navigate to the login page
2. Enter username tomsmith
3. Enter Password "Password"
4. Click Login

**expected result:**
User is not logged in.  
An error message indicating invalid credentials is displayed.  
User remains on the login page.

**Actual Result:**  
A red error message is displayed at the top of the page stating "Your password is invalid!".  
The user remains on the login page and the username and password fields are cleared.

**Status:**  
Pass


## TC-03: Login with empty fields

**Preconditions:**  
User is on the login page

**Steps:**
1. Navigate to the login page
2. Leave the username field empty
3. Leave the password field empty
4. Click Login

**Expected Result:**  
User is not logged in.  
Validation or error message is displayed.  
User remains on the login page.

**Actual Result:**  
A red error message is displayed at the top of the page stating "Your username is invalid!".
The user remains on the login page

**Status**
Pass


## TC-04: Logout from secure area

**Preconditions:**  
User is logged into the secure area

**Steps:**
1. Log in with valid credentials
2. Click the Logout button

**Expected Result:**  
User is logged out successfully.  
User is redirected to the login page.  
A confirmation message is displayed.

**Actual Result:**  
A confirmation message is displayed stating "You logged out of the secure area!".  
User is redirected to the login page.

**Status:**
Pass