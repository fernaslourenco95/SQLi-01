# SQLi-01
## SQL injection vulnerability in WHERE clause allowing retrieval of hidden data.
### Overview

This project demonstrates a SQL Injection vulnerability in a WHERE clause that allows attackers to retrieve hidden or unauthorized data from a database using Burp Suite.
The vulnerability occurs when user input is improperly sanitized and directly included in SQL queries.

## Vulnerability Description

The application builds SQL queries dynamically using user-supplied input or Burp. When this input is not properly validated or parameterized, an attacker can manipulate the query logic.

## PoC
01:

![SQLi ](https://github.com/user-attachments/assets/7fd8c1e6-68c7-419b-a5fc-7cd63929660e)

02:
![SQLi 1](https://github.com/user-attachments/assets/61f108bf-ed86-4352-8155-c1ad66884baa)

## Mitigation Strategies

### To prevent SQL Injection vulnerabilities:

1. Use Parameterized Queries
SELECT * FROM users WHERE username = ?;
2. Use Prepared Statements
Ensures input is treated as data, not executable code
3. Input Validation
Whitelist allowed characters
Reject suspicious patterns
4. Least Privilege Principle
Limit database user permissions
5. ORM Usage
Use secure frameworks that abstract SQL queries

## Conclusion

SQL Injection remains one of the most critical web security vulnerabilities. Proper input handling and secure coding practices are essential to protect applications and user data.
