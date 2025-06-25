
# Task 2 - SQL Developer Internship

This project demonstrates how to handle data insertion, NULL values, updates, deletions, and foreign key constraints in a relational database using MySQL.

## ✅ Objectives Covered
- Creating relational tables with constraints
- Inserting records with partial data (NULLs)
- Updating missing data
- Deleting incomplete or invalid records
- Using `ON DELETE CASCADE` to maintain referential integrity
- Creating archive tables using `INSERT INTO ... SELECT`
- Running queries to validate results

---

## 📂 Tables Created
- `Customers`
- `Products`
- `Orders`
- `ProductArchive`

## 📌 Key Concepts
- DML operations: `INSERT`, `UPDATE`, `DELETE`
- Handling NULLs
- Foreign Keys and cascading deletes
- Filtering using `IS NULL`
- Creating new tables from existing data

---

## 🧪 Sample Query Output

After performing all operations, the remaining records in the `Orders` table are:

| OrderID | CustomerID | ProductID | Quantity | OrderDate  |
|---------|------------|-----------|----------|------------|
| 1002    | 2          | 102       | 1        | 2024-06-25 |
| 1003    | 3          | 103       | 2        | 2024-06-01 |

---

## ▶️ How to Run

1. Visit [https://www.db-fiddle.com/](https://www.db-fiddle.com/)
2. Select **MySQL 8.0**
3. Copy the code from `task2_final_working.sql`
4. Paste it into the left panel
5. Click **Build Schema** → then **Run**
6. Scroll to the bottom to view the results

---

## 📁 Files Included
- `task2_final_working.sql` – Full SQL script for Task 2
- `README.md` – You’re reading it 😉

---

## ✅ Prepared By:
**Rahil Dudekula**  
With help from ChatGPT 😉  
