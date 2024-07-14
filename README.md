# Online-Banking-App  Python Project



import math #import math = it is 

print (" Welcome to the online banking application  ")
def sign_in():
                    global name #username
                    global pin # #password
                    global cb # current balance
                    global option_1 #option1
                    global rate 
                    
                    name = str (input("Please create your username : "))
                    pin = str (input ("Please create your 6 digits pin :"))
                    if len (pin)== 6:
                                        pin = pin
                                        print("Thanks for creating your bank account")
                    else: 
                                        print("Note : The pin has to be in 6 digits")
                                        new_pin = str (input("please create your 6 digits pin : "))
                                        if len(new_pin) != 6:
                                                            print(" Note : The pin has to be in 6 digits ")
                                                            sign_in()
                                        else :
                                                            pin = new_pin
                                                            print("The new pin has been stored successfully, please log in with  " , (pin))
                    
                                        print ("Thanks for creating your bank account")

def forgot_pin():
                    
                                        recover_pin = str (input("Please create new your 6 digits pin :"))
                                        if len (recover_pin) != 6:
                                                            print (" Note : The pin has to be in 6 digits ")
                                                            forgot_pin()
                                        else :
                                                            pin = recover_pin
                                                            print("The new pin has been stored successfully, please log in with  " , (pin))
                                                            
                                                            sign_in()
                                                            
forgot_pin()
                                        
                                                            
def deposit_interest (p,r,t):  # A = Pe^(rt) which is the formula of calculating the compound interest.
                    p = float(p) # p=principal
                    r=float(r) #r = rate
                    t=float(t) # t = time
                    rt = r*t    # r*t = rate*time
                    e = math.exp(rt)  # e = e^(rt)
                    #Calculation
                    a =  p * e #Future value of your investment 
                    return a
print ("Your deposit interest = "),deposit_interest(1000,0.05,5)



def login(): 
                    #name1 represents username
                    #pin1 represents user pin
                    name1 = str(input("please enter your user name :"))
                    pin1 = str (input("Please enter your pin :"))    
                    
                    #check  if the name and pin match 
                    list_menu = ["1-Deposit", "2-Withdraw","3-Transfer","4-Check Balance", "5-Deposit interest rate", "6-Calculate compound interest"]
                    for b in list_menu:
                                        print(b)
                    choose = int(input ("Please enter your choice below"))
                    d = 0 # deposit
                    w = 0 # withdraw
                    cb = 0 #current balance
                    if choose == 1:
                                        d = int(input("Please enter the amount you want to deposit"))
                                        cb = cb + d
                                        print("Your current balance is now ", cb)
                                        
                    elif choose == 2:
                                        w = int(input("Please enter the amount you want to withdraw"))
                                        if w >cb:
                                                            print("Your balance is not sufficient for this transaction")
                                        login()
                                                            
                    else:
                                        cb = cb - w
                                        print("Your current balance is now ", cb)
                                        
                    if choose == 3:
                                        desk = str(input("Please enter the account number of your destination in a digits format"))
                                        if len(desk)== 8:
                                                            amount = int(input("Please enter the amount you want to transfer"))
                                                            if amount >cb :
                                                                                print("Your balance is not sufficient for this transaction")
                                        else: 
                                                            cb = d - amount 
                                                            print("The transaction of "+ str(amount) + " has been transferred to " +" " +str(desk)+""+ "Your current balance is now ", cb)
                    else:
                                                            print("Invalid account number")
                    
                    if choose == 4:
                                        print("Your current balance is now ", cb)
                    
                    elif choose == 5:
                                        if d > 50000:
                                                            rate =3
                    elif d > 30000:
                                                            rate = 2
                    else:               
                                                            rate = 1.5
                    print("Your current deposit interest rate is : "+""+str(rate)+" %" ) 
                    
                    if choose == 6:
                                        list_option = ["Calculate your deposit compound interest based on CB","2-Calculate your deposit compound interest based on input "]
                                        for n in list_option:
                                                            print (n)
                    choice  = int(input("Please enter your choice from the options above"))
                    if choice == 1:
                                        timing= str (input("how many years you want to invest your money :"))
                                        if d > 50000:
                                                            rate_x = 3/100
                                        elif d > 30000:
                                                            rate_x = 2/100
                                        else:               
                                                            rate_x = 1.5/100
                                                            
                                        print("Your current balance in"+ ""+"timing"+" "+"years will be :" )
                                        print ( deposit_interest(cb, rate_x, timing))
                    elif choice == 2:
                                        timing = str(input("how many years you want to invest your money : "))
                                        money = str (input("Please enter the amount you want to invest : "))
                                        money = int(money)
                                        if d > 50000:
                                                            rate_x = 3/100
                                        elif d > 30000:
                                                            rate_x = 2/100
                                        else:               
                                                            rate_x = 1.5/100
                                        
                                                            
                                        print("Your current balance in"+ ""+"timing"+" "+"years will be :" )
                                        print ( deposit_interest(money, rate_x, timing))
                    else : 
                                        print("Option is not available, back to the main menu")
                                        login()
                                        
                                        
                    if name1 == name and pin1 == pin :
                                        print("Welcome to the online banking application" +" " + name )
                                        print("Please choose the menu down here")
                    else: 
                                        print("Either your username or pin is wrong. Did you create your account?")
                                        list1 = ["1-yes", "2-no."]
                                        for i in list1:
                                                            print(i)

                                        inp = int (input("Enter your choice below : "))
                                        if inp == 1:
                                                            list2 = ["1- Do you want to attempt login again? ","2- You forgot your pin"]
                                        for e in list2:
                                                            print(e)
                                        the_answer = str (input("Please enter your choice"))
                                        the_answer = int (the_answer)
                                        if the_answer == 1:
                                                            login()
                                        elif the_answer == 2:
                                                            forgot_pin()
                                        else: 
                                                            print("Option is not available ")
                                                            login()
                    if inp == 2:
                                        print ("Please create your account")
                                        sign_in()
                    exit()
                                        
def main_menu():
                    option_one = int(input("Please choose 1 to sign up and choose 2 to login"))
                    if option_one == 1 :
                                        sign_in()
                    elif option_one == 2:
                                        login()
                    else: 
                                        print("Option is not available ")
                                        main_menu()
                    exit()
                                        
def exit ():
                    answer = str(input("Do you still want to conduct transaction?  Yes or No :"))
                    if answer == "Yes":
                                        login()
                    elif answer == "No":
                                        print("Thank you for using the application")
                    else: 
                                        print("Option is not available ")
                                        main_menu()
main_menu()

