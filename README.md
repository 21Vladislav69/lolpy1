# lolpy1
#Rock, Paper, Scissors
import random
print('1/R/r is Rock   2/P/p is Paper   3/S/s is Scissors')
print('PC is your adversary, the AI')
print('User is you, the possible human')
print('Enter CLOSE to stop the program')
ba = 0
a = 0
while 1:
    tries = int(input('How many tries would you like to have? Enter here (must be an uneven number): '))
    while int(tries) % 2 != 1:
        print('The amount of tries must be an uneven number!')
        tries = int(input('How many tries would you like to have? Enter here: '))
    damn = 0
    c = 0
    k = 0
    while 1:
        User = str(input('Make your choice here:'))
        if str(User) == '1' or str(User) == 'R' or str(User) == 'r':
            User = str('1')
            PC = random.randint(1, 3)
            if int(User) == int(PC):
                print('Draw!')
            if int(PC) == 2:
                print('You lost!')
                a = a + 1
            if int(PC) == 3:
                print('You won!')
                ba = ba + 1
                a = a + 1
        if str(User) == '2' or str(User) == 'P' or str(User) == 'p':
            User = str('2')
            PC = random.randint(1, 3)
            if int(User) == int(PC):
                print('Draw!')
            if int(PC) == 3:
                print('You lost!')
                a = a + 1
            if int(PC) == 1:
                print('You won!')
                ba = ba + 1
                a = a + 1
        if str(User) == '3' or str(User) == 'S' or str(User) == 's':
            User = str('3')
            PC = random.randint(1, 3)
            if int(User) == int(PC):
                print('Draw!')
            if int(PC) == 1:
                print('You lost!')
                a = a + 1
            if int(PC) == 2:
                print('You won!')
                ba = ba + 1
                a = a + 1
        if str(User) == 'CLOSE':
            break
        if str(User) != '1' and str(User) != '2' and str(User) != '3':
            print('Only 1/2/3/R/P/S/r/p/s are allowed!')
        if a == int(tries):
            print('User: ' + str(ba) + '   PC: ' + str(int(tries) - int(ba)))
            if int(ba) < int(tries) + 1:
                print('Defeat!')
            if int(ba) >= int(tries) + 1:
                print('Victory!')
            a = 0
            ba = 0
            while 1:
                damn = str(input("Do you wish to continue? Yes or No: "))
                if damn == 'No' or damn == 'no':
                    break
                if damn == 'CLOSE':
                    break
                if damn == 'Yes' or damn == 'yes':
                    k = k + 2
                    break
                else:
                    print('The answer can only be Yes/yes/No/no!')
            if damn == 'No' or damn == 'no':
                break
            if damn == 'CLOSE':
                break
            if damn == 'Yes' or damn == 'yes':
                k = k + 2
                break
    while k == 0:
        c = str(input("Are you sure you want to quit? Yes or No:"))
        if c == 'Yes' or c == 'yes':
            k = k + 2
            break
        if c == 'No' or c == 'no':
            break
        if damn == 'No' or damn == 'no':
            k = k + 2
            break
        else:
            print('Please enter only Yes/yes/No/no!')
    if damn == 'Yes' or damn == 'yes':
        k = 0
    if k != 0:
        break
