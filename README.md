# Tic-Tac-Toe-Project
board = ["-","-","-","-","-","-","-","-","-"]
def display_board():
    print(board[0]+"|"+board[1]+"|"+board[2])
    print(board[3]+"|"+board[4]+"|"+board[5])
    print(board[6]+"|"+board[7]+"|"+board[8])

display_board()
poz = None

def inp_turn_x():
    global poz
    print("X's Turn.")
    poz=input('Enter the Loc to Occupy: ')

def occp_loc_x():
    global poz
    poz=int(poz)-1
    board[poz]='X'

def inp_turn_o():
    global poz
    print("O's Turn.")
    poz=input('Enter the Loc to Occupy: ')

def occp_loc_o():
    global poz
    poz=int(poz)-1
    board[poz]='O'

while "-" in board:
    while(True):
        inp_turn_o()
        if board[int(poz)-1] == "-":
            occp_loc_o()
            display_board()
            break
        else:
            print("Loc is Already Occupied.")

    while(True):
        inp_turn_x()
        if board[int(poz)-1] == "-":
            occp_loc_x()
            display_board()
            break 
        else:
            print("Loc is Already Occupied.")

    if "-" not in board:
        break

# display_board()
