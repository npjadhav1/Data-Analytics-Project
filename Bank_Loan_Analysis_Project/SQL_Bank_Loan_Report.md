# A. KPI’s

## 1. Total Loan Applications:


sql
SELECT COUNT(id) AS Total_Applications FROM bank_loan_data


![image](https://github.com/user-attachments/assets/255a765d-eb77-4065-9280-980d796125c7)


---

## 2. MTD Loan Applications

sql
SELECT COUNT(id) AS Total_Applications FROM bank_loan_data
WHERE MONTH(issue_date) = 12;


![image](https://github.com/user-attachments/assets/2071e645-3ae2-4a57-b7c1-e71598a30664)


---

## 3. PMTD Loan Applications

sql
SELECT COUNT(id) AS Total_Applications FROM bank_loan_data
WHERE MONTH(issue_date) = 11;


![image](https://github.com/user-attachments/assets/aa8590ee-0909-4fb1-9354-352744655729)


---

## 4. Total Funded Amount

sql
SELECT SUM(loan_amount) AS Total_Funded_Amount FROM bank_loan_data;


![image](https://github.com/user-attachments/assets/ea202667-afff-4d1e-92fa-53d16103f0bf)


---

## B. MTD Total Funded Amount:

sql
SELECT SUM(loan_amount) AS Total_Funded_Amount FROM bank_loan_data
WHERE MONTH(issue_date) = 12


![image](https://github.com/user-attachments/assets/b34dd871-b895-409b-8789-2bf7d67e33c4)


---

## D. PMTD Total Funded Amount
sql
SELECT SUM(loan_amount) AS Total_Funded_Amount FROM bank_loan_data
WHERE MONTH(issue_date) = 11

![image](https://github.com/user-attachments/assets/b1755317-42cf-48c9-9948-8b9fd0d65c85)

---

## E. Total Amount Received

sql
SELECT SUM(total_payment) AS Total_Amount_Collected FROM bank_loan_data

![image](https://github.com/user-attachments/assets/3bca6832-bd6d-4a7d-ac4f-793dd9976800)


---

## F. MTD Total Amount Received

sql
SELECT SUM(total_payment) AS Total_Amount_Collected FROM bank_loan_data
WHERE MONTH(issue_date) = 12;


![image](https://github.com/user-attachments/assets/8ae19736-c1ee-49be-b18d-30fbd1f4e19e)


---

## G. PMTD Total Amount Received

sql
SELECT SUM(total_payment) AS Total_Amount_Collected FROM bank_loan_data
WHERE MONTH(issue_date) = 11;


![image](https://github.com/user-attachments/assets/f719d147-e861-4d98-871a-f706c5b33a35)

---

## H. Average Interest Rate:

sql
SELECT AVG(int_rate)*100 AS Avg_Int_Rate FROM bank_loan_data


![image](https://github.com/user-attachments/assets/6c6b86bd-e543-41fa-ab07-a464b77f5285)


---
## I. MTD Average Interest Rate
sql
SELECT AVG(int_rate)*100 AS MTD_Avg_Int_Rate FROM bank_loan_data
WHERE MONTH(issue_date) = 12;


![image](https://github.com/user-attachments/assets/2f5c4e0b-c902-43df-a682-a17aa6f2e4fc)

---

## I. PMTD Average Interest Rate
sql
SELECT AVG(int_rate)*100 AS PMTD_Avg_Int_Rate FROM bank_loan_data
WHERE MONTH(issue_date) = 11;


![image](https://github.com/user-attachments/assets/2f5c4e0b-c902-43df-a682-a17aa6f2e4fc)

---

## J. Avg DTI

sql
SELECT AVG(dti)*100 AS Avg_DTI FROM bank_loan_data;

![image](https://github.com/user-attachments/assets/110e8d9f-03b3-4146-8e39-b1a2ecb3124c)

---

## K. MTD Avg DTI

sql
SELECT AVG(dti)*100 AS MTD_Avg_DTI FROM bank_loan_data
WHERE MONTH(issue_date) = 12;


![image](https://github.com/user-attachments/assets/757cf58e-a83a-447c-8460-a48c3efd3220)

---

## L. PMTD Avg DTI

sql
SELECT AVG(dti)*100 AS PMTD_Avg_DTI FROM bank_loan_data
WHERE MONTH(issue_date) = 11;


![image](https://github.com/user-attachments/assets/3f57eeae-74ed-4b60-9beb-a1b6f5f03d82)


---
## M. Good Loan Percentage
sql
SELECT
    (COUNT(CASE WHEN loan_status = 'Fully Paid' OR loan_status = 'Current' THEN id END) * 100.0) / 
	COUNT(id) AS Good_Loan_Percentage
FROM bank_loan_data;


![image](https://github.com/user-attachments/assets/7b18d03b-4657-4f71-8976-613fd4044f96)

---

## N. Good Loan Applications

sql
SELECT COUNT(id) AS Good_Loan_Applications FROM bank_loan_data
WHERE loan_status = 'Fully Paid' OR loan_status = 'Current';


![image](https://github.com/user-attachments/assets/86e2e84b-02a0-4b8b-afc5-899272f2cc3f)


---

## O. Good Loan Funded Amount

sql
SELECT SUM(loan_amount) AS Good_Loan_Funded_amount FROM bank_loan_data
WHERE loan_status = 'Fully Paid' OR loan_status = 'Current';


![image](https://github.com/user-attachments/assets/a62c8ba1-c52b-4d58-8529-46a88af411f1)

---

## P. Good Loan Amount Received

sql
SELECT SUM(total_payment) AS Good_Loan_amount_received FROM bank_loan_data
WHERE loan_status = 'Fully Paid' OR loan_status = 'Current';


![image](https://github.com/user-attachments/assets/372d397f-59ed-4208-a98a-7073401e79f1)

---

## Q. Bad Loan Percentage

sql
SELECT
    (COUNT(CASE WHEN loan_status = 'Charged Off' THEN id END) * 100.0) / 
	COUNT(id) AS Bad_Loan_Percentage
FROM bank_loan_data;


![image](https://github.com/user-attachments/assets/130236f3-8cc2-4ad4-bdeb-872853608785)


---
## R. Bad Loan Applications

sql
SELECT COUNT(id) AS Bad_Loan_Applications FROM bank_loan_data
WHERE loan_status = 'Charged Off';


![image](https://github.com/user-attachments/assets/4a040723-0878-43a7-8a85-f4b3f3cc8fde)


---
## S. Bad Loan Funded Amount

sql
SELECT SUM(loan_amount) AS Bad_Loan_Funded_amount FROM bank_loan_data
WHERE loan_status = 'Charged Off';


![image](https://github.com/user-attachments/assets/603fb2e9-7d3e-4a37-b83e-09b327188d23)

---

## T. Bad Loan Amount Received

sql
SELECT SUM(total_payment) AS Bad_Loan_amount_received FROM bank_loan_data
WHERE loan_status = 'Charged Off';


![image](https://github.com/user-attachments/assets/5911c214-09da-42a4-aafb-31d9c639b2cd)


---

## U. Loan Status

sql
SELECT
        loan_status,
        COUNT(id) AS LoanCount,
        SUM(total_payment) AS Total_Amount_Received,
        SUM(loan_amount) AS Total_Funded_Amount,
        AVG(int_rate * 100) AS Interest_Rate,
        AVG(dti * 100) AS DTI
    FROM
        bank_loan_data
    GROUP BY
        loan_status;


![image](https://github.com/user-attachments/assets/e08fcb82-4e84-4cd6-b4b1-451d21161451)


---

sql
SELECT 
	loan_status, 
	SUM(total_payment) AS MTD_Total_Amount_Received, 
	SUM(loan_amount) AS MTD_Total_Funded_Amount 
FROM bank_loan_data
WHERE MONTH(issue_date) = 12 
GROUP BY loan_status;


![image](https://github.com/user-attachments/assets/63d52a67-6fd8-4a8d-9a98-32f14c79c06a)


---

## V.	BANK LOAN REPORT | OVERVIEW
## Month
sql
SELECT 
	MONTH(issue_date) AS Month_Munber, 
	DATENAME(MONTH, issue_date) AS Month_name, 
	COUNT(id) AS Total_Loan_Applications,
	SUM(loan_amount) AS Total_Funded_Amount,
	SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY MONTH(issue_date), DATENAME(MONTH, issue_date)
ORDER BY MONTH(issue_date);


![image](https://github.com/user-attachments/assets/92477800-2f39-4794-9b10-2d6a090f5b88)



---

## W. State

sql
SELECT 
	address_state AS State, 
	COUNT(id) AS Total_Loan_Applications,
	SUM(loan_amount) AS Total_Funded_Amount,
	SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY address_state
ORDER BY address_state;


![image](https://github.com/user-attachments/assets/650202d1-7d07-477c-928d-e66dd47a0e3b)


---

## X. Term

sql
SELECT 
	term AS Term, 
	COUNT(id) AS Total_Loan_Applications,
	SUM(loan_amount) AS Total_Funded_Amount,
	SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY term
ORDER BY term;


![image](https://github.com/user-attachments/assets/eb10a14a-9cab-48a9-a8c9-4cb62da9bc00)


---

## Y. Employee Length

sql
SELECT 
	emp_length AS Employee_Length, 
	COUNT(id) AS Total_Loan_Applications,
	SUM(loan_amount) AS Total_Funded_Amount,
	SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY emp_length
ORDER BY emp_length;


![image](https://github.com/user-attachments/assets/d41b1636-8b92-4423-9165-f32cd81b7427)


---

## Z. Purpose

sql
SELECT 
	purpose AS PURPOSE, 
	COUNT(id) AS Total_Loan_Applications,
	SUM(loan_amount) AS Total_Funded_Amount,
	SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY purpose
ORDER BY purpose;


![image](https://github.com/user-attachments/assets/8a7338ad-b8c2-407e-82f3-3b485f516572)


---

## V.Home Owenership
sql
SELECT 
	home_ownership AS Home_Ownership, 
	COUNT(id) AS Total_Loan_Applications,
	SUM(loan_amount) AS Total_Funded_Amount,
	SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY home_ownership
ORDER BY home_ownership;


![image](https://github.com/user-attachments/assets/dc92cca5-8570-4344-9e5d-1d029adca07a)


---
