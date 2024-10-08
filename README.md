#task1
#Calculator
def add(a,b):
    print(a+b)
def sub(a,b):
    print(a-b)
    
def mul(a,b):
    print(a*b)
def div(a,b):
    if b != 0:
        print(a/b)
    else:
        print("0 in denominator in division gives error")    
c=add(4,3)
d=sub(10,4)
e=mul(8,9)
f=div(4,6)
#task2
#Rock Pepper scissor
import random
userscore=0
custscore=0

print("Select options:")
print("1. Rock")
print("2. Pepper")
print("3. Scissor")

while True:
    userchoice = input("Enter your selection (1: Rock, 2: Pepper, 3: Scissor): ")
    computerchoice = random.choice(["1", "2", "3"])  # Randomly selects computer choice
    print(f"Computer selected: {computerchoice}")

    if userchoice == "1" and computerchoice == "2":
        print("Pepper beats rock")
        custscore += 1
    elif userchoice == "1" and computerchoice == "3":
        print("Rock beats scissor")
        userscore += 1
    elif userchoice == "1" and computerchoice == "1":
        print("Both user and computer have entered rock")
    
    elif userchoice == "2" and computerchoice == "1":
        print("Pepper beats rock")
        userscore += 1
    elif userchoice == "2" and computerchoice == "3":
        print("Scissor beats pepper")
        custscore += 1
    elif userchoice == "2" and computerchoice == "2":
        print("Both user and computer have entered pepper")
    
    elif userchoice == "3" and computerchoice == "1":
        print("Rock beats scissor")
        custscore += 1
    elif userchoice == "3" and computerchoice == "2":
        print("Scissor beats pepper")
        userscore += 1
    elif userchoice == "3" and computerchoice == "3":
        print("Both user and computer have entered scissor")
    
    else:
        print("Enter an appropriate selection")
        continue
    
    print(f"User Score: {userscore} | Computer Score: {custscore}")
    
    # Ask if the user wants to continue playing
    play_again = input("Do you want to play again? (yes/no): ").lower()
    if play_again != "yes":
        break

# Final score
if userscore > custscore:
    print("User wins!")
elif userscore < custscore:
    print("Computer wins!")
else:
    print("It's a tie!")

print(f"Final User Score: {userscore} | Final Computer Score: {custscore}")

#task3
#password generator
n = int(input("Enter the length of password: "))  # Correct input handling
concatinate="0"
for i in range(n):  # Correct loop syntax
    passinput = input("Enter any alphabet, numeric value, or special character: ")
    concatinate+=passinput
concatinate=concatinate.replace("0", "")   
print("password generated is:",concatinate,end="\n")  # Print the input without extra \n

    


           
    
