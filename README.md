Simulated Banking Project I made to start out in learning Java. Made with guidance from Coursera course by the University of Pennsylvania and Instructor Brandon Krakowsky.

---

# Banking System (Java)

A simple Java program that simulates a **banking system**.
It models **banks**, their **customers**, and each customer’s **bank accounts**, allowing for basic transactions such as deposits and withdrawals.

---

## 📂 Project Structure

```
banking/
├── Bank.java         # Entry point of the program (main method)
├── BankAccount.java  # Represents a customer's bank account
└── Customer.java     # Represents a bank customer
```

---

## ⚙️ Features

* Create a **Customer** with a name and address
* Create a **BankAccount** (checking or savings) for a customer
* Perform **deposits** and **withdrawals**
* Retrieve **account balance** and **customer information**
* Console-based interaction using `Scanner`

---

## 🚀 How to Run

### 1. Clone this repository

```bash
git clone https://github.com/your-username/banking-system.git
cd banking-system
```

### 2. Compile the program

Make sure you are in the **parent folder** of `banking/`:

```bash
javac banking/*.java
```

### 3. Run the program

```bash
java banking.Bank
```

---

## 🖥️ Example Interaction

```
Customer name: Alice
Customer address: 123 Main St
Account type (checking/savings): checking
Account number: 1001
Initial deposit: 500
Owner: Alice from 123 Main St
Balance: 500.0
```

---

## 📘 Concepts Demonstrated

* Java **classes and objects**
* **Encapsulation** with private fields and getters/setters
* **Packages** (`package banking;`)
* Basic **console input/output** with `Scanner`
* **OOP relationships** (a `Customer` "owns" a `BankAccount`)

---

## 🔧 Requirements

* Java JDK 8 or higher
* A terminal/command line (or an IDE such as VS Code, IntelliJ, or Eclipse)


UML Diagram: 

classDiagram
    class Bank {
        +main(String[] args) void
        +run() void
    }

    class Customer {
        -name : String
        -address : String
        +Customer(name : String)
        +setAddress(address : String) void
        +getName() String
        +getAddress() String
    }

    class BankAccount {
        -accountType : String
        -accountNumber : int
        -balance : double
        -customer : Customer
        +BankAccount(type : String, number : int, customer : Customer)
        +deposit(amount : double) void
        +withdraw(amount : double) boolean
        +getBalance() double
        +getCustomerInfo() String
    }

    Bank --> BankAccount : creates
    BankAccount --> Customer : belongs to

