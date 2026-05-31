<div align = "center">
  <h1>Scramble Game</h1>
  <p>*********</p>
</div>

<div>
<details>
<summary>Click here to see python code</summary>  
  
```python
import random

u_name = input("Username: ")
print(f"Welcome {u_name.capitalize()}, to the Scramble Game")
word_list = ['caramel', 'yellow', 'entangle', 'aramaic', 'interventionism']

def scramble_word(word):
    length = len(word)
    word_scrambled = ''.join(random.sample(word, length))
    return word_scrambled
    
gameOn = True
while gameOn:
    rand_index = random.randrange(0,len(word_list))
    correct_word = word_list[rand_index]
    game_word = scramble_word(word_list[rand_index])
        
    tries = 3
    
    print('\nReady...')
    print(f'Your word is {game_word}\n')
    
    while tries > 0:
        ans = input()
        if ans == correct_word:
            print('Correct')
            tries = 0
            gameOn = False
        else:
            tries -= 1
            print('Wrong answer. Try again')
    else:
        print('Game over')
        gameOn = False
        break
```
</div>
