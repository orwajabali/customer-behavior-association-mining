# 🏦 Customer Behavior Mining — Association Rule Discovery

Applying **Apriori** and **FP-Growth** algorithms on real bank customer data to uncover hidden purchasing patterns and generate actionable marketing recommendations.

---

## 🎯 What This Project Does

> *"What customer profiles are most likely to respond to a new financial product — and what drives that behavior?"*

Mines transactional-style customer records to discover high-confidence rules linking demographics, account types, and product adoption — insights directly usable in targeted marketing campaigns.

---

## 🔬 Approach

**1. Data Preprocessing**
- Removed non-informative identifiers
- Discretized continuous variables (`age` → Child/Young/Adult/Senior, `income` → Low/Medium/High)
- Mapped binary flags to human-readable labels for interpretable rules
- One-hot encoded all features via `TransactionEncoder`

**2. Algorithm Comparison — Apriori vs. FP-Growth**
- Ran both algorithms with `min_support=0.25`, `min_confidence=0.6`
- Generated 80–100 strong rules per algorithm
- Ranked by support, confidence, and lift
- Visualized top-10 popular items (bar plots) and rule distributions (support vs. confidence scatter plots)

**3. Business Insight Extraction**
- Selected top 5 most *actionable* rules per algorithm
- Each rule translated into a concrete marketing recommendation

---

## 💡 Sample Insight

> **Rule:** *Adult + Savings Account + Married → PEP Buyer* (high lift)
>
> **Recommendation:** Prioritize direct mail to married adults with existing savings accounts — they show the highest propensity to adopt new financial products like PEPs.

---

## 🛠️ Tech Stack

`Python` · `pandas` · `mlxtend` · `Matplotlib` · `Seaborn`

---

## 📁 Key Files

| File | Description |
|---|---|
| `association_rule_data-mining.ipynb` | Full analysis — preprocessing, Apriori, FP-Growth, insights |
| `bank-data.csv` | Customer records with demographics and account info |

---

## 📊 Scale

| Metric | Value |
|---|---|
| Dataset | Bank customer records · demographic + account features |
| Algorithms | Apriori · FP-Growth |
| Rules generated | 80–100 strong rules per algorithm |
| Evaluation metrics | Support · Confidence · Lift |
