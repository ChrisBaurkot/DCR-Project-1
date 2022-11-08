# DCR Project #1

## Presentation Slides
https://docs.google.com/presentation/d/1-1hZoFboclRLvzZiwhu1CCzvfWnd_d9yo-xKOZOKsJk/edit#slide=id.g17e7ab02de7_0_135

## Idea:
Recent developments in open banking interfaces and the arrival of some financial consolidators app/fintechs (such as Plaid, Yodlee, Klarna, etc) have made it possible for clients with multiple banking relationships to service all of their banking needs (such as Payment Initiation, Account Balances & Transaction Reporting and/or Data Analytics) via a single banking channel. Note that this is already a well-accepted and well-established offering in Europe (enabled mostly due to regulatory mandates such as the 'Second Payment Services Directive' i.e. PSD2 across Europe, which standardized Open Banking requests for Payment Initiation and Account Reporting across the banks operating in the region). In the US there currently is no similar initiative from the authorities for standardization across banks, however the availability of Open Banking/API from most of these banks in the last few years has enabled several tech organizations (e.g. Plaid or Yodlee) to build interfaces to several banks and offer these connectivity solutions to businesses that may then use that data to create even more-value-added services.

This is the use-case gap that our product seeks to fill - we aim to build a service that will have the ability to consolidate, view and manage multiple banking accounts through a single interface regardless of the underlying banks that our clients have accounts with, making it easier for people to see the full picture of all their finances.

To that end, we will:
Build UI to get the users to enter their Banks and Accounts details (users will have to select from banks that we already have data connectivity with).
Consolidate, parse and normalize all client account data from all provided sources so that the user can see all the Balances & Transaction Reporting (in Reference Currency USD), and also be able to Initiate Payments from those ‘Multibank’ accounts from a single channel.
Build Management Reporting for internal (i.e. Bank or Fintech’s) consumption that will detail the quarterly/yearly growth in number of multibank accounts, geo-locations of the banks/accounts serviced by our product, user profile (gender, age, etc) of users of our service, monthly balance trends, etc (see also HVPLOT section below).

## Advantages of Multibank:
Broadened Search across connected accounts: If a client uses multiple accounts across several banks providers, retrieving information about a specific transaction, identifying duplicate payments or conducting an audit of historical transactions can be time-consuming and labor-intensive due to having to log into several banking portals/apps to get that information.
Enhanced Security: Accessing multiple accounts via a single channel negates the need to use different user-id/passwords for individual accounts and simplifies authentication processes by providing an integrated gateway to multiple accounts.
Standardized Data Analytics/Insights across accounts: Even though these accounts are held with multiple banking partners, multibanking provides a real-time, holistic view of all accounts of the client.


## Hvplot:
Display people geographically throughout major cities or highly populated areas that have multiple accounts with different banks or credit card companies.
Display a graph of people and ages of those people that may have multiple accounts or just one.
Display differences between numbers of accounts in the past 3 years.

 
## Steps:
Create the following spreadsheets with data (20 people for each bank, each bank should have 2 to 3 same people):

BANKSTATEMENT.XLS 
Client_id (PK)
ABA Number (FK)
Account Number (1234567890)
Transaction Detail (Date, Amount) (12/04/21, +$3000.00)
Opening Balance ($50,000.00)
Available Balance USD ($48,000.00)
Available Balance  EUR (20,000.00)
Available Balance YEN (190,000.00)
Closing Balance ($51,000.00)

CLIENTS.XLS
Client_id (PK)
SSN (123-456789)
Gender (M) */clean up for the future/
Marital status (Married) */clean up for the future/
First Name (John)
Last Name (Smith)
Address (123 North Ave)
City (New York)
State (NY)
Zip (30456)


BANKS.XLS
ABA Number (PK)
Bank Name
Address (123 Bank Street)
City (New York)
State (NY)
Zip (10001)



## List of Target Banks: 
Ravi (Chase, Bank of America, Wells Fargo, Citibank).
Christopher (CapitalOne, Fifth Third Bank, PNC Bank, Truist).
Dmitry (TD Bank, US Bancorp, ​​Goldman Sachs, Bank of New York Mellon).

## Requirements: 
Use pandas to clean data sets
Use Pyviz, Geoviews and Hvplot to make the following visualizations:
     For Client:
month-wise/yearly trends of consolidated balances (across all banks)
balances in each individual account
Cities where accounts are held
     For Bank:
Ages of account holders
Gender-wise (bar chart) plot of account-holders
Cities/States where account holders live

Save png images of your visualizations to distribute to class
Use at least one API
One new python library
Create README in repository as a write summarizing findings (code images slides and readme)
Use large data sources, contain more data than needed
10 min presentation with financial conclusions and findings
Using one new python library (conversion rates for currencies)














