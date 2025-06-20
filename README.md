# 🧾 Monthly-Bill-Generator
This project is a Monthly Bill Generator built in Python for a workspace rental company. It takes a list of rented items (with start and end dates, rate, and quantity) and calculates a prorated monthly invoice based on usage during a given month. It groups similar items, calculates partial usage accurately, and returns the final monthly bill.

This repository contains a solution to the Python Developer assignment given by **Novel Office**. The task focuses on generating a **monthly invoice** for rented items (furniture or space resources), accurately calculating the **prorated cost** for each item depending on usage duration within a given month.

---

## 📌 Problem Statement

A company rents out furniture and space resources with specific `start_date` and `stop_date` for each item. Each item has a rate and quantity. Some items are used for partial months or overlap across different months.

We need to **generate a monthly invoice** that:
- Includes only items active during the **target month**
- **Prorates** the cost for partial-month usage
- Groups similar items (by `item_code`, `rate`, and `billing period`)
- Returns a total bill for the month.

---

## 🧾 Input Format

### 1. `item_list`: *List of Dictionaries*
Each dictionary represents a billing item with keys like:
- `item_code`
- `rate`
- `qty`
- `start_date`
- `stop_date`

### 2. `target_month`: *String*
```python
"2024-11"  # Format: "YYYY-MM"

