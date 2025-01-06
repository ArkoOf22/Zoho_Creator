A simple library system created with the help of Zoho Creator.
It has the following functionalities:-
Task 1: Create Modules and Forms 
1.Books Module 
oCreate a form with the following fields:  
Book ID (Auto-generated) 
Title (Text - Mandatory) 
Author (Text - Mandatory) 
Genre (Dropdown - Predefined values: Fiction, Non-Fiction, Sci-Fi, Biography) 
Publication Year (Number - Only valid years between 1900 and the current 
year) 
Available Copies (Number - Mandatory, minimum value = 0) 
ISBN Number (Text - Unique validation) 
Rating (Number - Accept values between 1 to 5) 
2.Members Module 
oCreate a form with the following fields:  
Member ID (Auto-generated) 
Name (Text - Mandatory) 
Email (Email - Validate for proper email format) 
Phone Number (Number - Mandatory, validate for 10 digits) 
Membership Start Date (Date - Default to the current date) 
Membership Type (Dropdown - Values: Basic, Premium, Elite) 
Max Books Allowed (Number - Auto-filled based on Membership Type: 
Basic=2, Premium=5, Elite=10) 
3.Transactions Module 
oCreate a form with the following fields:  
 
Transaction ID (Auto-generated) 
Member (Lookup to Members) 
Book (Lookup to Books) 
Issue Date (Date - Default to the current date) 
Return Date (Date - Must be greater than Issue Date) 
Status (Dropdown - Values: Issued, Returned, Overdue) 
Fine Amount (Currency - Auto-calculated for overdue books) 
4.Staff Members Module 
oCreate a form with the following fields:  
Staff ID (Auto-generated) 
Name (Text - Mandatory) 
Email (Email - Validate for proper email format) 
Role (Dropdown - Values: Librarian, Assistant) 
Phone Number (Number - Mandatory, validate for 10 digits) 
 
Task 2: Implement Form Validations 
1.Books Form 
oEnsure ISBN Number is unique. 
oValidate Publication Year to accept only years between 1900 and the current year. 
2.Members Form 
oPrevent duplicate entries based on the Email field. 
oAutomatically populate Max Books Allowed based on the selected Membership 
Type. 
3.Transactions Form 
oPrevent transactions if Available Copies of the selected book is 0. 
oValidate Return Date to ensure it is later than the Issue Date. 
 
Task 3: Create Workflows 
1.Books Module: 
oAutomatically decrease Available Copies by 1 when a book is issued. 
oAutomatically increase Available Copies by 1 when a book is returned. 
2.Transactions Module: 
oCalculate Fine Amount for overdue books ($2 per day overdue). 
oSend an email to members for overdue books, including fine details. 
3.Members Module: 
oSend a welcome email to new members upon form submission. 
4.Staff Members Module: 
oSet role-based permissions:  
Librarians can issue and return books. 
Assistants can only view books and members but cannot make changes.
