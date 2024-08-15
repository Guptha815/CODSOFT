# CODSOFT
# ROCK PAPER SCISSORS GAME CODE IS AS FOLLOWS
   
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

