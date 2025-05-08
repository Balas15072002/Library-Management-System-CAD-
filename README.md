# Readify – Library Management System

**Type:** B2C (Business-to-Consumer)  
**Target Audience:**  
Students, Teachers, Librarians, Aspirants, Bookworms, Narrators, Directors, and Poets

**Timeline:** Approximately 3 Weeks  
**Budget:** ₹10,00,000 (10 Lakhs)  
**Team Size:** 10 Members  

---

## Project Overview

**Readify** is a full-stack Library Management System designed for both library staff and end users. The platform allows librarians to manage book inventory efficiently, while users can explore, borrow, and purchase books with ease. It includes borrowing history, fine management, UPI payments, and real-time recommendations.

---

## Key Features

### Librarian Features
- Register and login with role-based access control
- Add, update, and remove books
- View book details along with cover pages
- Search and filter books by title, author, or genre
- Receive notifications when books are borrowed
- Low stock alerts and return due reminders
- Manage book quantities and stock
- View user profiles and borrowing history
- Fine management for overdue books
- Handle book returns with user feedback
- Optimize storage space (Shelf tracking)

### User Features
- Separate registration and login for users
- View book details and first-page preview
- Borrow books directly
- View available discounts
- Search and filter by genre, title, author, or rating
- View trending and recommended books
- Add books to a wishlist
- Purchase books using UPI (GPay, PhonePe, etc.)
- Submit feedback or reviews
- Provide comments during book returns

---

## Model Classes

### 🔹 User
- int userId  
- String name  
- String email  
- long contact  
- LocalDate dateOfBirth  
- String address  
- String password  
- String confirmPassword  

### 🔹 Librarian
- int librarianId  
- String name  
- String email  
- long contact  
- LocalDate dateOfBirth  
- String address  
- String password  
- String confirmPassword  

### 🔹 Book
- int bookId  
- String name  
- String author  
- String isbn  
- int quantity  
- double price  
- String genre  
- int publishedYear  
- int volume  
- boolean isAvailable  
- double rating  

### 🔹 Feedback
- int feedbackId  
- int userId  
- int bookId  
- String comments  
- int rating  

### 🔹 Transaction
- int transactionId  
- String paymentMethod // GPay, PhonePe, etc.  
- int userId  
- int bookId  
- LocalDate borrowedDate  
- LocalDate returnDate  
- boolean isReturned  
- double fine  

### 🔹 Notification
- int notificationId  
- String message  
- LocalDate timestamp  

### 🔹 Storage
- int shelfNumber  
- int capacity  
- int usedSpace  

### 🔹 Wishlist
- int userId  
- List<Book> wishlistItems  
