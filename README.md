# Customer-Data-Insights-Power-BI--Dashboard
In this project I have used a dataset on a customer transactions for different products which I will analyse this data and build a Power BI Dashboard.

# 📊 Power BI Project Setup and Data Transformation Guide

## 🧩 Project Initialization

1. **Open Power BI Desktop** and create a new project by selecting **“Blank Report.”**
2. **Rename** the project as you like and **save** it in a **new folder** (this keeps all files organized).
3. **Add the data files** you plan to analyze to that same folder.
4. Return to the Power BI interface and click **“Get Data from Another Source.”**
5. You can now upload any type of file (Excel, CSV, Text, JSON, etc.).
6. In this example:
   - One **Excel file** and one **Text (.txt)** file were uploaded.
   - Each file was **transformed before loading** into Power BI.
7. *(Alternative method)* — You may also load both files first and then perform transformations one by one.

---

## 🧮 Data Transformation Steps

### 🔹 1. Text Data (Invoice Data) Transformation

Perform the following steps for the text data file:

- Change the **"Sales"** column data type from **Integer** ➜ **Fixed Decimal Number** to display it as a currency.
- Merge the **Year**, **Month**, and **Day** columns:
  - Select all three columns while holding **Ctrl**.
  - Use the **Merge Columns** command.
  - Set the **Separator** to `/` and the **New Column Name** to `Date`.
- Change the data type of the new **Date** column to **Date** format.

---

### 🔹 2. Excel Data (Customer Data) Transformation

Perform the following steps for the Excel data file:

- Select the **"CityProvince"** column and **split it by a custom delimiter**:
  - Navigate to *Split Column → By Delimiter → Custom ('(')*  
  - Split at the **Left-most delimiter** and click **OK**.
  - Rename the first new column to **City** and the second to **Province**.
  - In the **Province** column, replace `'('` with an empty string (`""`).
- **Remove unnecessary columns** such as email, telephone number, address, etc.:
  - Go to **Home → Manage Columns → Choose Columns**.
  - Untick the unneeded columns and click **OK**.

---

## ✅ Finalizing Transformations

- Once both transformations are completed, click **Close & Apply**.
- Power BI will automatically **detect relationships** between tables.

---

## 🧱 Data Model Structure

In this project:

| Table Type | Table Name |
|-------------|-------------|
| Fact Table | Invoice Data |
| Lookup Table | Customer Master Data |

---

## 📈 Creating Insights and Visualizations

Use the **Visualizations** panel to create insights from both tables.  
You can insert multiple pages and mix visuals as needed.

**Recommended Visuals:**
- 📊 Chart with Slicer  
- 📋 Table with Quick Measures  
- 🗺️ Map Chart  
- 📉 Line Chart  
- 📍 KPI Chart (for dashboard insights)

---

## 🚀 Publishing the Report

1. After completing all visuals, **save your project**.
2. Click **Publish** to upload your report to the Power BI Service.
3. **Share your report** on the web or with team members via Power BI dashboard access.

---

## 🧾 Summary of Steps

| Step | Description |
|------|--------------|
| 1–3 | Project setup and data preparation |
| 4–7 | Importing data into Power BI |
| 8–10 | Data cleaning and transformation |
| 11 | Relationship setup (Fact & Lookup Tables) |
| 12 | Visualization creation |
| 13 | Publishing and sharing report |

---

### 🏁 End of Guide

> 🎯 **Tip:** Always save your Power BI file frequently and document each transformation step for reproducibility.
