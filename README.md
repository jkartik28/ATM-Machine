# ATM-Machine


balance = 10000
print("\nWelcome to our ATM. How we can a help you...?")

def display_menu() :
    print("\n........ATM Menu......")
    print("1. Check Balance")
    print("2. Withdrawl Money")
    print("3. Deposit Money")
    print("4. Exit ")

while True :
    display_menu() 
    choose = input("Choose Option in between (1-4) : ")
    if choose == "1" : 
        print("Your Current balance is :",balance)
    elif choose == "2" :
        withdrawl_amount = float(input("Enter a amount : "))
        if withdrawl_amount <= balance and withdrawl_amount > 0 :
            balance -= withdrawl_amount
            print("Your amount", withdrawl_amount,"succesfully withdrawl.....!")
        elif withdrawl_amount <= 0 :
            print("Enter a valid amount ")
        else :
            print("No have enough balance in your account....!")
    elif choose == "3" :
        deposit_amount = float(input("Enter a amount : "))
        if deposit_amount > 0 :
            balance += deposit_amount
            print("Your", deposit_amount,"successfully Deposit in your account")
        else :
            print("Invalid amount")
    elif choose == "4" :
        print("Thank you for using ATM....! Have a nice Day")
        break
    else :
        print("Enter a valid number.....!")
