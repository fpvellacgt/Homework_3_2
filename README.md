# Homework_3_2

import pandas as pd

p=pd.read_csv("pokemon.csv")

team=[]

#pandas check for specific input being present or not
#p.loc[p['identifier']=='bulbasaur'].empty

while True:
    n=input("What would you like to do:\n\n\t1) Add teammate\n\t2) Exit\n\t3) manage: Team\n\n\input: ")
    if int(n)==1:
        t=input("Who is your teamate: ")
        if len(team) == 3:
            print("Too many teammates")
            continue
        elif p.loc[p['identifier']==t].empty:
            print("Invalid Pokemon")
            continue
        team.append(t)
        print(team)
        #print(len(team))
    if int(n)==3:
        p=input("what would you like to do:\n\nt3) Change")
    if int(n)==2:
        # print("change")
        team.sort(reverse=True)
        old=team.index("squirtle")
        e=team.pop(old)
        print(e)
        team.insert(2,e)
        print(team.sort())
    if int(n)==2:
        print("world")
        break

# In console, type: p.sample(n=5)['identifier'] 
# This is in order to see a list of variables from yhr Pokemon lists. 
# Add .tolist() for complete list of certain variables. 
# Also print team, and team.sort() and to.list() 

# In console, also type in for strings and integers: list.sort()
    # For whole list print "list" in console. 
    # sorted(team,key=operator.itemgetter('id))
    # [x in list['name'] for x in team]
p=pd.read_csv("data/pokemon.csv")

# In console: g.loc[g['pokemon_id']==3].shape(20,3)
# g.loc[g['pokemon_id']==3].shape[0] It returns 20. 
# g.loc[g['pokemon_id']==3].shape[0] Returns 20. 

##### Manage option new user functions. #####

# Next, we will add new options for the manage options. 
# At this time, we will allow the user to generate a random team. 

n=input("Generate your own team\n\t3") # if this does not work, it may be needed to 
# Be moved to the main code. 

#Next, we will create a function to allow users to move team members if necessary. 
#Along with, deleting them from the list. 
