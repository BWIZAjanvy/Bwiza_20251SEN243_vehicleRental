# Project Proposal: Enterprise Vehicle Rental and Fleet Management System

## 1. Title
Enterprise Vehicle Rental and Fleet Management System

## 2. Problem Statement
Traditional vehicle rental operations often rely on manual record-keeping or fragmented spreadsheets to track vehicle availability, customer bookings, and rental durations. This leads to double-bookings, delayed returns, inaccurate late-fee calculations, and difficulties in auditing daily transactions. A centralized, robust database system is needed to automate inventory updates, ensure data integrity, and streamline the rental lifecycle.

## 3. Proposed Solution
An Oracle-backed relational database application that manages vehicle inventory (cars/bikes), customer records, and booking transactions. The system will leverage PL/SQL packages, stored procedures, and triggers to automatically calculate rental fees, apply late penalties, and update vehicle statuses (available vs. rented) in real time.

## 4. Data Source
* **Dataset Name:** Car Rental / Vehicle Fleet Dataset (sourced from Kaggle or open data repositories).
* **Description:** Contains historical records of vehicle types, mileage, daily rates, customer demographics (anonymized), and rental transaction logs (spanning several hundred records).
* **License:** Open educational use license.

## 5. Planned Tables (3NF Schema)
1. **CUSTOMERS:** Stores customer ID, name, contact details, and driver’s license info.
2. **VEHICLES:** Stores vehicle ID, make, model, registration number, category (car/bike), daily rate, and status.
3. **RENTALS:** Stores booking ID, customer ID, vehicle ID, rental start date, expected return date, and actual return date.
4. **PAYMENTS / INVOICES:** Stores payment ID, rental ID, total amount calculated, late penalties, and payment status.

## 6. Planned PL/SQL Features
* **Procedures & Functions:** A function to calculate total rental charges based on duration and vehicle category; a procedure to process vehicle check-outs and check-ins.
* **Triggers:** An automated trigger on the `RENTALS` table that instantly updates a vehicle's status to 'RENTED' upon booking insertion, and back to 'AVAILABLE' upon return.
* **Cursors:** Cursor-based loops to generate monthly summary reports of total revenue and rental counts per vehicle category.
* **Exception Handling:** Custom exceptions to catch negative rental durations or attempts to rent an already-booked vehicle.

## 7. Innovation Plan
* **Option Chosen:** Analytics Dashboard / User Interface.
* **Tool:** Python Streamlit app or Power BI connected directly to the Oracle database to display live fleet availability metrics, total active rentals, and revenue trends.

## 8. References
* Oracle Corporation. (2021). *Oracle Database PL/SQL Language Reference*. Oracle Docs.
* Kaggle. (2025). *Vehicle Rental Operations Dataset*. Retrieved from https://www.kaggle.com
