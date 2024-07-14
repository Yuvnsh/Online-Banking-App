Overview
This project is a Python-based online banking application that allows users to manage their bank accounts through an interactive and secure software system. The program provides various functionalities including account creation, deposit and withdrawal of funds, fund transfer between accounts, checking account balance, calculating deposit interest rates, and compound interest calculations based on the principal amount.

Features
1. User Authentication: New users can create an account by providing a username and 6-digit PIN. Existing users can log in using their credentials.
2. Security Measures: The system includes appropriate security measures such as PIN validation and recovery functionality to ensure user privacy.
3. Account Operations:
   - Deposit: Users can add funds to their account with the specified amount.
   - Withdrawal: Funds can be withdrawn from the account if sufficient balance is available.
   - Fund Transfer: Users are able to transfer money securely between accounts by providing destination account details.
   - Check Balance: Provides instant access to check the current account balance at any time.
4. Interest Calculations:
   - Deposit Interest Rate: The system calculates deposit interest rates based on deposited amounts in accordance with preset criteria for different rate structures.
   - Compound Interest Calculation: Allows users to calculate compound interest based on principal amount considering varying time periods and applicable rates.

Implementation
The program utilizes Python's core functionalities along with math operations for financial calculations such as compound interest determination. It incorporates recursive functions for PIN validation during sign-in or recovery operations while ensuring smooth user interaction within a command-line interface.

 Usage
To use this application:
1. Clone or download the repository containing this project onto your local machine.
2. Open a terminal or command prompt in the project directory where "banking_app.py" is located.
3. Run the script using `python banking_app.py`.
4. Follow the prompts provided in the command-line interface to interact with different features of this online banking application.

So in this project -

1. Description:
   The application begins with a welcome message introducing users to the online banking system.
   
2. Sign-In Function (sign_in):
   - This function allows new users to create an account by entering their username and a 6-digit PIN.
   - It checks if the PIN is of the desired length; if not, it prompts for another PIN entry.
   
3. Forgot PIN Function (forgot_pin):
   - This function helps users recover their forgotten PIN by creating a new 6-digit PIN.

4. Deposit Interest Calculation Function (deposit_interest):
   - Implements compound interest calculation using the formula A = P * e^(rt), where A represents future value,  as principal amount, as the rate of interest per year in decimal form,  as time in years.

5. Login Function :
    - Allows existing users to log into their accounts.
    - Provides options for depositing money into their account or withdrawing funds from it.
    - Offers fund transfer functionality along with checking current balance and calculating deposit interest rates based on deposited amounts.

6. Main Menu & Exit Functions: 
    These functions help manage user interaction with different system functionalities while enabling controlled exits from transactions or login sessions.

7. The main program loop ensures continuous operation until exiting is initiated by user choice.

8. At the last step `main_menu()` is called which initiates the execution of this code whenever it's run.


Overall, this program provides essential operations that one would expect from an online banking system while ensuring user security through PIN verification and recovery functionality.

