balance = 10000 pin = 1234 attempts = 3

//balance stores the initial account balance. pin stores the user’s 4-digit PIN. attempts limits the number of PIN entry tries to 3.

Line 5–12: PIN Verification

while attempts > 0: entered_pin = int(input("Enter your 4-digit PIN: ")) if entered_pin == pin: print("PIN verified successfully!\n") break else: attempts -= 1 print(f"Incorrect PIN! Attempts left: {attempts}") else: print("Too many incorrect attempts. Exiting...") exit()

//Uses a while loop to allow multiple attempts. If entered PIN is correct, program continues (break). If incorrect, attempts decreases by 1. If all attempts are used, program exits.

Line 14–36: ATM Menu Loop

while True: print("\n------ ATM MENU ------") print("1. Check Balance") print("2. Deposit Money") print("3. Withdraw Money") print("4. Exit") choice = int(input("Enter your choice: "))

//Infinite loop (while True) keeps the menu running until exit. Displays options for Check Balance, Deposit, Withdraw, Exit. Reads user choice and converts to integer.

Line 18–19: Check Balance

if choice == 1: print("Your current balance is:", balance)

//Shows the current account balance when option 1 is selected.

Line 21–25: Deposit Money

elif choice == 2: deposit = int(input("Enter deposit amount: ")) if deposit > 0: balance += deposit print("Amount deposited successfully!") else: print("Invalid amount")

//User enters deposit amount. Adds the amount to balance if it is positive. Prints a confirmation message.

Line 27–31: Withdraw Money

elif choice == 3: withdraw = int(input("Enter withdrawal amount: ")) if withdraw > 0 and withdraw <= balance: balance -= withdraw print("Please collect your cash") else: print("Insufficient balance or invalid amount")

//User enters withdrawal amount. Checks if balance is sufficient and amount is positive. Deducts amount and prints a confirmation message.

Line 33–35: Exit

elif choice == 4: print("Thank you for using the ATM. Goodbye!") break

//Ends the program when user selects option 4. break exits the infinite loop.

Line 37–38: Invalid Choice

else: print("Invalid choice, please try again.")

//Handles any invalid input (not 1–4). Prompts user to try again
