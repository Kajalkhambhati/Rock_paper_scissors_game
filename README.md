# Rock_paper_scissors_game
import random
rock='''
    --------
---'    _ _ _)
       (_ _ _ )
       (_ _ _ _)
       (_ _ _ )
----._ _(_ _ )
'''
paper='''
     ----------
----'     _ _ _)_ _ _
          _ _ __ _ _ )
          _ _ __ _ _ _)
          _ _ __ _ _)
----._ _ __ _ __ _)      

'''
scissors='''
     -----------
-----      _ _ _)_ _ _ _
                _ _ _ _ _)
           _ _ __ _ __ _ _)
          (_ _ _ _)
----._ _ _(_ _ _)           

'''
game_image=[rock,paper,scissors]
user_choice=int(input("Enter your choice:type 0 for rock 1 for paper 2 for scssors."))
if user_choice>=3 or user_choice<0:
    print("Enter number is invalid,you Lose")
else:    
    print(game_image[user_choice])
    computer_choice=random.randint(0,2)
    print("Computer choice:")
    print(game_image[computer_choice])
    if computer_choice==user_choice:
        print("It's draw")
    elif computer_choice==0 and user_choice==2:
        print("you lose")             
    elif user_choice==0 and computer_choice==2:
        print("you Win")    
    elif computer_choice>user_choice:
        print("You lose")
    elif user_choice>computer_choice:
        print("you Win")             
