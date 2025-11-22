
# 🛒 Online Retail Market – Data Engineering & Analysis Project

## 📌 Project Overview
This project focuses on performing **EDA (Exploratory Data Analysis)** and **ETL (Extract–Transform–Load)** on the *Online Retail* dataset.  
Το repository είναι οργανωμένο ώστε να συνεργάζονται 3 developers σε διαφορετικά branches.

---


### 🔧 Branch Roles
- **main** → Production-ready code
- **dev** → Integration branch για όλα τα features
- **Extract** → Data extraction & loading from CSV
- **Transform** → Data cleaning & transformation
- **Reports** → Visualizations, EDA, insights

### 🚀 Workflow
1. Κάθε developer δουλεύει στο αντίστοιχο branch.
2. Όταν ολοκληρωθεί μια ενότητα → **Pull Request → dev**
3. Από το `dev` → μετά από review → **merge στο main**

---

## 🔍 Dataset

**Online Retail CSV**

- Retail transactional data
- Περιέχει:
  - Invoice information
  - Customer IDs
  - Product descriptions
  - Quantities & prices
  - Country-based purchasing behavior

---

## 🧪 EDA Tasks
- Checking missing values  
- Checking duplicates  
- Statistical summaries  
- Visualizations (histograms, boxplots, correlations)  
- Customer & product segmentation insights  

---

## 🔧 ETL Pipeline

### 1️⃣ Extract  
- Load CSV  
- Handle encoding issues (`latin1`, `cp1252`)  
- Basic type validation  

### 2️⃣ Transform  
- Remove duplicates  
- Clean missing values  
- Convert data types  
- Create new calculated features  
- Filtering invalid entries  

### 3️⃣ Reports  
- Create histograms, correlation heatmap and pie chart (Descriptive Statistics & Visualization)

---

# 📊 Summary of Insights from EDA

## 🔹 1. Revenue Distribution
- Η κατανομή του **Revenue** είναι έντονα **right-skewed**.
- Οι περισσότερες συναλλαγές έχουν revenue κάτω από **50£**.
- Υπάρχουν αρκετά μεγάλα **outliers** (άνω των 1000£), που αυξάνουν σημαντικά τη μέση τιμή.
- Λίγες παραγγελίες δημιουργούν το μεγαλύτερο ποσοστό του συνολικού εσόδου.

**💡 Business Insight:** Η επιχείρηση εξαρτάται έντονα από high-value orders. Αξίζει στρατηγική στόχευση σε αυτούς τους πελάτες.

---

## 🔹 2. Quantity Distribution
- Οι περισσότερες παραγγελίες περιλαμβάνουν **1–10 τεμάχια**.
- Υπάρχουν **σημαντικά outliers** (ποσότητες έως και >100), πιθανώς από:
  - χονδρικές παραγγελίες,
  - λάθη εισαγωγής (data entry errors),
  - bulk stock replenishment.

**💡 Data Insight:** Πριν από predictive models απαιτείται χειρισμός ή φιλτράρισμα των outliers.

---

## 🔹 3. Unit Price Distribution
- Η τιμή μονάδας είναι επίσης **right-skewed**.
- Η πλειοψηφία των προϊόντων κοστίζει **0.5£–4£**.
- Outliers εμφανίζονται με τιμές έως και **15£** ή περισσότερο.

**💡 Business Insight:** Το κατάστημα πουλά κυρίως χαμηλού κόστους προϊόντα, με λίγα premium items που αυξάνουν τη μέση τιμή.

---

## 🔹 4. Correlation Analysis
- Η **Quantity** και η **UnitPrice** έχουν αρνητική συσχέτιση (~ -0.25).
  - Όσο αυξάνεται η ποσότητα, τείνει να πέφτει η τιμή (λογικό σε wholesale orders).
- Η συσχέτιση μεταξύ **CustomerID** και άλλων μεταβλητών είναι σχεδόν μηδενική (τυπικό).

**💡 Insight:** Δεν υπάρχει έντονη γραμμική σχέση ανάμεσα σε τιμή και ποσότητα, αλλά υπάρχουν patterns που εξηγούνται από wholesale vs retail orders.

---

## 🔹 5. Top 10 Products
- Τα προϊόντα με τις περισσότερες πωλήσεις είναι διακοσμητικά και μικροαντικείμενα χαμηλού κόστους.
- Το **WHITE HANGING HEART T-LIGHT HOLDER** έχει το μεγαλύτερο ποσοστό πωλήσεων.
- Τα περισσότερα top-selling προϊόντα είναι:
  - χαμηλής τιμής,
  - υψηλής ζήτησης,
  - μικρού physical size (εύκολα στη μεταφορά & αποθήκευση).

**💡 Business Insight:** Το e-shop στηρίζεται σε low-cost, high-volume προϊόντα → ιδανικό για cross-selling & bundling.

---

## 📌 Overall Conclusion
Η επιχείρηση παρουσιάζει:
- Υψηλή συγκέντρωση revenue σε λίγους πελάτες/παραγγελίες,
- Bulk orders που δημιουργούν outliers σε quantity και revenue,
- Κυριαρχία χαμηλού κόστους προϊόντων,
- Αδύναμες γραμμικές συσχετίσεις μεταξύ των βασικών μεταβλητών.

Αυτό σημαίνει ότι το κατάστημα λειτουργεί κυρίως ως low-cost gift/home decor retailer, με occasional wholesale orders που «φουσκώνουν» τα έσοδα.



👥 Contributors

Developer 1, 2, 3 – Extract Pipeline

Developer 1 – Transform Pipeline

Developer 2, 3 – Reports & EDA


