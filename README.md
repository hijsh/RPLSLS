# RPLSLS
Rock-paper-scissors-lizard-Spock Game for Python


# The key idea of this program is to equate the strings
# "rock", "paper", "scissors", "lizard", "Spock" to numbers
# as follows:
#
# 0 - rock
# 1 - Spock
# 2 - paper
# 3 - lizard
# 4 - scissors

# helper functions
import random
def name_to_number(name):
    if name=='rock':
        return 0
    elif name=='Spock':
        return 1
    elif name=='paper':
        return 2
    elif name=='lizard':
        return 3
    elif name=='scissors':
        return 4
    else :
        return 'You have wrong spelling'

def number_to_name(number):
    if number== 0:
        return 'rock'
    elif number== 1:
        return 'Spock'
    elif number== 2:
        return 'paper'
    elif number== 3:
        return 'lizard'
    elif number== 4:
        return 'scissors'
    else :
        return 'You have wrong number'
    
def rpsls(player_choice): 
    print 'Player chooses ', player_choice
    player_number = name_to_number(player_choice)
    comp_number = random.randrange(0,5)
    comp_choice = number_to_name(comp_number)
    print 'Compuer chooses ', comp_choice    
    difference = int(player_number - comp_number)
    # compute difference of comp_number and player_number
    if (difference > 0 and difference <3) or difference < -2 :
       print 'Player wins!'
    elif difference == 0 :
       print 'Player and computer tie!'
    else :
       print 'Computer wins!'
    # determine winner, print winner message
    print '\n'
    
# test your code - THESE CALLS MUST BE PRESENT IN YOUR SUBMITTED CODE
rpsls("rock")
rpsls("Spock")
rpsls("paper")
rpsls("lizard")
rpsls("scissors")



