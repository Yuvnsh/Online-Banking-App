# Online-Banking-App  PYthon Project
This code implements an interactive online banking application where users can sign in, check their account balance, deposit and withdraw money, transfer funds to other accounts, calculate deposit interest rates, and calculate compound interest based on the principal amount.
1. Description:
   The application begins with a welcome message to introduce users to the online banking system.
   
2. Sign-In Function (sign_in):
   - This function allows new users to create an account by entering their username and a 6-digit PIN.
   - It checks if the PIN is of the desired length; if not, it prompts for another PIN entry.
   
3. Forgot PIN Function (forgot_pin):
   - This function helps users recover their forgotten PIN by creating a new 6-digit PIN.

4. Deposit Interest Calculation Function (deposit_interest):
   - Implements compound interest calculation using the formula A = P * e^(rt), where A represents future value,  as principal amount,  as the rate of interest per year in decimal form, as a period in years.

5. Login Function :
    - Allows existing users to log into their accounts.
    - Provides options for depositing money into their account or withdrawing funds from it.
    - Offers fund transfer functionality along with checking current balance and calculating deposit interest rates based on deposited amounts.

6. Main Menu & Exit Functions: 
    These functions help manage user interaction with different functionalities within the system while also enabling controlled exits from transactions or login sessions.

7. The main program loop ensures continuous operation until exiting is initiated by user choice.

8. At the last step `main_menu()` is called which initiates the execution of this code whenever it's run.


Overall, this program provides essential operations that one would expect from an online banking system while ensuring user security through PIN verification and recovery functionality.

