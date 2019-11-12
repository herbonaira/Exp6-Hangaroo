# Exp6-Hangaroo
def isWordGuessed(secretWord,lettersGuessed):
    if secretWord == lettersGuessed: 
        print(list(lettersGuessed))
        return True
    else:
        print(list(lettersGuessed))
        return False
        
def getGuessedWord (secretWord, lettersGuessed):
    x = ' '
    for char in secretWord:
        if char in lettersGuessed:
            x += char
        else:
            x += '_'
    return x
    
def getAvailableLetters(lettersGuessed):
    letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
    x = list(lettersGuessed)
    for char in letters:
        if char == lettersGuessed:
            x.remove(char)
            print(x)
            
def Hangaroo(secretWord):

    mistakesMade = 0
    lettersGuessed = set()
    i = 1
    while  i == 1:
        x = input('Input letter here: ')
        while len(x) > 1 or x in lettersGuessed:
            if x in lettersGuessed:
                print('This has already been guessed - so try again!')
            else:
                print('This is not a letter! Try again!')
            imput = input('Input letter here: ')
        lettersGuessed.add(x)
        if isWordGuessed(secretWord,lettersGuessed) is True:
             print("You've Guessed it!")
             print(" ")
             print("Secret word is ", secretWord)
             mistakesMade = 0
             break
        elif isWordGuessed(secretWord, lettersGuessed) is True:
             print("mistakesMade: ",mistakesMade )
             mistakesMade += 1
             print(" ")
             print("Guess left: ")
             getGuessedWord(secretWord, lettersGuessed)
             print (" ")
             print ("Letters left: ")
             getAvailableLetters (lettersGuessed)
             print('End of the Game') 
