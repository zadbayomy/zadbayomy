import time
import random


def print_pause(text,seconds = 2): # function to make an interval between sentences
    print(text)
    time.sleep(seconds)


def cave(): #function to go to the cave
    global score
    score = 0
    print_pause("you choose go to the cave")
    print_pause("the cave is so dark,you shoud light the fire")
    print_pause("what is that,there are strange warnings")
    score += 1 # take a point for choose right way
    print("your score is", score)
    print_pause("choose 1 for continue")
    print_pause("choose 2 if you want return and clim moutain")
    choose = input("choose: ") 
    while choose != "1" and choose !="2":
       print_pause("please enter 1 or 2")
       choose = input("choose: ")
    if choose == "1":
        score = 0 # lose all points becouse choose wrong way
        print_pause("wow,there is a light at the end of the cave")
        print_pause("watch out for a hole")
        print_pause("you drop in it")
        print_pause("unfortunately,you lose")
        print("your score is, score")
        print_pause("do you want to play again")
        choose = input("enter yes for play again")
        while choose != "yes" and choose != "no":
            choose = input("enter yes for play again: ")
        if choose == "yes":
            play_game()
        else:
            print_pause("thanks for play")
    else:
        score -= 1 #lose point for return
        print("your score is", score)
        mountain()


def mountain():# function to go to the mountain
    global score
    print_pause("you choose go to the mountain")
    print_pause("climb the mountain carefully because there is a lot of snow")
    print_pause("that can make you fall")  
    score += 1 # take a point for choose the right way
    print("your score is", score)
    print_pause("choose 1 if you want to continue,choose 2 to go to cave")
    choose = input("choose: ")
    while choose != "1" and choose != "2":
        print_pause("please choose 1 or 2")
        choose = input("choose: ")
    if choose == "1":
        print_pause("wonderful,you reached to the top of the mountain")
        print_pause("there is a X mark that looks like a button")
        print_pause("click on it to see what happens")
        print_pause("there is a gate opens")
        print_pause("inside it there is a big treasure")
        print_pause("congratulation,you are win")
        print_pause("do you want to play again")
        choose = input("enter yes for play again: ")
        while choose != "yes" and choose != "no":
            choose = input("enter yes for play again: ")
        if choose == "yes":
            play_game()
        else:
            print_pause("thanks for play")
    else:
        score -= 1 # lose point for return to cave
        print("your score is",score)
        cave()


def lake(): # function to go to the lake
    global score
    score += 1 # get a point for go to in save way
    print_pause("you choose go to the lake,you see something in water")
    print("your score is", score)
    print_pause("choose 1 for return and go to the house")
    print_pause("choose 2 for go to see what is in the water")
    choose = input("choose: ")
    while choose != "1" and choose != "2":
        print_pause("please choose 1 or 2")
        choose = input("choose: ")
    if choose == "1":
        house()
        score -= 1 # lose point for return to house
        print("your score is", score)
    else:
        mysterious_monster = ["crocodile", "frog", "magic fish"]
        monster = random.choice(mysterious_monster)
        print("it is a huge", monster, ",you do not have any weapons")
        print_pause("unfortunately,you died") 
        score = 0 # lose all points because die
        print("your score is", score)
        print_pause("do you want to play again")
        choose = input("enter yes for play again:" )
        while choose != "yes" and choose != "no":
            choose = input("enter yes to play again: ")
        if choose == "yes":
            play_game()
        else:
            print_pause("thanks for play")


def house(): # function to go to house 
    global score
    print_pause("you choose go to the house")
    score += 1 # get a point for choose the right way
    print("your score is", score)
    print_pause("open the door,there is a sound up the stairs")
    print_pause("choose 1 for go to see what is there")
    print_pause("choose 2 for back and go to the lake")
    choose = input("choose: ")
    while choose != "1" and choose != "2":
        print_pause("please choose 1 or 2")
        choose = input("choose: ")
    if choose == "1":
        score += 1 # get point for choose the right way
        print("your score is", score)
        monsters_kinds = ["mouse", "squirrel", "hawk"]
        monster = random.choice(monsters_kinds)
        print("it is a", monster,"holding something,it is looks a map")
        print_pause("catch it,beware of being bitten")
        print_pause("well done,it is a map of a secret treasure")
        print_pause("choose 1 for follow the instructions on map")
        print_pause("choose 2 for give it up because you think it is fake")
        choose = input("choose: ")
        while choose != "1" and choose != "2":
            print_pause("please choose 1 or 2")
            choose = input("choose: ")
        if choose == "1":
            score += 1 # get a point for choose the right way
            monster = ["dinosausr", "loin", "fox"]
            creepy_monster = random.choice(monster)
            print("your score is", score)
            print_pause("the map leads you to go to a road with monsters,beware")
            print_pause("there are two ways")
            print("the frist with a" ,creepy_monster)
            print_pause("the second way with a dragon")
            print_pause("choose 1 for the frist way,2 for second way")
            choose = input("choose: ")
            while choose != "1"and choose != "2":
                print_pause("please choose 1 or 2")
                choose = input("choose: ")
            if choose == "1":
                score = 0 # lose all points for choose wrong way and die
                print("your score is",score)
                print("the" ,creepy_monster,"is hungry")
                print_pause("it will eat you")
                print_pause("unfortunatly,you lose")
                print_pause("do you wnt to play again")
                choose = input("enter yes for play again: ")
                while choose != "yes" and choose != "no":
                    choose = input("enter yes for play again: ")
                if choose == "yes":
                    play_game()
                else:
                  print_pause("thanks for play")
            else:
                score += 1 # get a point for choose the right way
                print("your score is", score)
                print_pause("the dragon is kind")
                print_pause("it will help you to reach to the treasure")
                print_pause(
                    "ride on its back let it fly with you in the amazing sky"
                )
                print_pause("you retch to huge montain")
                print_pause("there is a cave at the bottom of the mountain")
                print_pause("choose 1 for go to the cave")
                print_pause("choose 2 for clim the mountain")
                choose = input("choose: ")
                while choose != "1" and choose != "2":
                    print_pause("please choose 1 or 2")
                    choose = input("choose: ")
                if choose == "1":
                    cave()
                else:
                    mountain()
        else:
                score = 0 # lose all points becouse choose wrong way
                print("your score is", score)
                print_pause("unfortunatly,it is not fake")
                print_pause("now you lose the way to treasure")
                print_pause("you lose,you can play again")
                choose = input("enter yes to play again: ")
                while choose != "yes" and choose != "no":
                    choose = input("enter yes for play again: ")
                if choose == "yes":
                    play_game()
                else:
                    print_pause("thanks for play")
    else:
        score -= 1 # lose point for return back
        print("your score is", score)
        lake()


def play_game():
    global score
    score = 0
    print_pause("you are in the enchanted desert")
    print_pause("there is a house that seems to be old")
    print_pause("in the north there is a lake")
    print_pause("you do not have any weapons")
    print_pause("you have some food and water")
    print_pause("there are two ways and you have to choose")
    print_pause("if you a way and survive,you take a point")
    print_pause(
        "if you choose the wrong way,you will die and lose your points"
        )
    print_pause("you can play again if you want")
    print_pause("when you choose return back you lose one point")
    print("your score is", score)
    print_pause("enter (1) if you want to go to the house")
    print_pause("enter (2) if you want to go to the lake")
    choose = input("choose: ")
    while choose != "1" and choose != "2":
        print_pause("please choose 1 or 2")
        choose = input("choose: ")
    if choose == "1":
        house()
    else:
        lake()


score = 0
play_game()     
