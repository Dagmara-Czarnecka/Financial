# Financial
In this project, I used the Financial database, which contains information about loans that have been repaid or not.
It is worth noting that the database is based on real data that has been anonymized in order to make it public. It is a collection of financial information from a certain Czech bank. The dataset includes data for over 5,300 customers with approximately one million transactions. What's more, the bank also provided data for nearly 700 loans granted and about 900 credit cards issued

Description of the tables 

Card
A table containing credit card details.

Columns:

card_id - card id,
disp_id - card holder id,
type - card type (classic, gold, etc.),
issued - card issue date.

Disp
The table contains information about persons assigned to a given card. Its name comes from the shortened name of the disposer, i.e. the person who can also use the card.

Columns:

disp_id - card holder id,
client_id - client id,
account_id - id of the account to which the card is assigned,
type - card management type (owner or administrator).

Client
The table contains the basic characteristics of the client.

Columns:

client_id - client id,
gender - gender,
birth_date - date of birth,
district_id - id of the district of residence.


District
The table contains the demographics of the district.

Columns:

district_id - district id,
A2 - name of the district,
A3 - region,
A4 - number of inhabitants,
A5 - number of communes with less than 499 inhabitants,
A6 - the number of communes with inhabitants between 500-1999,
A7 - number of communes with inhabitants between 2000-9999,
A8 - number of communes with inhabitants over > 10,000,
A9 - number of cities,
A10 - the ratio of the number of inhabitants of cities to villages,
A11 - average salary,
A12 - unemployment rate in 1995,
A13 - unemployment rate in 1996,
A14 - number of entrepreneurs per 1000 inhabitants,
A15 - number of crimes committed in 1995,
A16 - number of crimes committed in 1996.

Account
The table contains account information.

Columns:

account_id - account id,
district_id - id of the district of the branch where the account was created,
frequency - frequency of issuing statements,
date - account creation date.

Trance
The table contains information about transactions.

Columns:

trans_id - transaction id,
account_id - id of the account where the transaction is saved,
date - transaction date,
type - whether a debit/credit transaction,
operation - transaction type,
amount - transaction amount,
balance - account balance after transaction,
k_symbol - transaction characteristics,
bank - the bank of the transaction partner,
account - account of the transaction partner.

Order
The table contains the characteristics of direct debit.

Columns:

order_id - identifier,
account_id - account id,
bank_to - recipient's bank id,
account_to - recipient's account id,
amount - transfer amount,
k_symbol - payment characteristics.
loans
The table contains information about the status of the loan.

Columns:

loan_id - loan id,
account_id - id of the account applying for a loan,
date - date of granting the loan,
amount - loan amount,
duration - duration of the loan,
payments - monthly payment amount,
status - loan repayment status.
