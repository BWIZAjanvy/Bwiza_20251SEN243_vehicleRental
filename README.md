# Enterprise Vehicle Rental and Fleet Management System

* **Student Name:** Bwiza Janviere[cite: 2]
* **Student ID:** 20251SEN243[cite: 2]
* **Course:** INSY 8311 & Database Development with PL/SQL (Semester I, 2026-2027)[cite: 1]
* **Instructor:** Eric Maniraguha[cite: 1]

## Problem Statement
Traditional vehicle rental operations often rely on manual record-keeping or fragmented spreadsheets to track vehicle availability, customer bookings, and rental durations. This leads to double-bookings, delayed returns, inaccurate late-fee calculations, and difficulties in auditing daily transactions. A centralized, robust database system is needed to automate inventory updates, ensure data integrity, and streamline the rental lifecycle.

## Objectives
* **Main Objective:** Design and deploy a fully normalized (3NF) Oracle relational database backed by modular PL/SQL packages, procedures, triggers, and auditing mechanisms to manage a vehicle rental business.
* **Specific Objective 1:** Implement automated status triggers that update vehicle availability instantly upon checkout and return.
* **Specific Objective 2:** Develop PL/SQL functions and cursors to calculate rental fees and late penalties dynamically.
* **Specific Objective 3:** Integrate an interactive analytics dashboard as an innovation layer to monitor fleet utilization.

## Data Source
* **Dataset:** Car Rental Data (Kaggle)[cite: 13]
* **Link:** [Kaggle Car Rental Dataset](https://www.kaggle.com/datasets/yuremartins/car-rental-data)[cite: 13]

## Planned Innovation
* **Tool:** Power BI / Python Streamlit
* **Description:** An interactive dashboard connected directly to the Oracle database to visualize live vehicle availability, active rentals, and revenue trends.

## Planned Tables
1. `CUSTOMERS`: Stores client contact information and license details.
2. `VEHICLES`: Tracks car/bike inventory, category, daily rates, and status.
3. `RENTALS`: Records booking dates, duration, and associated customer/vehicle IDs.
4. `PAYMENTS`: Handles billing, calculations, and late penalties.

## Planned PL/SQL Features
* Stored procedures for transaction check-ins/check-outs.
* Triggers for real-time inventory status switching.
* Cursors for generating batch financial reports.
* Exception handling for invalid dates and duplicate bookings.
