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


## Phase I – Business Process Modeling

Selected Business Process

End-to-End Vehicle Rental & Fleet Lifecycle: This process models the complete workflow of the Enterprise Vehicle Rental and Fleet Management System—from initial customer rental request submission, vehicle availability and customer eligibility verification, and booking confirmation through vehicle pickup/usage, return inspection, late-fee or damage penalty assessment, final payment processing, and record archiving.

Modeling Tool Used

[diagrams.net (draw.io)](https://app.diagrams.net/)

Published Diagram Link

Interactive BPMN Swimlane Diagram:[View Published Diagram on draw.io](https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=PL.drawio.png&dark=auto#R%3Cmxfile%20scale%3D%221%22%20border%3D%220%22%3E%3Cdiagram%20name%3D%22Page-1%22%20id%3D%22pnNysA7Lv4wQS3qSd9c6%22%3E5Vxtd6I4FP41fmwPL4Ly0bdOu6fbdbXTnc6XOSlEzRaIG2LV%2FvpNIAhISimC2s6Zc2bIJSRwX5775CZOSx94m28ELBd%2FYge6LU1xNi192NI01eya7B8u2UYS0zAiwZwgR3RKBFP0CoVQEdIVcmCQ6UgxdilaZoU29n1o04wMEILX2W4z7GZnXYI5zAmmNnDz0n%2BQQxeRtGsoifwaovkinllVxB0PxJ2FIFgAB69TIn3U0gcEYxpdeZsBdLnyYr1Ez129cXf3YgT6tMwD%2BrijOI%2FrDbr%2F%2BazYo2dwAzsXklGEKKDbWAfBGnku8FmrH1BAqLASm0%2FvLzBBr9inwGWSUEA9fqmyy%2FUCUThdApv3XjP%2FYLJo8BfgrsTg9iqg2INE3ICEwk3qRcS3fIOsDyVb1mWRVrcplLtObKMasQnEOFrcFi7YFk0gXGO%2BG3s33YS5EvDnTAHZ%2Bbr56drZyazsXKq6NxlwKSQ%2BoLCPV74TpC3GLlIfmohCO8ptemHYy8HrFF75%2Ffup%2Beu5bTiPF%2B1oRujkPDsxcpEzBHhFbFgwQd5D%2BFxT0cSELvAc%2B8AdJdI%2B4Z8LHeEkSZ9bjJfCXf6FlG6Fb4EVxVlncuAMrFx6C56g2wf28zwccYBdTFiPKIz7Lr87Bo6D%2FHk4laa0mRj6To9jARPZLggCZEfCK%2BTGwwtoAWQOacGn6zn%2FlTspgS6g6CVrAJnDZYz%2FUUt%2F1LApg7kuQ1D4RpCm1M5Qawlv%2FIChsJCAYBkB7QxtuEHzIc3fBrihFv5bwYDyz%2FARRczrnUphLgm7bjbsjGzY6QUhfpDG9coaTwLgLWhMaV10HkOC2HtDknHSlKanqycPcf1OYpVPdipvaSbw%2BLjR30wyZAYIdmL%2FKRDyltEfTEa9%2B1HLGFayjwyFtayBVNMoDcJlLQRvv%2F3Zv9bu1rd33yeuNbimP%2B8vuudloe8BlNpiAumK%2BOziAS6QzRNNM3pv6%2BWTX1m9y%2FWpnZxK7HDHARQ8gaCaUlUJ2rzLKfROU4gTE4gK6Vwrmc%2BN3zefW2eVz42PWrZh8BosoP2cxiil9wIQMwpyEd3KcS3KMTynsJQybDKjHCvnWwdYZYG9p1VQhWbljJEzgivPLA%2FAZZ%2BjKYN4YaVfVcNBRWIDPWsDXd1b7jSV1SXJ5bSRQSBz9DTxyhtiCmkmdnhXToBTfIs%2FxqyjfB8Pm6Vf7U79wSI1lG7Wma7kU%2BifLV%2Flk5H8w4xTZaNCPZ9N0E2gjQkPoDHYevyVykRdBizfCryw2ZsMrm8eGl0EKWY2DI3GwvAAKlFnbSCgBD%2FvKqe63KoCQQfYW7qwuRqBqu1pv7E1qKqWAEFJta1oQfvl0E5V5EY9Dri1y%2BSpsiaSxFDzJoIbRH%2Bkrh%2FFUPx6uEk3tnHDZ5rjjyiXXT1uh49dWl0tFiTPhq344SN4RPdIDiEFQgnLP1X5gg09m1UCQbUjSULv1S527fqDrFOVDFr5yJNXRz5d6GXi7qgxJ1egeaSgKzRfaX9omGHeYYpm2%2FTiOSaKf81mYasn9u%2B4ahpiiYwW7sVnU9o3K2u%2Ffo4Ye3WLrU2H%2FE%2Fs2ixAHUji2yIk2E2mdTqN99TVclyTLRfCZ23MXkcz5%2Fw62TEZQttFPuefUS%2Bm1HTHhmipsb9l3Bgr1RtHY4mjfDauWhgp9a3Mw0d7hIBtqsMSI58GqZHHXJBylbZ0%2BXhVqTtf8Ybz13r4QJXwqFMi%2BgD7M0Q8Juxj%2FMyNLysa3ATBCrYa34zTG1iASq1wMO86Lp1K1iXGsehRyS2kkhEu7KtcKkan7qBX9%2FJDpzjoNbWoezbo353rwtzz0CgFiKc%2B8Ba5NUYEubmBKsBQQXHhfGCIMaCQ9aQrk3kYivfbdocDhuEmQzNgZHb3TGQ0xTsqbwlIeId8hpOsAo%2B%2Bgy3%2F9vPaNFBF6hHnccPCe4SNeZsXesueLUMtZ%2FUPXDT3uQL5vhpTeZ%2FHCLKB2xM3POQ4kalhgF7Fq3BjC8hlgxt9Xu7X%2B8hfsBCm92xNURurTFlkC4PSYVyUYC6US1WzzGzcvpNvEmyOu%2BDZLICNwK5ufc1Qjws%2BcV3nMSV%2Fp%2BCzIzhRobWzYzinq7Oqxyq0youCyoEIoctJ6udGCB%2FXBRCGZWlZEtc%2BI4Q4pOJX42GaiGGFpzFuo4McmIR8y2NmcypRLktCudQs5eoe67iM2jwO%2Fx6HBgvw83woV9m9%2FmOVXIBrr9woqkRwXcFowcMr6WPILE63lWKsxLLGsrLV8%2BZirOxJ8yOpfUywDQN%2B9vIK%2BeE%2B4u6YTDOaVverBY2tICvu1Red5jyPCtfu3gk3AE%2BKXYeuFr%2FiYpFTwWgDykEvyeZTJHoi%2BxKm90y%2FGlikcqnEkriKeBoKKfXYeMX7JeDANMwMIDDNN3kSp75fTkQU86N%2BpSla9x1X%2Bmh93Nz7hZPeLi6Qm3rn0ip64uCNsd7ox994YN2tHh7mf3hr9ddsOYx%2Fb1YG6Qq9%2FktBXY11sbZiZOtiF%2B9txBy1MFYjZH2FXfa3j1GeionoZX42X%2FZAqPpVD%2B3qB%2F0APlXFViy95jyg6trecqR7EKyzZvKfc0Tdk%2F%2FiRB%2F9Dw%3D%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E)

Supporting Documentation
* [Business Process Diagram (PDF)](docs/business_process/business_process_diagram.pdf)
* [One-Page Process Explanation (PDF)](docs/business_process/business_process_explanation.pdf)
