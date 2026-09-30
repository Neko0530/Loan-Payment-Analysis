# Loan Payment Analysis Dashboard

A Power BI dashboard analyzing a loan portfolio, built around the questions a lending or risk team asks daily: how many loans are outstanding, how many have been paid off, and how repayment behavior varies across borrower demographics.

---

## Dataset

| Category | Fields |
|---|---|
| Loan identifier | `Loan_ID` |
| Loan outcome | `loan_status` (paid off vs. outstanding/other) |
| Loan amount | Principal |
| Borrower demographics | Age, `Gender`, `education` |

All fields come from a single table: **Loan payments data**.

---

## Report Pages

### Page 1 — Summary

A clean overview built around five KPI cards.

**KPI Cards**
| Metric | What it shows |
|---|---|
| Total Loans | Overall loan count |
| Paid Off Loans | Count of loans fully repaid |
| Paid Off Rate | Percentage of loans paid off |
| Average Age | Mean borrower age |
| Total Principal | Sum of loan principal across the portfolio |

**Visuals**
| Visual | Breakdown | Purpose |
|---|---|---|
| Clustered column chart | Loan count by `loan_status` | Immediate read on how the portfolio splits between paid-off and outstanding loans |

### Page 2 — Loan Payment Analysis (Detailed View)

The report's default landing page, titled **"LOAN PAYMENT ANALYSIS."** Repeats the five headline KPI cards from Page 1, then breaks the portfolio down further by demographics.

**Visuals**
| Visual | Breakdown | Purpose |
|---|---|---|
| Clustered bar chart | Loan count by `education` | Shows which education segments carry the most loans |
| Donut chart | Loan count by `Gender` | Shows the portfolio's gender split |
| Column chart | Loan count by `loan_status` | Same status breakdown as Page 1, kept here for reference |

**Filters**
Three slicers — **Gender**, **loan_status**, and **education** — filter the page interactively. For example, selecting "paid off" and "bachelor's degree" updates every visual and KPI card to reflect just that segment.

---

## Tools & Format

Built in Power BI Desktop using the PBIR (Power BI Enhanced Report) project format, which stores each page and visual as its own readable JSON file rather than a single packed binary. This keeps the report easier to version-control alongside the rest of a portfolio project.

**To open:** load the `.pbix` file directly in Power BI Desktop.
