This project is a **Python-based ATM Management System** designed to demonstrate the core principles of Object-Oriented Programming (OOP) in a practical, real-world scenario.

Instead of just writing a script that calculates numbers, I structured it as a proper banking simulation to show how different parts of a system interact securely and efficiently.

### **What the Project Does**

It simulates a fully functional ATM interface where a user can perform standard banking operations.

* **Check Balance:** Users can view their current funds securely.
* **Deposit Money:** Allows adding funds with validation to ensure amounts are positive.
* **Withdraw Money:** Includes checks for sufficient funds and valid input before processing.
* **Account Details:** displays the user's name, account number, and balance in a formatted report.

### **The Technical "Why" (OOP Concepts Used)**

I built this specifically to showcase how OOP makes code safer and more organized:

* **Encapsulation (Security):** I made sensitive data like the `__balance` private so it can't be directly modified from outside the class. You have to go through specific methods (getters/setters) to change it, just like a real bank prevents direct database access.
* **Inheritance:** I created a hierarchy where the `ATM` class inherits features from a generic `Account` class. This means we can easily expand the system later (e.g., adding a "CreditCard" class) without rewriting the base logic.
* **Polymorphism:** The system uses method overriding for the `transaction()` function. The generic account has one definition, but the ATM class overrides it to provide its own specific behavior.
* **Abstraction:** I used an abstract base class (`BankAccount`) to enforce a blueprint. It ensures that any future account type added to the system *must* implement a transaction method, keeping the code consistent.

### **How It Runs**

The program features a **menu-driven loop** that keeps the session alive until the user chooses to exit. It’s interactive, asking for user input at each step and providing immediate feedback (like "Deposit successful!" or "Insufficient balance!").

**Would you like me to add a feature to simulate a PIN verification step for added security?**
