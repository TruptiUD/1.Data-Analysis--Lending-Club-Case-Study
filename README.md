# Lending Club Case Study

### Group Details:
Group Facilitator Name: Trupti Dhumal
Group Member Name: Sunil Jadhav 
Start On: 03-Feb-2022
Deadline: 09-Feb-2022

### Problem Statement:
You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. 

Two types of risks are associated with the bank’s decision:
1. If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
2. If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

### Goal:
1. Using EDA, identify risky loan applicants. 
   When a person applies for a loan, there are two types of decisions that could be taken by the company.
    a. Loan Accepted
        i. Fully paid
        ii. Current loan running
        iii. Loan defaulted / Charged-off
    b. Loan Rejected (Applicant data not in the dataset)
2. Understand the driving factors (driver variables) behind loan default i.e the variables which are strong indicators of default

### About Repository
* Trupti_Dhumal.ipynb File -
  - This python file contins all python code required for EDA analysis
  - has divided cells by sections for Each step in EDA process i.e. data Understanding, Data Cleaning, Data Anlysis
  - comments are helpfull to understand assumptions and the each code snippet
* Lending Club PPT PDF File:- 
  - This is a power point presentation of whole EDA process follwed for this project
  - clear visualization are provided for analysis
  
### Project completion steps as follow (based on EDA)
1. Data Understanding
2. Data Cleaning and Manupulations
3. Data Analysis
  - Univeraient and segmented univarient analysis
  - business driven , type driven , data driven matrices
  - bivarient analysis
4. Presentation
5. Recommndation 

#### 1. Data Understanding
About Data Set:-
- Name - loan.csv
- The complete loan data for all loans issued through the time period 2007 t0 2011
- Source :- upgrad portal
- Domain :- Banking
- Understanding of each Variable(column) and its purpose done in this step as follows:-
    - checking number of unique values 
    - its distribution, 
    - number of NaN(missing values)
    - datatype of each variable
    - understanding weather it will impact or not
    - understanding weather the variable needs data cleaning step
- all these steps are done using python pandas functions for DatFrame and this code is present in this repositories ipynb file with the Secction named as "Data Understanding"
 
#### 4. Presentation
- The PPT Representation is uploaded in same repository(link to PPT file).
