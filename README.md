import random as r
num = r.randint(1, 100)
guesses = 1
try :
    while num != 0:
        guess = int(input("Enter a number between 1 and 100: "))
    
        if guess < num and guess >= 1:
            print(f"Higher number please")
            guesses += 1    
        elif guess > num and guess <= 100:
            print(f"Lower number please")
            guesses += 1    
        elif guess == num:
            print(f"You win! and the number is {num}. You took {guesses} guesses.")
            break
        else:
            print("Invalid input, try again.")
except ValueError:
    print("Please enter a valid integer.")
