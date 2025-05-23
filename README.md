# 🛡️ Simple PHP Login & Register System

This is a basic user authentication project built with PHP and MySQL. It includes secure registration and login features, styled with custom CSS.

---

## 🚀 Features

- ✅ User Registration with secure password hashing (`password_hash`)
- ✅ User Login with password verification (`password_verify`)
- ✅ Error and success messages with styled feedback
- ✅ Simple and clean UI using custom `login.css`
- ✅ Prepared for redirection after login/registration

---

## 🗂️ File Structure

```bash
📁 login/
├── login.php # Login form + login logic
├── register.php # Registration form + registration logic
├── register.css # # Styles for register boxes
├── login.css # Styles for login box
├── db.php # Database connection (you must create this)
└── README.md # You are here.
```


---

## 💾 Database Setup

Create a MySQL database and use the following SQL to create the `users` table:

```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(255) NOT NULL,
  password VARCHAR(255) NOT NULL
);
```

Make sure your ```db.php``` file contains the correct database credentials and connection like this:

```php
<?php
$host = "localhost";
$dbname = "your_database_name";
$username = "root"; // or your MySQL username
$password = "";     // or your MySQL password

$conn = new PDO("mysql:host=$host;dbname=$dbname", $username, $password);
?>
```

## 🎨 UI Preview
The form is centered with a dark background and styled buttons and inputs.
Hovering over links changes color, and alert messages appear in styled divs like:

```html
<div class="success">Login successful!</div>
<div class="error">Username or password is wrong.</div>
```

## ⚠️ Notes
No JavaScript used — purely PHP + CSS

Does not include CSRF protection or advanced session handling (for simplicity)

For production: sanitize inputs, validate more thoroughly, and use HTTPS.

## 🧠 Inspiration
Made for learning PHP authentication basics and practicing Git + GitHub version control.





