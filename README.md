# Rock-Paper-Scissor-Project
# project using python

#Rock paper scissor game project//my firstever major project 

print("Let's start the game\n")
def playerinput():
    player="blank"
   
    
    while not( player.lower()=="r" or player.lower()=="p" or player.lower()=="s"):
        
        player=input("Hey Vaibhav..Please enter your choice among r|p|s  ")
    return player.lower()



import random
def botinput():    
    lst=["r","p","s"]
    return random.choice(lst)

def checkwinner(ply,bt):
    if ply=="r" and bt=="r":
        return "draw"
    if ply=="s" and bt=="s":
        return "draw"
    if ply=="p" and bt=="p":
        return "draw"
    if ply=="r" and bt=="p":
        return "bot"
    if ply=="r" and bt=="s":
        return "player"
    if ply=="s" and bt=="p":
        return "player"
    if ply=="s" and bt=="r":
        return "bot"
    if ply=="p" and bt=="s":
        return "bot"
    if ply=="p" and bt=="r":
        return "player"
    

def rockpaperscissor():
    end_game="n"
    player_score=0
    bot_score=0
    while end_game.lower()!="y":
        ply=playerinput()
        bt=botinput()
        print("computer entered-  ",bt)
        winner=checkwinner(ply,bt)
        
        if winner=="player":
            player_score+=2
        elif winner=="bot":
            bot_score+=2
        else:
            player_score+=1
            bot_score+=1

        print("-----SCORE BOARD----")
        print("----Player Score---- ",player_score)
        print("---- Bot Score  ---- ",bot_score)
        end_game=input("Do you want to end the game y/n- ")

    if player_score>bot_score:
        print ("Player Win...!!!!")
    elif player_score<bot_score:
        print("You lost..better luck next time")
    else:
        print("Game Draw...")


   

    


    
