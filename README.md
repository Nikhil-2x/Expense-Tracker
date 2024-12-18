# Expense Tracker 
- ### Created using ***JAVA*** and ***MYSQL***.

- ### If you wanna ***clone*** the project in ***netbeans IDE***(for apache netbeans IDE 23):
    > Go to team(at top) -> Git -> Clone -> Paste the URL of repo and enter credentials -> Finish

- ### Database code used for project(___for reference___):
```sql
CREATE DATABASE spendingdb;
USE spendingdb;

DROP TABLE IF EXISTS category_info, spendings, budgets;
CREATE TABLE category_info (
    category_name VARCHAR(100) PRIMARY KEY
    );
CREATE TABLE spendings (
    expense_id INT AUTO_INCREMENT PRIMARY KEY,
    category_name VARCHAR(100),
    amount INT NOT NULL,
    expense_date DATE NOT NULL,
    FOREIGN KEY (category_name) REFERENCES category_info(category_name)
);
CREATE TABLE budgets (
    budget_id INT AUTO_INCREMENT PRIMARY KEY,
    category_name VARCHAR(100),
    budget_amount INT NOT NULL,
    FOREIGN KEY (category_name) REFERENCES category_info(category_name)
);
```

- ### Video showing the working of Project:
    https://github.com/user-attachments/assets/4cc0ac0d-f55f-4e53-ab32-953c8ab9415d
