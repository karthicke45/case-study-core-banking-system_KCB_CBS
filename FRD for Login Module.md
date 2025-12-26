# **📄 Functional Requirements Document (FRD)**

 **Screen:** Login  
 **Module:** Login  
 **Project:** Core Banking System – Kongu Co-operative Bank (KCB CBS)  
 **Prepared By:** Karthick E  
 **Date:** December 2025  
 **Version:** 1.0

---

## 

## **Login Screen** 

## **1\. Introduction**

The Login screen allows registered users of the Kongu Co-operative Bank Core Banking System (KCB CBS) to securely access the web platform using their username and password.

It also provides navigation options for **new user registration** and **password/username recovery**.

## **2\. Actors & Preconditions**

* **Actors:** All the users of the platform namely,   
  ♦ Kongu Co-operative Bank customers  
  ♦ Admin  
  ♦ Branch Manger  
  ♦ Loan Officer.

* **Preconditions:**  
  ♦ User must visit the KCB  official website and navigate to the KCB CBS Login page.

## 

## 

## 

## 

## 

## 

## **3\. Business Rules**

| Business Rules |  |
| ----- | :---- |
| BR01 | The scene sequence/ user navigation should be as per the wireframes. |
| BR02 | System messages (Alerts, Warnings, Success, Failure messages) should be as given in the Use case table. |
| BR03 | Validation for each field should be done as per the instructions given in “Field Level Validations” table. |
| BR04 | The user must have completed the first-time setup in the KCB CBS platform in order to log in successfully. |
| BR05 | When user fails to enter the OTP within time (3 minutes), the OTP already sent should become expired.  |
| BR06 | When user clicks “Resend OTP” link, system should send another OTP to user’s registered mobile number. |
| BR07 | When the user enter incorrect password or username for more than 3 time user account will be locked, the user can either,  i) Contact the KCB CBS Admin or Bank branch to unlock the user account, Or  ii) Wait for 30 minutes to unlock the user account. |
| BR08 | If the user clicks the forgot username / Password link the system should navigate the user to the forgot username / Password screen. |
| BR09 | If the user is inactive for 10 minutes, the system should log out automatically for security. |
| BR10 | User doesn’t receive OTP to the registered mobile number, the user need to contact the bank branch or the platform admin. |

## 

## 

## 

## 

## **4\. Functional Requirements**

| \# | Label/ Field Name/ Data Type | Validation | Rule |
| ----- | ----- | ----- | ----- |
| **Login Screen** |  |  |  |
| FR01 | Username (Input field)   | Allow the following characters:     ♦ Upper case letters \[A-Z\]    ♦ Lower case letters \[a-z\]    ♦ Numerals \[0-9\]    ♦ Special Characters \[\~, \!, @, \#, $, %, \_, \-\] MaximumCharacter Limit: 20 | The Username field is mandatory. The Username field is active by default. The Username field must not allow spaces. The Username field must have a minimum of 6 characters. The Username field is case-sensitive.  |
| FR02 | Password (Input field) | Allow the following characters. ♦ Upper case letters \[A-Z\] ♦ Lower case letters \[a-z\] ♦ Numerals \[0-9\] ♦ Special Characters \[\~, \!, @, \#, $, %, \_, \-\] Maximum Character Limit: 16 Minimum Characters Limit: 8 |  Password is a mandatory field The password field should be active by default.  Password field should not allow any spaces. When the  user enters a password it should be masked in asterisks, the password should be visible only when the user clicks the eye icon. The password field is case sensitive. |
| FR03 | Login button | NA | Login button should be active by default When the user clicks the Login button, the system should validate the entered username and password. If valid, the user is redirected to the OTP screen **For error messages refer:**  AF03,AF05 |
| FR04 | Forgot Username/ Password (link) | NA |  Forgot Username/ Password link should be active by default.  When the user clicks the 'Forgot Username/Password' link, a popup appears allowing them to choose between recovering their username or resetting their password. |
| FR05 | New User ? Register here  (link) | NA | New User ? Register here link should be active by default.  When the user clicks the “New User ? Register here” link system should navigate the user to the first time account setup screen. |
| **OTP Screen** |  |  |  |
| FR06 | OTP Input Boxes (Input fields) | Allow only numeric values \[0-9\] | There should be 6 inputs boxes as shown in the wireframe.  The cursor should be in the first input box by default.  When a user enters a numeric value, the focus should automatically be shifted to the next input box. This should happen till the focus reaches the last input box. |
| FR07 | Resend OTP (link) | NA | Resend OTP link  Should be active by default.  When a user clicks this link, system should send a new OTP to user’s registered mobile number. OTP is valid for only 3 minutes. This link becomes inactive after the user uses it for 3 times for 30 minutes. **For error messages refer:**  AF01 |
| FR08 | Verify Button | NA | Verify button should be inactive by default. It should become active when 6 digits of OTP have been entered. When the user clicks the Verify button, the system should validate if the OTP entered is correct. If so, the system should navigate users to the specific user’s  dashboard. **For error messages refer:**  AF02,AF03,AF04 |
| FR09 | Time Remaining  (Read only field)  | NA | Time Remaining is a read only field, and cannot be edited.  It shows the remaining time before the OTP expires. |

## **First Time Setup Screen** 

## **1\. Introduction**

The First-Time Setup screen allows existing Kongu Co-operative Bank account holders to register for online banking services on the KCB CBS platform.Users can verify their account details and authenticate themselves using an OTP and ATM card validation.Upon successful setup, users can create their login credentials and gain secure access to the platform.

## **2\. Actors & Preconditions**

* **Actors:** Kongu Co-operative Bank customers  
    
* **Preconditions:**  
  ♦ User should already have an active bank account in Kongu Cooperative Bank


## **3\. Business Rules**

| Business Rules |  |
| ----- | :---- |
| BR01 | The scene sequence/ user navigation should be as per the wireframes. |
| BR02 | System messages (Alerts, Warnings, Success, Failure messages) should be as given in the Use case table. |
| BR03 | Validation for each field should be done as per the instructions given in “Field Level Validations” table. |
| BR04 | The user registering for KCB CBS digital banking must have an active bank account with Kongu Co-operative Bank. |
| BR05 | The user must provide the mobile number registered with the bank at the time of account creation for verification purposes. |
| BR06 | When a user clicks the “Resend OTP” link, the system should send another OTP to the user's registered mobile number. |
| BR07 | If the user has already registered for online banking then an error message will appear asking the user to login directly. |
| BR08 | If the user’s account is already registered for internet banking, they need to  login directly. |
| BR09 | If the user is inactive for 10 minutes, the system should log out automatically for security. |
| BR10 | User doesn’t receive OTP to the registered mobile number, the user need to contact the bank branch or the platform admin. |

## **4\. Functional Requirements**

| \# | Label/ Field Name/ Data Type | Validation | Rule |
| ----- | ----- | ----- | ----- |
| **First Time Setup Screen** |  |  |  |
| FR01 | Bank Account Number. (Input field)   | Allow the following characters:     ♦ Numbers  \[0-9\] Maximum and Minimum Character Limit : 16 | Bank Account number is a mandatory field. Bank Account Number field  is active by default. This field does not allow any spaces. |
| FR02 | CIF Number (Input field) | Allow the following characters. ♦ Numbers  \[0-9\] Maximum and Minimum Character Limit: 11 | CIF number is a mandatory field. This field  is active by default. This field does not allow any spaces. |
| FR03 | Branch Code (Read only field) | NA | Branch Code  is a read only field The Branch Code field will remain blank initially. Once the user enters a valid account number, the Branch Code field will be automatically populated based on the entered account number. |
| FR04 | Registered Mobile Number (link) | Allow the following characters. ♦ Numbers  \[0-9\] Maximum and Minimum Character Limit: 10 |  Registered Mobile number is a mandatory field. This field  is active by default. This field does not allow any spaces. User’s mobile number must be the registered number linked to their KCB account. |
| FR05 | Enter the text as shown in the image (Input fields) | Allow the following characters:     ♦ Upper case letters \[A-Z\]    ♦ Lower case letters \[a-z\]    ♦ Numerals \[0-9\] Maximum and Minimum Character Limit: 5 |  User entered cache should match with image shown This field is case sensitivity. This field is active by default. This is a mandatory field. |
| FR06 | Cancel button  | NA |  Cancel button should be active by default.  When the user clicks the cancel button the user will be navigated to the login screen.  User entered data will not be saved. |
| FR07 | Submit button | NA |  The submit button should be active by default.  When a user clicks the submit button all the data will be validated, if valid a user will be navigated to the OTP screen. If in valid the system will display error messages **For error messages refer:**  AF1, AF2,AF3 |
| **OTP Screen** |  |  |  |
| FR08 | OTP Input Boxes (Input fields) | Allow only numeric values \[0-9\] | There should be 6 inputs boxes as shown in the wireframe.  The cursor should be in the first input box by default.  When a user enters a numeric value, the focus should automatically be shifted to the next input box. This should happen till the focus reaches the last input box. |
| FR09 | Resend OTP (link) | NA | Resend OTP link  Should be active by default.  When a user clicks this link, system should send a new OTP to user’s registered mobile number. OTP is valid for only 3 minutes. This link becomes inactive after the user uses it for 3 times for 30 minutes. **For error messages refer:**  AF04, AF05 |
| FR10 | Verify Button | NA | Verify button should be inactive by default. It should become active when 6 digits of OTP have been entered. When the user clicks the Verify button, the system should validate if the OTP entered is correct. If so, the system should navigate users to the specific user’s  dashboard. **For error messages refer:**  AF04, AF05 |
| FR11 | Time Remaining  (Read only field)  | NA | Time Remaining is a read only field, and cannot be edited.  It shows the remaining time before the OTP expires. |
| **ATM Card Verification Screen** (After the OTP screen, a popup appears. If the user chooses the "**I have an ATM card**" option, they will be navigated to the **ATM Card Verification screen**. ) |  |  |  |
| FR12 | Card Number (Input field) | Allow the following characters:     ♦ Numbers  \[0-9\] Maximum and Minimum Character Limit : 16 | Card number is a mandatory field. Card Number field  is active by default. This field does not allow any spaces.  |
| FR13 | Expiry Date (Input field) | Allow the following characters:     ♦ Numbers  \[0-9\] Maximum and Minimum Character Limit : 4 | Expiry date is a mandatory field. This field  is active by default. This field does not allow any spaces. |
| FR14 | Cardholder Name (Input field) | Allow the following characters:     ♦ Upper case letters \[A-Z\]    ♦ Lower case letters \[a-z\]    ♦ Space  Maximum and Minimum Character Limit: 25 |  Cardholder name is mandatory by default. When the user enters any alphabets, they will be automatically converted to uppercase. This field is active by default.  |
| FR15 | ATM PIN (Input field) | Allow the following characters:     ♦ Numbers  \[0-9\] Maximum and Minimum Character Limit : 4 | ATM PIN  is a mandatory field. This field  is active by default. This field does not allow any spaces. |
| FR16 | Enter the text as shown in the image (Input field) | Allow the following characters:     ♦ Upper case letters \[A-Z\]    ♦ Lower case letters \[a-z\]    ♦ Numerals \[0-9\] Maximum and Minimum Character Limit: 5 |  User entered cache should match with image shown This field is case sensitivity. This field is active by default. This is a mandatory field. |
| FR17 | Cancel Button | NA |  Cancel button should be active by default.  When the user clicks the cancel button the user will be navigated to the login screen.  User entered data will not be saved. |
| FR18 | Submit button | NA |  The submit button should be active by default.  When a user clicks the submit button all the data will be validated, if valid a user will be navigated to the OTP screen. If in valid the system will display error messages **For error messages refer:**  AF06, AF03, |

