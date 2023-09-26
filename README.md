# Rock-paper-scissors-game
import random
score = 0
while(1):
	print("score : " +str(score))
	selection = input("1- rock \n2- paper \n3- scissor \n")
	selection = int(selection)
	if selection == 0 : 
		break
	if (selection != 1) and (selection != 2) and (selection != 3):
		print("the input is invalid")
		break
	systemselection = random.randint(1,3)
	systemselectionstring = ""
	if systemselection == 1 : systemselectionstring = "rock"
	elif systemselection == 2 : systemselectionstring = "paper"
	elif systemselection == 3 : systemselectionstring = "scissor"
	print("systemselection : "+ systemselectionstring)
	if(systemselection == 1 and selection == 2) or (systemselection == 2 and selection == 3) or (systemselection == 3 and selection == 1):
		print("you win!!!")
		score+=1
	elif systemselection == selection :
		print("equal !!")
	else :
		print("you lost !!!")
		score-=1
	print("\n\n") 
