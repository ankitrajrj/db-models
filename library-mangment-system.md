# Library Management System Entities With Attributes

[Click Here For Diagram](https://app.eraser.io/workspace/9XXFpBXwbbgsRxNUDn6F)


## 1. Students
- **Student_ID** (PK) - Unique student identifier
- **Name** - Student ka full name
- **Email** - Contact email
- **Phone_Number** - Contact number
- **Department** - Student ka department (CSE, ECE, etc.)
- **Library_Card_ID** (FK) - Library membership link
- **Registration_Date** - Library join date

## 2. Librarian
- **Librarian_ID** (PK) - Unique librarian identifier
- **Name** - Librarian name
- **Email** - Contact email
- **Phone_Number** - Contact number
- **Role** - Head Librarian / Assistant Librarian
- **Username** - Login username
- **Password** - Secure password

## 3. Staff
- **Staff_ID** (PK) - Unique identifier
- **Name** - Staff name
- **Email** - Contact email
- **Phone_Number** - Contact number
- **Role** - Assistant / Clerk
- **Assigned_Section** - Books category they manage

## 4. Books
- **Book_ID** (PK) - Unique identifier for each book
- **Title** - Book name
- **Author** - Book author
- **ISBN** - International Standard Book Number
- **Category** - Subject/Department-wise category
- **Publisher** - Name of the publisher
- **Edition** - Book edition
- **Price** - Book price
- **Quantity** - Available copies
- **Shelf_Location** - Book's shelf number

## 5. Reserve
- **Reserve_ID** (PK) - Unique reservation ID
- **Student_ID** (FK) - Who reserved the book
- **Book_ID** (FK) - Which book is reserved
- **Reserve_Date** - Date of reservation
- **Status** - Pending / Collected / Cancelled

## 6. Return
- **Return_ID** (PK) - Unique return ID
- **Loan_ID** (FK) - Reference to the issued book
- **Return_Date** - Actual return date
- **Condition** - Good / Damaged

## 7. Loan
- **Loan_ID** (PK) - Unique loan transaction ID
- **Student_ID** (FK) - Who borrowed the book
- **Book_ID** (FK) - Which book is borrowed
- **Issue_Date** - Date of issuing the book
- **Due_Date** - Last return date
- **Return_Date** - Actual return date
- **Fine_Amount** - Late fine if applicable

## 8. Fine
- **Fine_ID** (PK) - Unique fine ID
- **Loan_ID** (FK) - Reference to issued book
- **Student_ID** (FK) - Who has the fine
- **Amount** - Fine amount
- **Status** - Paid / Unpaid
- **Date_Issued** - Fine applied date

## 9. Reports
- **Report_ID** (PK) - Unique report ID
- **Generated_By** (FK) - Librarian ID
- **Report_Type** - Issued Books / Overdue Books / Fines Collected
- **Date_Generated** - Report creation date

## 10. Suppliers / Publishers
- **Supplier_ID** (PK) - Unique supplier ID
- **Name** - Publisher or supplier name
- **Contact_Person** - Person to contact
- **Phone_Number** - Contact number
- **Email** - Supplier email
- **Address** - Supplier address

## 11. Library Card
- **Library_Card_ID** (PK) - Unique card ID
- **Student_ID** (FK) - Assigned student
- **Issued_Date** - When card was issued
- **Expiry_Date** - Expiry date of card
- **Status** - Active / Expired

## 12. Departments
- **Department_ID** (PK) - Unique department ID
- **Department_Name** - CSE, ECE, ME, etc.

## 13. Events / Notices
- **Event_ID** (PK) - Unique event ID
- **Title** - Event name
- **Description** - Event details
- **Date** - Event date
- **Organizer** - Organized by whom
