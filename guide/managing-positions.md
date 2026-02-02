# Managing Positions

This guide explains how to properly track opening and closing positions in your crypto cash flow portfolio.

---

## Opening a New Position

When you open a new position, you need to update **2 sheets**:

### 1. Holdings Sheet
Add a new row with:

| Field | Description | Example |
|-------|-------------|---------|
| id | Unique identifier (lowercase, hyphenated) | `yousd-base` |
| name | Display name | `yoUSD` |
| category | Position category | `PENDLE` |
| network | Blockchain network | `Base` |
| date_acquired | Date you opened the position (MM/DD/YYYY) | `11/17/2025` |
| cost_basis | Amount deposited (number only) | `2500` |
| current_value | Current value (update periodically) | `2500` |
| last_checked_date | When you last updated current_value | `2-2-2026` |
| status | Position status | `open` |
| notes | Any relevant notes | `Expires 3-25-2026` |

### 2. Transactions Sheet
Add a **Deposit** entry:

| Field | Value |
|-------|-------|
| date | Date of deposit (MM/DD/YYYY) |
| amount | Negative number (money going out) e.g. `-2500` |
| type | `Deposit` |
| notes | Description e.g. `Deposit for yoUSD position on Base` |

---

## Closing a Position (Selling)

When you close/sell a position, you need to update **3 sheets**:

### 1. Holdings Sheet
Find the position row and change:
- `status`: Change from `open` to `closed`
- `current_value`: Update to final value before closing (optional)
- `last_checked_date`: Update to sale date

### 2. Sales Sheet
Add a new row with:

| Field | Description | Example |
|-------|-------------|---------|
| id | Identifier for this sale | `yousd-base-sale-1` |
| date | Date of sale (MM/DD/YYYY) | `2/2/2026` |
| cost_basis | Original cost basis | `2500` |
| sale_price | Amount received from sale | `2600` |
| notes | Any relevant notes | `Closed yoUSD position, earned $100` |

### 3. Transactions Sheet
Add a **Withdrawal** entry:

| Field | Value |
|-------|-------|
| date | Date of sale (MM/DD/YYYY) |
| amount | Positive number (money coming in) e.g. `2600` |
| type | `Withdrawal` |
| notes | Description e.g. `Closed yoUSD position on Base` |

---

## Why All Three Updates Matter

- **Holdings**: Tracks what you hold/held and maintains historical record
- **Sales**: Calculates realized gains (sale_price - cost_basis)
- **Transactions**: Powers IRR calculation (tracks all cash flowing in and out)

If you skip the Withdrawal transaction, your IRR will be incorrect because it won't know money came back to you.

---

## Quick Checklist

### Opening Position
- [ ] Add row to Holdings (status: `open`)
- [ ] Add Deposit to Transactions (negative amount)

### Closing Position
- [ ] Update Holdings row (status: `closed`)
- [ ] Add row to Sales
- [ ] Add Withdrawal to Transactions (positive amount)
