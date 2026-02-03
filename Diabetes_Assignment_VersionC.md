# Week 3 Assignment: Pima Indians Diabetes Dataset Analysis

## I 320D: Data Science for Biomedical Informatics | Spring 2026

### 📋 Assignment Version C

---

## 🎯 This Week's Mantra

> **"Every Column Tells a Story"**

In this assignment, you'll apply the 10-Point Data Inspection to a real-world healthcare dataset focused on diabetes prediction. By the end, you'll understand not just *what* the data contains, but *why* each variable matters for clinical decision-making.

---

## Learning Objectives

By completing this assignment, you will be able to:

1. ✅ Apply the systematic 10-Point Inspection to a new healthcare dataset
2. ✅ Identify and classify feature types (continuous, discrete, categorical, ordinal)
3. ✅ Detect and document data quality issues (missing values, zero-encoded values)
4. ✅ Research and document clinical meaning for healthcare variables
5. ✅ Create meaningful data groupings based on clinical standards
6. ✅ Formulate answerable research questions about diabetes risk factors

---

## About the Dataset

**Dataset:** Pima Indians Diabetes Database  
**Source:** Originally from the National Institute of Diabetes and Digestive and Kidney Diseases  
**File:** `diabetes.csv`  
**Target Variable:** `Outcome` (whether the patient has diabetes: 1 = Yes, 0 = No)

### Clinical Context

Diabetes affects over 37 million Americans and is the 8th leading cause of death in the United States. Type 2 diabetes, which accounts for 90-95% of all diabetes cases, can often be prevented or delayed with lifestyle changes when risk factors are identified early.

This dataset contains diagnostic measurements from female patients of Pima Indian heritage, all at least 21 years old. The Pima Indians have one of the highest rates of diabetes in the world, making this population particularly important for understanding diabetes risk factors. Understanding these variables is crucial for:

- Early identification of high-risk patients
- Preventive care planning
- Resource allocation in healthcare settings
- Clinical decision support systems

---

## Getting Started

First, load the dataset and import your libraries:

```python
# Import libraries


# Load the dataset


# Display first few rows to confirm it loaded

```

---

## Part 1: The 10-Point Data Inspection (40 points)

Complete each inspection step and document your findings.

### Step 1: Shape (4 points)

**Your Code:**
```python

```

**Your Findings:**
- How many rows (observations)? _______________
- How many columns (features)? _______________
- What does each row represent in clinical terms? _______________

---

### Step 2: Column Names (4 points)

**Your Code:**
```python

```

**Your Findings:**
- List all column names:

- Which columns might need further research to understand?

---

### Step 3: Data Types (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns are numeric?

- Which columns are categorical (object/string)?

- Are there any data types that seem incorrect?

---

### Step 4: First Look (4 points)

**Your Code:**
```python

```

**Your Findings:**
- What do the actual values look like?

- Do you notice anything unusual or unexpected?

- Are there any values that look like they might be placeholders for missing data?

---

### Step 5: Last Look (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Does the data end cleanly?

- Are the last rows consistent with the first rows?

---

### Step 6: Memory Usage (4 points)

**Your Code:**
```python

```

**Your Findings:**
- How much memory does the dataset use? _______________ KB
- Is this a "small" or "large" dataset by data science standards?

---

### Step 7: Missing Values (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns have missing values (according to `.isnull()`)?

- What percentage of each column is missing?

- ⚠️ **IMPORTANT:** This dataset uses **zeros to encode missing values** for certain physiological measurements. Which columns have zeros that are biologically impossible? (Hint: Can a living person have a blood pressure of 0? A BMI of 0? Glucose of 0?)

---

### Step 8: Duplicates (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Are there any duplicate rows? _______________
- If there are duplicates, how many? _______________

---

### Step 9: Basic Statistics (4 points)

**Your Code:**
```python

```

**Your Findings:**
- What is the age range in the dataset? _______________ to _______________
- What is the range of glucose levels? _______________ to _______________
- What is the range of BMI values? _______________ to _______________
- Do any min values of 0 represent biologically impossible measurements?

---

### Step 10: Unique Counts (4 points)

**Your Code:**
```python

```

**Your Findings:**
- Which columns have very few unique values (likely categorical or binary)?

- Which columns have many unique values (likely continuous)?

- What does the `Outcome` column represent and how many unique values does it have?

---

## Part 2: Data Dictionary (20 points)

Complete the following data dictionary. For each column, you must:
1. **Research** the clinical meaning
2. **Identify** the feature type (Continuous, Discrete, Categorical-Nominal, Categorical-Ordinal, Binary, Identifier)
3. **Document** the valid values/range you observe
4. **Note** any issues or questions

| Column | Description | Feature Type | Valid Values/Range | Notes/Issues |
|--------|-------------|--------------|-------------------|--------------|
| `Pregnancies` | | | | |
| `Glucose` | | | | |
| `BloodPressure` | | | | |
| `SkinThickness` | | | | |
| `Insulin` | | | | |
| `BMI` | | | | |
| `DiabetesPedigreeFunction` | | | | |
| `Age` | | | | |
| `Outcome` | | | | |

### Clinical Research Questions for Version C

Answer these questions based on your research (you may need to use Google):

**1. What is the Oral Glucose Tolerance Test (OGTT)? How is it administered and what do the glucose values in this dataset likely represent?**

Your answer:

---

**2. What are the American Diabetes Association's diagnostic criteria for diabetes based on glucose levels? Include thresholds for normal, pre-diabetes, and diabetes.**

Your answer:

---

**3. What is diastolic blood pressure (which is what's measured in this dataset)? How does hypertension relate to diabetes risk?**

Your answer:

---

**4. What is the "metabolic syndrome" and how do the variables in this dataset relate to its diagnostic criteria?**

Your answer:

---

## Part 3: Data Validation (15 points)

### 3.1 Zero-Value Analysis (5 points)

A unique challenge in this dataset is that **zeros are used to encode missing values** for several columns where zero is biologically impossible.

Write code to count how many zeros exist in each column:

**Your Code:**
```python

```

**Your Findings:**

- Which columns have zeros that are biologically impossible?

- For each problematic column, what percentage of values are zeros?

- Why would the original data collectors use zeros instead of leaving these as empty/null values?

---

### 3.2 Glucose Validation (5 points)

Write code to examine glucose values. Check for zeros and understand the distribution.

**Your Code:**
```python

```

**Your Findings:**

- How many patients have a glucose value of 0?

- What is the valid glucose range in this dataset (excluding zeros)?

- Based on the maximum glucose value, do all values seem clinically plausible for a 2-hour OGTT?

---

### 3.3 SkinThickness Validation (5 points)

Write code to examine skin thickness values and identify problematic entries.

**Your Code:**
```python

```

**Your Findings:**

- How many patients have a skin thickness value of 0?

- What is a typical range for triceps skinfold thickness in adults? (Research this)

- Are there any non-zero values that seem clinically unlikely?

---

## Part 4: Create Clinical Glucose Groups (10 points)

Create a new column called `glucose_category` that categorizes patients into clinically-meaningful groups.

### Version C: Glycemic Status Categories

Use these categories based on the American Diabetes Association diagnostic criteria for the 2-hour Oral Glucose Tolerance Test:

| Glucose Category | Range (mg/dL) | Clinical Rationale |
|------------------|---------------|-------------------|
| Normal | < 140 | Normal glucose tolerance |
| Pre-diabetes | 140-199 | Impaired glucose tolerance, high risk for developing diabetes |
| Diabetic Range | 200+ | Meets diagnostic criteria for diabetes |

**⚠️ Important:** You must handle Glucose values of 0 (missing data) before creating categories. Either exclude them or create a separate "Missing" category.

### Your Code:

```python
# First, handle the zero Glucose values
# Then create the glucose_category column
# You can use a custom function with .apply() OR pd.cut()


```

### Verify your groupings worked:

```python
# Show counts per glucose category

```

### Calculate diabetes rate by glucose category:

```python
# Calculate the percentage of patients who have diabetes (Outcome=1) in each glucose category
# Exclude patients with missing glucose from this analysis

```

### Analysis Questions:

**1. How many patients are in each glucose category (excluding missing)?**

Your answer:

---

**2. What is the diabetes rate (percentage with Outcome=1) for each glucose category?**

Your answer:

---

**3. You might notice something surprising: some patients with glucose in the "Diabetic Range" (≥200) have Outcome=0 (no diabetes), and some with "Normal" glucose have Outcome=1 (diabetes). What might explain these apparent contradictions?**

Your answer:

---

## Part 5: Research Questions (15 points)

### 5.1 Write Three Answerable Questions (9 points)

Write three questions that THIS dataset can answer. Remember: the data can show relationships and patterns, but cannot prove causation.

**Your questions must explore these specific areas:**

1. **A question about glucose levels and diabetes outcome:**


---

2. **A question comparing patients by blood pressure levels:**


---

3. **A question about the combination of insulin AND BMI:**


---

### 5.2 Identify One Question the Data CANNOT Answer (3 points)

Write one question about **HbA1c (glycated hemoglobin) or long-term glucose control** that this dataset cannot answer, and explain why.

**Question:**


**Why it cannot be answered with this data:**


---

### 5.3 Grouping Analysis (3 points)

Answer this question using a groupby analysis:

**"What is the average BMI for patients with diabetes (Outcome=1) versus without diabetes (Outcome=0)?"**

(Note: You should exclude zero BMI values before calculating!)

**Your Code:**
```python

```

**Your Interpretation:**

What is the difference in average BMI between diabetic and non-diabetic patients? Is this difference clinically meaningful?


---

## Part 6: Target Variable Analysis (Bonus - 5 points)

The `Outcome` column is our **target variable** - what we're trying to predict. Analyze its distribution.

**Your Code:**
```python
# Show the count and percentage of diabetic vs non-diabetic patients

```

### Bonus Questions:

**1. What percentage of patients in this dataset have diabetes?**

Your answer:

---

**2. Is this dataset balanced or imbalanced? (A balanced dataset has roughly equal classes)**

Your answer:

---

**3. Why does class imbalance matter for machine learning? (You may need to research this)**

Your answer:

---

**4. The Pima Indians have one of the highest rates of diabetes in the world (around 50% in some studies). How does this dataset's diabetes rate compare? What might this tell you about the patient selection criteria?**

Your answer:

---

## Submission Checklist

Before submitting, verify you have completed:

- [ ] **Part 1:** All 10 inspection steps with code AND written findings
- [ ] **Part 2:** Complete data dictionary with all 9 columns filled in
- [ ] **Part 2:** Answered all 4 clinical research questions
- [ ] **Part 3:** All 3 validation checks with code and answers
- [ ] **Part 4:** Created `glucose_category` column using the **Glycemic Status Categories**
- [ ] **Part 4:** Calculated diabetes rate by glucose category with interpretation
- [ ] **Part 5:** Three research questions (glucose, blood pressure, insulin+BMI)
- [ ] **Part 5:** One unanswerable question about HbA1c/long-term glucose control
- [ ] **Part 5:** BMI by outcome groupby analysis
- [ ] **Bonus (Optional):** Target variable analysis

---

## Grading Rubric

| Component | Points | Requirements for Full Credit |
|-----------|--------|------------------------------|
| Part 1: 10-Point Inspection | 40 | All 10 steps complete with working code AND thoughtful written analysis |
| Part 2: Data Dictionary | 20 | All 9 columns documented with correct feature types and clinical research |
| Part 3: Data Validation | 15 | All validation checks complete with working code and insightful answers |
| Part 4: Glucose Categories | 10 | Working code that creates correct groups, handles missing data, AND meaningful interpretation |
| Part 5: Research Questions | 15 | Three good questions in specified areas, one clear limitation, groupby analysis complete |
| **Bonus:** Target Analysis | +5 | Thoughtful analysis of class imbalance with real-world connection |
| **Total** | 100 (+5 bonus) | |

---

## Hints (Read Before You Get Stuck!)

### ⚠️ Common Pitfalls:

1. **Zeros as Missing Values**
   - Unlike most datasets, this one uses **0** to represent missing values for columns like `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI`
   - The `.isnull()` method won't detect these!
   - You need to check for zeros manually in columns where 0 is biologically impossible

2. **Glucose of 0 will break your categories** - you MUST handle these before using `pd.cut()` or your analysis will be incorrect

3. **The glucose measurement is from a 2-hour OGTT** - not a fasting glucose test. The thresholds are different!

4. **Outcome vs. Glucose Category mismatch** - Don't be surprised if they don't perfectly align. Think about why this might be.

### 💡 Pro Tips:

- Use `value_counts()` liberally to understand distributions
- Use `df[df['ColumnName'] == 0].shape[0]` to count zeros in a column
- When creating glucose categories, consider using `df[df['Glucose'] > 0]` to filter first
- Use `pd.cut()` with appropriate bin edges: `[0, 140, 200, float('inf')]`
- The `describe()` function is your friend - look at those min values!

---

## Useful Resources

- **Original Dataset Source:** UCI Machine Learning Repository
- **Diabetes Diagnostic Criteria:** https://www.diabetes.org/a1c/diagnosis
- **Oral Glucose Tolerance Test:** https://www.mayoclinic.org/tests-procedures/glucose-tolerance-test/about/pac-20394296
- **Metabolic Syndrome:** https://www.heart.org/en/health-topics/metabolic-syndrome/about-metabolic-syndrome
- **Pandas Documentation:** https://pandas.pydata.org/docs/

---

*Remember: "Every Column Tells a Story" - your job is to figure out what that story is!*

---

**Due Date:** [See Canvas]

**Submission:** Upload your completed Jupyter notebook (.ipynb) to Canvas
