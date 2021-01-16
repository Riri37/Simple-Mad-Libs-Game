# VARIATION DEFINITION. 
a      = 0.9
b      = 0.05
c      = 0.04
tbold  = '\033[1m'     # Bold Text
endc   = '\033[m'      # Reset to the defaults
import sys
import time

# INTRODUCTION OF THE GAME. 
# ADDING TYPEWRITER EFFECT FOR THE STORY. 
def intro():
    print()
    print("*" * 50)
    print()
    print()
    intro1 = "Argh! My head hurts. Wha.. What happened?"
    for character in intro1:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    print()
    intro2 = "Where am I? Where is my people??"
    for character in intro2:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    print()
    print()
    print("*" * 50)
    print()
    print()
    intro3 = (f"Hello there, welcome to the Gold Island, Captain {user_name}! \nCongratulations! You finally found us!")
    for character in intro3:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    print()
    print()
    print("*" * 50)
    print()
    print()
    intro4 = "Who's there? Who are you?"
    for character in intro4:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    print()
    print()
    print("*" * 50)
    print()
    print() 
    intro5 = "I am the guardian of this island! \nI know you and your crew are coming here \nfor gold! \nDo not worry, your crew are safe with me. \nI need you to answer three questions correctly that will lead you \nto gold. \nHowever, no man has ever managed to bring the gold home."
    for character in intro5:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    print()
    print()
    print("*" * 50)
    print()
    print()
    print(f"""{tbold}Are you brave enough to take this challenge? (Y/N): {endc}""") 
    intro6 = input("> ")
    # NESTED CONDITIONAL
    if intro6 == "n" or intro6 == "N":
        print()
        print()
        print("*" * 50)
        print()
        print()
        print("Hmmm.. We understand that not all captains are \nbrave enough to answer these. \nHere is your boat.. Please leave this island.")
        time.sleep(c)
        print()
        print()
    elif intro6 == "y" or intro6 == "Y":
        print()
        print()
        print("*" * 50)
        print()
        print()
        print(f"Great, Captain {user_name}! Then you must pass all these three questions!")
        print()
        print("May the force be with you, captain!")
        time.sleep(c)
        question_1()
    else:
        print()
        print()
        print("We can't understand you. \nHere is your boat.. You may return.")
        print()
        print()
        print("*" * 50)
        print()
    # END OF NESTED CONDITIONAL
    
# QUESTION 1. 
def question_1():
    print()
    print()
    print("*" * 50)
    print()
    print()
    question_1comment = "The gold is located up in the mountain in the middle of \nthe island. There are two paths to reach there: "
    for character in question_1comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(c)
    print()
    print("1: Jungle")
    time.sleep(c)
    print("2: Seashore")
    time.sleep(c)
    print()
    print()
    answer1 = input (f"""{tbold}Which path will you choose? (1/2): {endc}""")
    # NESTED CONDITIONAL
    if answer1 == '1':
        path_jungle()
    elif answer1 == '2':
        path_seashore()
    # END OF NESTED CONDITIONAL

# QUESTION 2.
def path_jungle():
    print()
    question_2comment = "Such a brave decision! \nHowever, jungle is full of danger! \nBe careful with mosquitos. \nThey are small but deadly. \nAlso, please be careful with wild bear. They do not like people."
    for character in question_2comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(c)
    print()
    print()
    print("Please choose one weapon you would like to take with you: ") 
    time.sleep(c)
    print("1: Mosquitos repellent")
    time.sleep(c)
    print("2: Knife")
    time.sleep(c)
    print()
    answer2 = input (f"""{tbold}Which weapon will you choose? (1/2): {endc}""")
    # NESTED CONDITIONAL
    if answer2 == '1':
        path_mosquito()
    elif answer2 == '2':
        path_knife()
    # END OF NESTED CONDITIONAL
        
# QUESTION 3.
def path_seashore():
    print()
    question_3comment = "Such a smart decision! \nHowever, seashore path will take you longer \nand night in Gold Island is super cold!"
    for character in question_3comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(c)
    print()
    print()
    print("Please choose one weapon you would like to take with you: ") 
    time.sleep(c)
    print("1: Lighter")
    time.sleep(c)
    print("2: Snake venom")
    time.sleep(c)
    print()
    answer3 = input (f"""{tbold}Which weapon will you choose? (1/2): {endc}""")
    # NESTED CONDITIONAL
    if answer3 == '1':
        path_lighter()
    elif answer3 == '2':
        path_snakevenom()
    # END OF NESTED CONDITIONAL        

# QUESTION 4.        
def path_mosquito():
    print()
    question_4comment = "Walking for hours make you tired. You decided to rest. \nWhile resting, you are applying your mosquitos repellent. \nSuddenly you see a wild bear's coming from far."
    for character in question_4comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(c)
    print()
    print()
    print("What will you do? ") 
    time.sleep(c)
    print("1: Keep moving!")
    time.sleep(c)
    print("2: Too tired! I can't run anymore.")
    time.sleep(c)
    print()
    answer4 = input (f"""{tbold}Which one will you choose? (1/2): {endc}""")
    # NESTED CONDITIONAL
    if answer4 == '1':
        path_keepmoving()
    elif answer4 == '2':
        fail()
    # END OF NESTED CONDITIONAL

# QUESTION 5.
def path_knife():
    print()
    question_5comment = "You managed to pass one night in the jungle. \nThe next morning, you get a severe fever \nand all you body is aching. It will be too hard to walk."  
    for character in question_5comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    print()
    print()
    print("What will you do?: ") 
    time.sleep(a)
    print("1: Keep moving!")
    time.sleep(a)
    print("2: Too aching! I can't walk.")
    time.sleep(a)
    print()
    answer5 = input (f"""{tbold}Which one will you choose? (1/2):{endc} """)
    # NESTED CONDITIONAL
    if answer5 == '1':
        path_keepmoving()
    elif answer5 == '2':
        fail()
    # END OF NESTED CONDITIONAL

# QUESTION 6. 
def path_lighter():
    print()
    question_6comment = "The night has come. Your lighter keeps you warm. \nBut you do not see that there is a snake coming to you. \nShe bites you and you die!"  
    for character in question_6comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
    fail()
        
# QUESTION 7.
def snake_venom(): 
    print()
    question_7comment = "The night is super cold in the shore of Gold Island. \nYou have nothing to keep you warm. \nYou can't survive the cold. You lost!"
    fail()

# FAIL FUNCTION
def fail():
    print("\nYou have failed. Here is your boat.. \nYou may return home with nothing!")
    print()
    print("Or would you like to play again? (Y/N)")
    replay = input ("> ")
    # NESTED CONDITIONAL
    if replay == "y" or replay == "Y":
        question_1()
    
    else:
        input('<Press any key to exit>\n')
    # END OF NESTED CONDITIONAL
        
# LAST QUESTION.
def path_keepmoving():
    print()
    lastquestion_1comment = "As you keep moving, \nyou finally reach the top of the mountain. \nYou see a shiny gold cave and decided to enter the cave."
    for character in lastquestion_1comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(c)
    print()
    print()
    print('*' *50)
    print()
    print()
    congrats_comment = "Congratulations, captain! \nYour gold is awaiting! \nBefore that, please answer our last question. \nWould you like to take the crew back with you? \nHowever, you can only choose between gold or your crew."
    for character in congrats_comment:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(c)
    print()
    print()
    print("What will you choose, captain?") 
    time.sleep(c)
    print()
    print("1: Gold! I've been searching for it for my whole life!")
    time.sleep(c)
    print("2: My crew! They've been with me \nsince the beginning of this expedition.")
    time.sleep(c)
    print()
    answer_last1 = input (f"""{tbold}Which one will you choose? (1/2): {endc}""")
    if answer_last1 == '1':
        path_gold()
    elif answer_last1 == '2':
        path_crew()

# ENDING OF STORY.
def path_gold():
    print()
    ending_commentgold = "You are such a greedy captain! \nYou leave people who help you come here \ntherefore I'll leave you here forever with your gold!"
    for character in ending_commentgold:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)

def path_crew():
    print()
    ending_commentcrew = "You are such a wise captain! Teamwork is all you need \nin order to achieve greater success. \nHere is your crew and please bring all the gold you want!"
    for character in ending_commentcrew:
        sys.stdout.write(character)
        sys.stdout.flush()
        time.sleep(b)
                
# BEGINNING STORY.
user_name = input(prompt = "What's your name? ")
user_name = user_name.capitalize()
print()
print()
print()
print("         |\           ")
print("         | \          ")
print("    _____|_/_____     ")
print("    \           /     ")
print("     \_________/      ")
print("~~~~~~~~~~~~~~~~~~~~~~")
print("              ~~~~~~~~~~~~~~~~~~~~~~")
print()
print()
time.sleep(a)
print("SAIL! SAIL! SAIL!")
time.sleep(a)
print()
print("Can't you hear the gold is calling us, people! \nKeep sailing!")
time.sleep(a)
print()
print("The night is too dark, captain!")
time.sleep(a) 
print()
print("We see a shadow in front of us.....")
time.sleep(a)
print()
print()
print("                                                   /\         ")
print("                                                  /  \        ")
print("                         |\                      /    \       ")
print("                         | \                    /      \      ")
print("                    _____|_/_____              /        \     ")
print("                    \           /             /          \    ")
print("                     \_________/             /            \   ")
print("         ~~~~~~~~~~~~~~~~~~~~~~             /              \  ")
print("                     ~~~~~~~~~~~~~~~~~~~~~~/                \ ")
print()
print()
print()
print("Yes! It must be the mysterious Gold Island! \nFinally we found it! , people!")
time.sleep(a)
print()
print("Oh no! It is an iceberg, captain! Our ship will hit it! \nWe go too fast!!")
time.sleep(a)
print()
print("Sharp left, people! Now!!")
time.sleep(a)
print()
print("We hit the iceberg! Our ship is sinking!!")
print()
print()
print("                                      /\         ")
print("                                     /  \        ")
print("                          |\        /    \       ")
print("                          | \      /      \      ")
print("                     _____|_/_____/        \     ")
print("                     \           /          \    ")
print("                      \_________/            \   ")
print("         ~~~~~~~~~~~~~~~~~~~~~~/              \  ")
print("                     ~~~~~~~~~/                \ ")
print()
print()
time.sleep(a)
print()
print("AHHHHHHHHH!!!!")
time.sleep(a)
print()
startGame = input(f"""{tbold}Would you like to start the game? (Y/N): """)
# NESTED CONDITIONAL.
if startGame == "n" or startGame == "N":
    print("That's too bad! The captain and crew will be a missing mystery!")
    time.sleep(c)
elif startGame == "y" or startGame == "Y":
    intro()
else:
    print("Invalid entry. Sorry we do not understand you.")
# END OF NESTED CONDITIONAL.
   


