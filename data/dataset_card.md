# Dataset Card — Enterprise Vehicle Rental & Fleet Dataset

## Overview
* **Source Link:** Synthetic dataset generated for INSY 8311 capstone modeling (`data/raw/vehicle_rentals_raw.csv`)
* **Licence:** Academic coursework / synthetic sample dataset (no restricted third-party redistribution terms)
* **Format:** CSV (UTF-8, comma-separated, 15 columns)
* **Size:** 520 records (521 lines including header)
* **Date Collected:** 2026-11-26
* **What One Record Represents:** Each row represents a single vehicle rental transaction, capturing anonymised customer info, vehicle details, pickup/return dates, rental rates and totals, payment method, rental status, and requested add-ons.

## Privacy & Raw File Rules
* Personal identifiers are anonymised using synthetic customer codes (`CUST-XXXX`) with no real names, phone numbers, IDs, or driver's license numbers included.
* The file in `data/raw/vehicle_rentals_raw.csv` is kept untouched in its raw state; no cleaning or edits are applied here (data cleaning happens in Phase IV).

## Data Quality Audit (Counts Only)
* **Exact duplicate rows:** 8 rows
* **Missing `actual_return_date` values:** 18 blank entries
* **Blank `add_ons` entries:** 86 blank entries
* **Non-ISO `pickup_date` values (`DD/MM/YYYY` instead of `YYYY-MM-DD`):** 15 rows
* **Prices stored as text / currency strings in `daily_rate`:** 45 rows (e.g., `$55/day`, `85 USD`)
* **Prices stored as text / currency strings in `total_amount`:** 22 rows (e.g., `$220.00`)
* **Non-standard `pickup_district` spelling/casing variants:** 29 rows (e.g., `kigali city`, `KGL`, `Kicukiro Dist.`, `Nyarugenge Dist`)
* **Non-standard `vehicle_category` spelling/casing variants:** 23 rows (e.g., `suv`, `S.U.V.`, `Saloon`, `Hatchback`, `Four-Wheel Drive`)
