# Banking-app-Mini-project
def Show_balance(balance): #This function shows the account Balance when called.
    print("***************************")
    print(f"Your balance is ${balance:.2f}")
    print("***************************")

def deposit(): #This function takes the user deposit and returns the amount.
    print("***************************")
    amount=float(input("Enter an amount you want to deposit:"))
    print("***************************")

    if amount < 0:
        print("***************************")
        print("Please Enter A Valid Amount")
        print("***************************")
        return 0
    else:
        return amount

def withdraw (balance): #This Function allows the user to withdraw funds from the account.
    print("***************************")
    amount = float(input("enter amount to be withdrawn"))
    print("***************************")

    if amount > balance:
        print("***************************")
        print("Insufficient funds")
        print("***************************")
        return 0
    elif amount < 0:
        print("***************************")
        print("Amount must be less than 0")
        print("***************************")
    else:
        return amount

def main(): #This is the main function that runs the whole program.
    balance=0
    is_running= True

    while is_running:
        print("***************************")
        print("Banking program")
        print("***************************")
        print("1. Show Balance")
        print("2. Deposit")
        print("3. Withdraw")
        print("4. Exit")
        print("***************************")
        choice = input("Enter your choice (1-4):")

        print("***************************")

        if choice=='1':
            Show_balance(balance)
        elif choice == '2':
            balance += deposit()
        elif choice == '3':
            balance-= withdraw(balance)
        elif choice== '4':
            is_running = False
        else:
            print("***************************")
            print("that is not a valid choice")
            print("***************************")
    print("***************************")
    print("Thank You! have a beautiful day!!!")
    print("***************************")

main()
