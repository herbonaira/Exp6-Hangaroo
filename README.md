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
