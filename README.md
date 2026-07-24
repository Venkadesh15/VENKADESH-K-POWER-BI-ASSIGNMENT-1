# POWER BI ASSIGNMENT 1

## DATA TRANSFORMATION & DATA MODELING

**Date of Submission:** 24/07/2026 – 08:00 AM

---

## PREVIEW SCREENSHOTS: QUESTIONS

## 1) IMPORT DATA

### 1.1) Import `List of Orders.csv` into Power BI

* **1.1.1)** Open **List of Orders** in Power Query Editor by clicking **Transform Data**.
* **1.1.2)** Use **First Row as Headers** in the **List of Orders** table.

### 1.2) Import `Order Details.csv` into Power Query Editor

* **1.2.1)** Open **Order Details.csv** in Power Query Editor by clicking **Transform Data**.

### 1.3) Import `Sales Target.csv` into Power Query Editor

* **1.3.1)** Open **Sales Target.csv** in Power Query Editor by clicking **Transform Data**.

---

## 2) DATA TRANSFORMATION

### 2.1) Data Transformation in `List of Orders`

* **2.1.1)** Keep only the **first 500 rows** of the **List of Orders** table.

* **2.1.2)** Change the data type of the **Order Date** column to **Date**.

* **2.1.3)** Verify the changed **Date** format of the **Order Date** column.

* **2.1.4)** Change the **Amount** and **Target** columns to **Fixed Decimal Number**.

* **2.1.5)** Convert the **CustomerName** column to **Proper Case**, ensuring consistent capitalization for each word.

  **Preview:** Proper Case of **Customer Name**

* **2.1.6)** Merge the **State** and **City** columns to create a new column named **Location**.

  **Preview:** Merged column as **Location**

* **2.1.7)** Create a new **Custom Column** named **Profit Margin** by calculating Profit as a percentage of Amount.

```text
Profit Margin = [Profit] / [Amount]
```

Change the data type of the **Profit Margin** column to **Fixed Decimal Number**.

* **2.1.8)** Create a new **Conditional Column** named **Profit Status**.

```text
if [Profit] < 0 then "Loss"
else if [Profit] = 0 then "Break-Even"
else if [Profit] > 0 then "Profit"
```

Change the data type of the **Profit Status** column to **Text**.

---

## 3) MERGING DATA (JOINS)

### 3.1) Merge Tables

Merge the **List of Orders** and **Order Details** tables into a new single table named **Orders Data**, based on the **Order ID** relationship using a **Left Outer Join**.

**Preview:** View the **Orders Data** table.

---

## 4) HANDLING MISSING DATA & DUPLICATE DATA

### 4.1) Check for Duplicate Values

Check and apply **Remove Duplicates** where required in each table.

**Result:** No duplicate values found.

---

## 5) SORTING AND FILTERING DATA

### 5.1) Sorting and Filtering the `Orders Data` Table

Perform sorting and filtering using the **Order Date**, **State**, **Location**, and **Category** columns.

* **5.1.1)** Sort the **Order Date** column.
* **5.1.2)** Filter **Location** for **Tamil Nadu**.

---

## 6) GROUPING AND AGGREGATING DATA

### 6.1) Duplicate `Order Details`

* **6.1.1)** Create a duplicate of the **Order Details** table and name it **Order Details (2)**.

* **6.1.2)** Calculate the **Count of each Order ID**.

  **Preview:** Count of **Order ID**

* **6.1.3)** Calculate the **Average Profit by Category**.

  **Preview:** Average Profit by **Category**

### 6.2) Duplicate `Sales Target`

* **6.2.1)** Create a duplicate of the **Sales Target** table and name it **Sales Target (2)**.
* **6.2.2)** Calculate the **Total Target Amount by Month of Order Date**.

  **Preview:** Total Target Amount

---

## 7) DATA MODELING

### 7.1) Relationship between `List of Orders` and `Order Details`

Create a relationship between the **List of Orders** and **Order Details** tables using **Order ID**.

### 7.2) Relationship between `Order Details` and `Orders Data`

Create a relationship between the **Order Details** and **Orders Data** tables using **Order ID**.

#### 7.2.1) Change an Inactive Relationship to Active

**Step 1:** Click **Manage Relationships**.

**Step 2:** Check whether any required relationship is **Inactive**.

**Step 3:** Change the required relationship from **Inactive** to **Active**.

### 7.3) Relationship between `Order Details` and `Sales Target`

Create the required data model relationship between the **Order Details** and **Sales Target** tables.

---

## 8) VERIFICATION VIA CHARTS

Create appropriate charts in Power BI to verify the transformed, aggregated, and modeled data.

---

## END OF ASSIGNMENT

**POWER BI ASSIGNMENT 1**
**DATA TRANSFORMATION & DATA MODELING**

**Prepared by:** Venkadesh K
