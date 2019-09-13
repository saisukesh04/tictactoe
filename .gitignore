import os

x=['#',1,2,3,4,5,6,7,8,9]

def chooseplayer(player1,player2):
    import random
    global p1,p2
    p1,p2="",""
    a=random.randint(0,1)
    if a==0:
        while True:
            p1=input(f"{player1}, choose(X/O): ")
            p1=p1.upper()
            if p1=='X' or p1=='O':
                break
            else:
                print('Choose only X or O')
                continue
    else:
        while True:
            p2=input(f"{player2}, choose(X/O): ")
            p2=p2.upper()
            if p2=='X' or p2=='O':
                break
            else:
                print('Choose only X or O')
                continue
    if p1!="":
        if p1=='X':
            p2='O'
        else:
            p2='X'
    else:
        if p2=='X':
            p1='O'
        else:
            p1='X'

def displayboard(board,player1,player2):
    os.system('cls')
    print(f'{player1} is {p1}')
    print(f'{player2} is {p2}')
    print(f"  {board[1]}  |  {board[2]}  |  {board[3]}  ")
    print('-----|-----|-----')
    print(f"  {board[4]}  |  {board[5]}  |  {board[6]}  ")
    print('-----|-----|-----')
    print(f"  {board[7]}  |  {board[8]}  |  {board[9]}  ")

def result(x):
    if x[1]==x[2]==x[3] or x[1]==x[5]==x[9] or x[1]==x[4]==x[7]:                  #x[1] is common
        print(f'{x[1]} has won')
        return 1
    elif x[3]==x[5]==x[7] or x[3]==x[6]==x[9]:                                    #x[3] is common
        print(f'{x[3]} has won')
        return 1
    elif x[4]==x[5]==x[6] or x[2]==x[5]==x[8]:                                    #x[5] is common
        print(f'{x[5]} has won')
        return 1
    elif x[7]==x[8]==x[9]:                                                        #used x[7]
        print(f'{x[7]} has won')
        return 1


player1=input('enter PLAYER 1 name:')
player1=player1.upper()
player2=input('enter PLAYER 2 name:')
player2=player2.upper()
chooseplayer(player1,player2)

displayboard(x,player1,player2)
i=1
for i in range(1,10):
    if i%2!=0:
        while True:
            y=int(input(f'{player1}, Select the location at which you want to put your symbol:'))
            if x[y]=='X' or x[y]=='O':
                print('ALREADY CHOSEN')
                continue
            else:
                x[y]=p1
                break
        displayboard(x,player1,player2)
        a=result(x)
        if a==1:
            break
            
    elif i==9:
        while True:
            y=int(input(f'{player2}, Select the location at which you want to put your symbol:'))
            if x[y]=='X' or x[y]=='O':
                print('ALREADY CHOSEN')
                continue
            else:
                x[y]=p2
                break        
        displayboard(x,player1,player2)
        a=result(x)
        if a==1:
            break
        else:
            print("It's a draw")
    
    else:
        while True:
            y=int(input(f'{player2}, Select the location at which you want to put your symbol:'))
            if x[y]=='X' or x[y]=='O':
                print('ALREADY CHOSEN')
                continue
            else:
                x[y]=p2
                break        
        displayboard(x,player1,player2)
        a=result(x)
        if a==1:
            break
            
    i+=1
