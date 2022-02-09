# Lending Club Case Study

### Group Details:
**Group Facilitator Name:** Trupti Dhumal<br/>
**Group Member Name:** Sunil Jadhav <br/>
**Start On:** 03-Feb-2022 <br/>
**Deadline:** 09-Feb-2022 <br/>

----
### Problem Statement:
You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. 

Two types of risks are associated with the bank’s decision:
1. If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
2. If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.
----
### Goal:
1. Using EDA, identify risky loan applicants. 
   When a person applies for a loan, there are two types of decisions that could be taken by the company.
    1. Loan Accepted
        1. Fully paid
        2. Current loan running
        3. Loan defaulted / Charged-off
    2. Loan Rejected (Applicant data not in the dataset)
2. Understand the driving factors (driver variables) behind loan default i.e the variables which are strong indicators of default
----
### About Repository
* Trupti_Dhumal.ipynb File -
  - This python file contins all python code required for EDA analysis
  - has divided cells by sections for Each step in EDA process i.e. Data Understanding, Data Cleaning, Data Anlysis
  - comments are helpfull to understand assumptions and the each code snippet
* Lending Club PPT PDF File:- 
  - This is a power point presentation of whole EDA process follwed for this project
  - clear visualization are provided for analysis
----
### About Data Set provided:-
**Name :-** loan.csv --> The complete loan data for all loans issued through the time period 2007 t0 2011 <br/>
**Source :-** upgrad portal<br/>
**Domain :-** Banking<br/>

----
### Project completion steps as follow (based on EDA)
1. Data Understanding
2. Data Cleaning and manipulation
   1. Fix Rows and columns
   2. Fix Missing Values
   3. Standardize values
   4. Fix Invalid Values
   5. Filter Data
3. Data Analysis
   1. Univariate Analysis ( 5 important variables which are strong indicators of defaulters ) 
   2. Segmented Univariate Analysis
   3. Bivariate Analysis
   4. Derived Metrics
      1. Type Driven Metrics
      2. Business Driven Metrics
      3. Data Driven Metrics
4. Presentation
5. Recommndations
----
#### 1. Data Understanding
Required Libraries (importing following libraries is very first step):- 
- numpy
- pandas
- matplotlib.pyplot
- seaborn-
- warnings  --> warnings.filterwarnings("ignore")

Process:-
- read dataset into dataframe
- Display the number of columns and rows of dataframe
- Display information about the dataframe (high level overview of dataframe)
- Indivisual Column Analysis -  
   - used unique, isna, describe functions to understand nature of each column
   - used histogram and distplot for analysing each columns value distribution/frequency
- Display/look dataframe before data cleanup process 
- Percentage of missing values in the dataframe before cleanup
----
#### 2. Data Cleaning and manipulation
**note:-** code snippet refers to the perticular numbered code section from ipynb file
1. Fixing Rows And Columns<br>
     1. Fixing Rows
        1. detect unnacessary Rows (refer code snippet - 3)
            - deleting the rows with loan status "Current" as the loan is in process.
        2. delete summary Rows - No summary rows like total and subtotal present in Dataframe
        3. delete extra Rows (crefer ode snippet - 1, 2)
            - there is no extra / empty / duplicate rows in Dataframe
     2. Fixing Columns:
        1. Add coulumn names if missing :- 
            added int_rate_in_backet_range and installment_in_bucket_range these 2 columns as part of staderdize values step
        2. delete unnecessary columns :- (refer code snippet - 4) -  bellow columns are deleted from main dataframe<br/>
            'delinq_2yrs',   'earliest_cr_line',    'inq_last_6mths',    'open_acc',    'pub_rec',    'revol_bal',    'revol_util',    'total_acc',
            'initial_list_status',    'out_prncp',    'out_prncp_inv',    'total_pymnt',    'total_pymnt_inv',    'total_rec_prncp',    'total_rec_int',    'total_rec_late_fee',    'recoveries',    'collection_recovery_fee',    'last_pymnt_d',    'last_pymnt_amnt',    'next_pymnt_d',    'last_credit_pull_d',    'collections_12_mths_ex_med',    'mths_since_last_major_derog',    'policy_code',    'application_type',    'annual_inc_joint',    'dti_joint',    'verification_status_joint',    'acc_now_delinq',    'tot_coll_amt',    'tot_cur_bal',    'open_acc_6m',    'open_il_6m',   'open_il_12m',    'open_il_24m',    'mths_since_rcnt_il',    'total_bal_il',    'il_util',    'open_rv_12m',   'open_rv_24m',    'max_bal_bc',    'all_util',    'total_rev_hi_lim',    'inq_fi',-    'total_cu_tl',    'inq_last_12m',    'acc_open_past_24mths',    'avg_cur_bal',    'bc_open_to_buy',    'bc_util',    'chargeoff_within_12_mths',    'delinq_amnt',    'mo_sin_old_il_acct',    'mo_sin_old_rev_tl_op',   'mo_sin_rcnt_rev_tl_op',    'mo_sin_rcnt_tl',    'mort_acc',    'mths_since_recent_bc',    'mths_since_recent_bc_dlq',    'mths_since_recent_inq',    'mths_since_recent_revol_delinq',    'num_accts_ever_120_pd',    'num_actv_bc_tl',    'num_actv_rev_tl',   'num_bc_sats',    'num_bc_tl',    'num_il_tl',    'num_op_rev_tl',   'num_rev_accts',    'num_rev_tl_bal_gt_0',   'num_sats',    'num_tl_120dpd_2m',    'num_tl_30dpd',    'num_tl_90g_dpd_24m',    'num_tl_op_past_12m',    'pct_tl_nvr_dlq',    'percent_bc_gt_75',   'pub_rec_bankruptcies',    'tax_liens',    'tot_hi_cred_lim',    'total_bal_ex_mort',    'total_bc_limit',    'total_il_high_credit_limit'
        
        3. spliting columns for more data - no columns splitted
        4. Rename Columns Consistently :- (refer code snippet - 5) bellow columns are renamed -
            'term' renamed as 'term_in_months', 
            'issue_d' renamed as 'loan_issue_date'
        5. Merge columns for identifiers :- no columns are merged
        6. Align missaligned columns :- no missaligned columns are found
2. Fix Missing Values
3. Standardize values
4. Fix Invalid Values
5. Filter Data
----
#### 3. Data Analysis
----
#### 4. Presentation
* Link To Presentation PPT PDF File :- link
* Assumptions Made during complete analysis process
----
#### 5. Recomndations

