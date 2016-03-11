import random;
width=10
height=20
board=[];
numberofblocks=0;
L=0;
n=0;
for i in range(width):
    board.append(n);
while 1:
    Ldirection=random.randint(1,2);
    if Ldirection==1:
        L=random.randint(0,8);
    elif Ldirection==2:
        L=random.randint(1,9);

        if Ldirection==1:
            if board[L]>=board[L+1]:
                board[L+1]+=board[L]+1;
                board[L]+=3;
                if board[L]>height-2:
                    break;
            else:
                board[L]+=board[L+1]+3;
                board[L+1]+=board[L+1]+1;
                if board[L]>height-2:
                    break
        elif Ldirection==2:
            if board[L]>=board[L-1]:
                board[L-1]+=board[L]+1;
                board[L]+=3;
                if board[L]>height-2:
                    break;
            else:
                board[L]+=board[L-1]+3;
                board[L-1]+=board[L-1]+1;
                if board[L]>height-2:
                    break
        numberofblocks+=1;

print("Sto paixnidi kataferan na mpoun ");
print(numberofblocks);
print("kommatia");
for i in range(width):
    print(board[i]);
