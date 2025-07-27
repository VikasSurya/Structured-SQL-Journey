# 📅 Day 1: Before You Start SQL – Understand the Basics

---

## 🔹 What is SQL?

**SQL** stands for **Structured Query Language**.  
It’s a language we use to talk to databases.

For example:

- “Show me all customers older than 30.”
- “Tell me how much money we made this month.”

We can ask these questions to a database using SQL — and get the answers.

---

## 🔹 What is a Database?

Think of a **database** like a digital cupboard where data is stored neatly.

**Example:**

- **Cupboard** = Database  
- **Each shelf** = Table  
- **Things on the shelf** = Data  

Everything is stored in the right place and easy to find.

---

## 🔹 File System vs Database

Imagine having **500 Excel files** and trying to find the **top 5 customers** — total headache, right?  
But with everything inside a **database**, one small SQL query and boom – done!

---

## 🔹 Where is SQL Used in Real Life?

- Behind apps and websites (login info, orders, etc.)
- Reporting tools like **Power BI** or **Tableau**
- Used daily by **Data Analysts**, **Developers**, **Testers** – almost everyone in tech!

---

## 🔹 What is DBMS?

**DBMS** = **Database Management System**  
It’s a software that manages databases.

It handles:

- Who can access the data  
- Managing multiple users  
- Keeping the data safe and organized  

**Popular DBMS tools:** MySQL, PostgreSQL, SQL Server

---

## 🔹 What is a Server?

A **server** is a powerful computer that runs 24/7.  
It hosts your database so you (and your app or website) can access it anytime.

Nowadays, most servers run on the **cloud** – like **AWS**, **Azure**, or **Google Cloud**.

---

## 🔹 Different Types of Databases

| Type            | Description                                | Examples             |
|-----------------|--------------------------------------------|----------------------|
| **Relational**   | Stores data in tables, like Excel sheets   | MySQL, PostgreSQL    |
| **Key-Value**    | Like a dictionary – one key, one value     | Redis, DynamoDB      |
| **Column-Based** | Stores data column-wise, fast for reading | Cassandra, Redshift  |
| **Document-Based** | Stores full JSON documents              | MongoDB              |
| **Graph**        | Focuses on relationships, like social media| Neo4j                |

> ✅ Right now, we’re focusing on **Relational Databases** – that’s where SQL is used.

---

## 🔹 Structure of a Database (Hierarchy)
Server
 └── Database
      └── Schema (logical group of tables)
           └── Table
                ├── Columns (fields)
                └── Rows (data)
## ✅ Quick Summary

- SQL is a language to talk to databases.
- Databases help you store and manage data smartly.
- DBMS is the software that runs the database.
- Servers host databases – usually on the cloud.

