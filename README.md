11-6-2014-HW
============
def ageCheck():
    human=eval(input("\nHow old are you? "))
    if (human<12):
        return 0
    elif (12<human and human<60):
        return 12
    elif (human>60):
        return 7

def rainCheck():
    weather=input("What is the weather today?(Sunny, rainy, etc.) ")
    if weather=="rainy":
        return False
    else:
        return True
        
def idCheck():
    IDCheck=input("Do you have an ID?(yes or no) ")
    if IDCheck=="yes":
        ID=input("Give me your ID(veteran, nurse, student) ")
        ID=ID.lower()
        if(ID=="veteran"):
            return 0.6
        elif(ID=="nurse"):
            return 0.65
        elif (ID=="student"):
            return 0.7
        else:
            return 1
    else:
        return 1

def totalPrice():
    price=5    
    return ((ageCheck()+price)*idCheck())

def runMe():
    if rainCheck()==True:
        amount=eval(input("How many people are in your group? "))
        total=0
        for i in range(amount):
            total=total+totalPrice()
        print("The total price is ", "$", total,)
    else:
        print("The theater is closed today.")
