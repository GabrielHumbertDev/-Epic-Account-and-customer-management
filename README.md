# Epic Account and customer management2

Project Overview

EpicAccountAndCustomerManagement is a Java-based banking system developed using Object-Oriented Design (OOD) principles.
The project follows a user-story-driven specification where a bank teller can manage customers and their accounts through a central controller.

The system demonstrates:

- Inheritance & polymorphism
- Encapsulation and abstraction
- Defensive programming and validation
- UML-driven design compliance

**Project structure**

- EpicAccountAndCustomerManagement/
- |
- |--Account.java
- |--CheckingAccount.java
- |--SavingsAccount.java
- |
- |--Customer.java
- |--Person.java
- |--Company.java
- |
- |--AccountController.java
- |--Runner.java


***
## EpicAccountAndCustomerManagement
About the project

This project is a simple banking system built in Java as part of an Object-Oriented Design exercise.
It follows a set of user stories where a bank teller can create customers, open accounts, charge fees and remove customers or accounts.

The main aim of the project is to practise:

- object-oriented programming in Java
- working from UML and written specifications
- clean, safe code with basic validation


## What the system can do
**Customers**

- Create customers as either a Person or a Company
- Customers are abstract, so they can only exist as a specific type
- Each customer gets an automatically generated ID
- (starts at 2,000,000 and increases by 7)
- Customers store: name, address and a list of their accounts
- Names and addresses are validated so they cannot be null, empty, or just spaces


**Accounts**

- Create CheckingAccount or SavingsAccount
- Accounts are abstract and cannot be created directly
- Each account has: a unique account ID (long, starting at 1000, increasing by 5) and a balance
- Accounts can be added to or removed from customers safely


**Account behaviour**

**CheckingAccount**

- Tracks cheque numbers starting at 1
- You can: check the next number without incrementing and issue a cheque number which then increments


**SavingsAccount**

- Does not allow overdrafts
- If a withdrawal is larger than the balance, nothing is deducted
- Supports interest calculation


**Charging fees**

- Person customers are charged the same fee on all accounts
- Company customers: checking accounts are charged normally and savings accounts are charged double
- Negative or zero fees are ignored

**Design choices**

- Customer and Account are abstract to prevent incorrect instantiation
- Inheritance is used for specialised behaviour
- Validation is done in the controller and also in constructors to protect the model
- Internal lists in the controller are protected to avoid accidental modification
- IDs are generated automatically and never passed into constructors


## How to run it
1. Open the project in Eclipse or IntelliJ
1. Make sure all classes are in the EpicAccountAndCustomerManagement package
1. Run the Runner class
1. The console output shows:
- customer and account creation
- validation checks
- charging fees
- removing accounts and customers


## Support
If you need help with this project or have questions about how it works, you can get in touch using the details below.

Gabriel Gomes

## Contributing
State if you are open to contributions and what your requirements are for accepting them.

For people who want to make changes to your project, it's helpful to have some documentation on how to get started. Perhaps there is a script that they should run or some environment variables that they need to set. Make these steps explicit. These instructions could also be useful to your future self.

You can also document commands to lint the code or run tests. These steps help to ensure high code quality and reduce the likelihood that the changes inadvertently break something. Having instructions for running tests is especially helpful if it requires external setup, such as starting a Selenium server for testing in a browser.

## Authors and acknowledgment
Gabriel Humberto Avelino Gomes Arevalo
FDM Group Consultant  – UK
BSc (Hons) Computer Science – Cyber Security
Graduate Software Engineer (Java)

## License
For open source projects, say how it is licensed.

## Project status
Future Improvements 

Persist customers/accounts to a database

Add unit tests (JUnit)

Introduce transaction history

Improve UI (CLI or GUI)
