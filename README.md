# guesser by Satya Prakash Das, 02/12/2017

/*
This is a random number(between 1 to 100) guessing game written using Python
Computer will choose a random number and the user will be asked to guess the exact number.
Hint will be provided after every unsuccessful trial to help find the number
*/

import random

def main():
    print("Guess a number between 1 to 100:")
    random_number = random.randint(1,100)
    found = False
    
    while not found:
        try:
            guess_number=int(input("Guess a number:"))
        except ValueError:
            print("You must enter an integer")
        if guess_number==random_number:
            print("You got it !")
            found= True
        elif guess_number<random_number:
            print("Guess a bit higher")
        else:
            print("Guess a bit lower")
main()
