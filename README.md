# CODSOFT
This repository totally consists of the tasks I have done in codsoft internship programme.
1. ROCK PAPER SCISSORS GAME CODE IS AS FOLLOWS
   
import random

rock = '''  
    _______
---'   ____)  
      (_____)  
      (_____)  
      (____)
---.__(___)  
'''

paper = '''  
    _______
---'   ____)____  
          ______)  
          _______)  
         _______)
---.__________)  
'''

scissors = '''  
    _______
---'   ____)____  
          ______)  
       __________)  
      (____)
---.__(___)  
'''
 
game_images = [rock, paper, scissors]
 
user_choice = int(input(  
    "What do you choose? Type 0 for Rock, 1 for Paper, 2 for scissor. \n => "))

print("User Choice: ")    

print(game_images[user_choice])

computer_chocie = random.randint(0, 2)

print("Computer Choice: ")
 
print(game_images[computer_chocie])
 
 
if computer_chocie > user_choice:  
    print("You lose. ☠")  
elif user_choice > computer_chocie:  
    print("You win!🎉 ")  
elif computer_chocie == user_choice:  
    print("It's a draw.")  
elif user_choice >= 3 or user_choice < 0:  
    print("You typed an invalid number, You Lose.  ☠") 

2.PASSWORD GENGRATOR

import random


letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u',
           'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P',
           'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the Password Generator!")
print("How many letters would you like in your password?")
n_letters = int(input("> "))
print("How many symbols would you like?")
n_symbols = int(input("> "))
print("How many numbers would you like?")
n_numbers = int(input("> "))

hard_level = True

blueprint = []

if n_letters > 0:
    for i in range(n_letters):
        blueprint.append("l")
        
if n_symbols > 0:
    for i in range(n_symbols):
        blueprint.append("s")

if n_numbers > 0:
    for i in range(n_numbers):
        blueprint.append("n")

if hard_level:
    random.shuffle(blueprint)

password = ""
for placeholder in blueprint:
    if placeholder == "l":
        password += random.choice(letters)
    elif placeholder == "s":
        password += random.choice(symbols)
    elif placeholder == "n":
        password += random.choice(numbers)

if len(password) > 0:
    print(f"Your password will be: {password}")
else:
    print("You need to choose at least 1 character to generate a password.")
