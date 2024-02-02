﻿| Work Item Type | ID   | Title                                                                            | State      | Tags                      | Repro Steps                                                                                                                                                                                                                                                                                                                                                                                                             | Severity                                                                                                                          | Closing Comment                                                                                                                                                                                                                          |                                                                                |              |   |
|----------------|------|----------------------------------------------------------------------------------|------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------|---|
| Bug          | 46 | Deposit Chequing - Improper Final Balance 2                  | Active | Exploratory Testing | Starting state: Off Inputs: 0 - \$20 bills, Card 2, deposit \$200 into chequing Expected output: \$ 300, Card #1 Actual output: Invalid Account type,                                                                                           |
| Bug          | 45 | 16.Withdraw - Withdrew more from chequing than in the account                  | Resolved | Manual Scripted Testing | 1. Logged in with valid Card and PIN. 2. Select Withdrawal from menu. 3. Select Chequing account. 4. Select a withdrawal amount less than amount in the ATM, but more than balance in chequing.  Expected outcome: Reject the withdrawal. Actual outcome: Allowed us to withdraw more money than in the chequing account.                                                                                             | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 44 | 40.Login - Initial PIN message after entering incorrect twice then correct PIN | Resolved | Manual Scripted Testing | 1. Enter a valid card number. 2. Enter an incorrect PIN. 3. The system displays a prompt to re-enter PIN. Enter an incorrect PIN. 4. The system displays a prompt to re-enter PIN. Enter an incorrect PIN. 5. The system displays a prompt to re-enter PIN. Enter the correct PIN.  Expected outcome: PIN accepted, logged in to account. Actual outcome: Clears error message but initial PIN prompt is displayed.   | 4 - Low                                                                                                                         |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 43 | 39.Login - Initial PIN message after entering incorrect then correct PIN       | Active   | Manual Scripted Testing | 1. Enter a valid card number. 2. Enter an incorrect PIN. 3. The system displays a prompt to re-enter PIN. Enter an incorrect PIN. 4. The system displays a prompt to re-enter PIN. Enter the correct PIN.  Expected outcome: PIN accepted, logged in to account. Actual outcome: Clears error message but initial PIN prompt is displayed.                                                                            | 4 - Low                                                                                                                         |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 42 | 37.Login - Asks for PIN again after entering correct PIN                       | Active   | Manual Scripted Testing | 1. Enter a valid card number. 2. Enter an incorrect PIN. 3. The system displays a prompt to re-enter PIN. Enter the correct PIN.  Expected outcome: PIN accepted, logged in to account. Actual outcome: Clears error message but initial PIN prompt is displayed.                                                                                                                                                     | 4 - Low                                                                                                                         |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 41 | 33.Inquiry - No Savings option in menu                                         | Active   | Manual Scripted Testing | 1. Logged in with valid card and PIN. 2. Select Balance Inquiry from menu.  Expected outcome : 3 accounts should be displayed (Chequing, Savings, and Money Market) Actual outcome: Savings account is not displayed as an option.                                                                                                                                                                                    | 1 - Critical                                                                                                                    |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 19 | Insert Pin - Large Pin Crashes App                                             | Active   | Exploratory             | Turn machine on Insert number of bills in ATM Insert card Type valid card number (1) Type an 11 digit or higher pin number Program freezes and cannot turn off machine                                                                                                                                                                                                                                                | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 18 | Transfer amount less than 50 cents is invalid                                  | Resolved | Exploratory             | Turn on ATM Input valid number of\$20 bills Input valid credit card & PIN Select Transfer Select Chequing or Savings (I chose Chequing) Select unchosen account in step 5 (I chose Savings) Input transfer amount under 50 cents (I chose 4 cents)  Output is: AMOUNT:\$0.0-46TOTAL BAL:\$999.53 AVAILABLE:\$999.53  The total balance should not have decreased                                                 | but instead increased by 4 cents (in my case)                                                                                    | 3 - Medium                                                                                                                                                                                                                             |                                                                                |              |   |
| Bug          | 17 | Transfer Savings to Money Market - Rejected Valid Transfer                     | Resolved | Exploratory             | Starting state: Logged in with Card 2,\$5000 in Money Market,\$1000 in Savings  Inputs: Navigate to transfer of\$1000 from savings to money market  Expected output:\$0 in savings,\$6000 in money market  Actual output: Invalid from account type   Rejected the transfer of\$1000 from savings into money market, even though there is exactly\$1000 in the Savings account.                                       | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 16 | Transfer Money Market to Chequing                                              | Resolved | Exploratory             | Starting state: Off  Inputs: 1 20$ initially in ATM, transferring 100$ from money market to checking  Expected output: 200$ in checking, 4900$ left in money market  Actual output:\$199.50 in Money Market,\$99.50 transffered   Transferred 50 cents less than requested, and from the wrong account.                                                                                                               | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 15 | Inquiry Money Market - Invalid Account Type                                    | Active   | Exploratory             | Starting state: Off  Inputs: Initialize ATM with 0 bills                                                                                                                                                                                                                                                                                                                                                               | Login with Card 2                                                                                                                 | Navigate to inquiry into Money Market  Expected output: 5000 to be displayed in money market  Actual output: Error message - Invalid account type   Showed an error message when trying to display balance of money market account.   | 3 - Medium                                                                   |              |   |
| Bug          | 14 | Withdraw Money Market - Improper Amount Withdrawn                              | Active   | Exploratory             | Starting state: Off  Inputs: Initialize ATM with 100\$20 bills, login with Card 2,navigate to withdraw from money market  Expected output: 4980 in money market, 20 withdrawn  Actual output:\$4960 in money market,\$40 withdrawn   Withdrew\$40 from Money Market and displayed a final balance of\$4960 when only\$20 was requested                                                                                | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 13 | Deposit Money Market - Improper Balance                                        | Active   | Exploratory             | Starting state: On, logged in to Card 2  Inputs: Deposit 1000$ into money market  Expected output: 6000$ in money market  Actual output: 5990$ in money market   \$10 less was deposited into the money market account than expected. The wrong card number is also displayed (3 rather than 2).                                                                                                                      | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 12 | Deposit Chequing 3 - Wrong Card Number                                         | Active   | Exploratory             | Starting state: Off  Inputs: Initially input 20$ into ATM, deposit 50$ into checking  Expected output: Card #2  Actual output: Card #3   Shows Card 3 (which doesnt exist) instead of Card 2                                                                                                                                                                                                                          | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 11 | Deposit Chequing 3 - Improper Balance                                          | Active   | Exploratory             | Starting state: Off  Inputs: Initially have 1 20$ bill in ATM, login with card 2, deposit 50$ into checking  Expected output: 150$ in checking  Actual output: 140$ in checking  \$10 less was deposited into chequing than expected.                                                                                                                                                                                 | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 10 | Transfer Money Market to Checking - Poor Error Message                         | Resolved | Exploratory             | Starting state: logged in with card# 1  Inputs: transferring\$ 6000 from Money Market to checking  Expected output: Dont allow the transfer since there is only 5000 in money market  Actual output: Did not allow the transfer    As expected, the transfer was not allowed. However, the error message could be a little more descriptive.                                                                          | 4 - Low                                                                                                                         |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 9  | Transfer Savings to Checking - Swapped Transfer Direction                      | Active   | Exploratory             | Starting state: Off  Inputs: transferring\$1000 from savings to checking   Expected output:\$ 2490 - in saving and \$1290 - in checking  Actual output: Transferred\$999.50 to Savings from Chequing    Swapped the transfer direction while transferring an invalid amount from Checking to Savings. Checking does not have\$1000 to transfer to Savings.                                                            | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 8  | Transfer Savings to Chequing - Wrong Amount Transferred                        | Active   | Exploratory             | Starting state: Off  Inputs: transferring\$1000 from savings to checking   Expected output:\$ 2490 - in saving and \$1290 - in checking  Actual output:\$ 1289.50 is the wrong output expected, should be 1290$    Transferred 999.50$ (50 cents less)                                                                                                                                                                | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 7  | Inquiry Money Market - Unknown Error message                                   | Resolved | Exploratory             | Starting state: On                                                                                                                                                                                                                                                                                                                                                                                                     | logged in with Card 1  Inputs: Inquiry into money market  Expected output: 5000$ in money market  Actual output:\$1000 in Savings | which is correct for savings but it is not the account we requested                                                                                                                                                                      | an Unknown Error message was displayed and\$500 was seemingly withdrawn     | 3 - Medium |   |
| Bug          | 6  | Withdraw Checking - Withdrew Double Requested                                  | Resolved | Exploratory             | Starting state: On, logged in as Card 1, 10\$20 bills in the ATM,\$290 balance in Card 1  Inputs: withdraw\$20 from checking  Expected output:\$ 270 left,\$20 Withdrawn  Actual output: Withdrew\$40,\$250 balance   Withdrew\$40 from chequing account, double the requested amount.                                                                                                                                | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 5  | Deposit Chequing 2 - Improper Card Number                                      | Active   | Exploratory             | Starting state: On , logged in as Card 1  Inputs: deposit\$2500 into savings  Expected output:\$ 3500, card #1  Actual output:\$ 3490, card #2   Card number is 2, but should be 1.                                                                                                                                                                                                                                   | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 4  | Deposit Chequing 2 - Improper Balance                                          | Active   | Exploratory             | Starting state: On , logged in as Card 1  Inputs: deposit\$2500 into savings  Expected output:\$ 3500, card #1  Actual output:\$ 3490, card #2    Total Balance is\$3490, it should be\$3500.                                                                                                                                                                                                                         | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 3  | Deposit Chequing - Improper Card Number                                        | Active   | Exploratory             | Starting state: Off  Inputs: 0 -\$20 bills, Card 1, deposit 200$ into chequing  Expected output:\$ 300, Card #1  Actual output:\$290, Card #2   Card number is 2, but should be 1.                                                                                                                                                                                                                                    | 3 - Medium                                                                                                                      |                                                                                                                                                                                                                                          |                                                                                |              |   |
| Bug          | 2  | Deposit Chequing - Improper Final Balance                                      | Active   | Exploratory             | Starting state: Off Inputs: 0 -\$20 bills, Card 1, deposit 200$ into chequing Expected output:\$ 300, Card #1 Actual output:\$290, Card #2 Total balance is 290,\$10 less than it should be                                                                                                                                                                                                                   | 2 - High                                                                                                                        |                                                                                                                                                                                                                                          |                                                                                |              |   |