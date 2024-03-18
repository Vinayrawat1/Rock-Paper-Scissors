# Rock-Paper-Scissors

import random

class RockPaperScissors:
   
    def __init__(self):
        self.choices = ['rock','paper','scissors']
    
    def get_user_choice(self):
        while True:
            user_choice = input("Enter you choice from ('rock','paper','scissors') Only!")
            if user_choice in self.choices:
                return user_choice
            else:
                print("Invalid choice! please enter your choice again!")
                
    def get_computer_choice(self):
        computer_choice = random.choice(self.choices)
        return computer_choice
    
    def determine_winner(self,user_choice,computer_choice):
        
        if user_choice == computer_choice:
            return "It Is Tie"
        elif (user_choice == 'rock' and computer_choice == 'scissors') or (user_choice == 'paper' and computer_choice == 'rock') or (user_choice == 'scissors' and computer_choice == 'paper'):
        
            return "You win!"
    
        else:
            return "computer wins!"
        
    def play_game(self):
        
        print("welcome to Rock Paper and Scissors Game!")
        
        while True:
            
            user_choice = self.get_user_choice()
            computer_choice = self.get_computer_choice()
            print("Your choice is :", user_choice)
            print("computer choice is :", computer_choice)
            
            result = self.determine_winner(user_choice,computer_choice)
            
            print(result)
            
            play_again = input("Do you want to play more ? say(yes/no)")
            
            if play_again == 'no':
                print("Okay bye, see you later : ")
                break
                
