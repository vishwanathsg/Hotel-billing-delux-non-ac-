# Hotel-billing-delux-non-ac-
This code calculates the bill for a hotel, and includes food bill, tip on the bill as well as GST

def billing(user):
    while True:
        try:
            room_type=str(input("What is the type of room? (type specifically 'delux' or 'non ac'): "))
            days_spent=int(input("Number of days after checking-in: "))
            food_bill=float(input("Total expenditure on food: "))
            break
        except:
            print("Invalid input, please try again")
    print()
    if room_type==("delux"):
        print("Room Tarrif for",days_spent,"days =",7500*(days_spent),"INR")
        print("Total food bill (incl. 10% tip + 18% GST)=",(round(food_bill + food_bill*0.10 + food_bill*0.18,2)),"INR")
        print("10% tip=",(round(food_bill*0.10,2)),"\n18% GST:\n9% CGST=",(round(food_bill*0.09,2)),"\n9% SGST=",(round(food_bill*0.09,2)))
    elif room_type==("non ac"):
        print("Room Tarrif for", days_spent,"days =", 4500*(days_spent),"INR")
        print("Total food bill (incl. 10% tip + 5% GST)=", (round(food_bill + food_bill*0.10 + food_bill*0.05, 2)),"INR")
        print("10% tip=", (round(food_bill * 0.10, 2)), "\n5% GST:\n2.5% CGST=", (round(food_bill * 0.025, 2)),"\n2.5% SGST=", (round(food_bill * 0.025, 2)))
user1="John Doe"
billing(user1)
