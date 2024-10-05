import time
import os
from termcolor import colored

quotes = [
    ('Steve Jobs', "Everyone here has the sense that right now is one of those moments when we are influencing the future."),
    ('Bill Gates', "Don’t compare yourself with anyone in this world. If you do so, you are insulting yourself."),
    ('Linus Torvalds', "Talk is cheap. Show me the code."),
    ('Mark Zuckerberg', "The biggest risk is not taking any risk. In a world that is changing really quickly, the only strategy that is guaranteed to fail is not taking risks."),
    ('Grace Hopper', "The most dangerous phrase in the language is, 'We’ve always done it this way.'"),
    ('Dennis Ritchie', "The only way to learn a new programming language is by writing programs in it."),
    ('James Gosling', "If you think it's simple, then you have misunderstood the problem.")
]

def print_artistic_quote(author, quote):
    os.system('cls' if os.name == 'nt' else 'clear')
    for char in colored(f"--- {author} ---", 'yellow', attrs=['bold']):
        print(char, end='', flush=True)
        time.sleep(0.05)
    print() 
    for char in colored(quote, 'cyan'):
        print(char, end='', flush=True) 
        time.sleep(0.05)
    print("\n")

for author, quote in quotes:
    print_artistic_quote(author, quote)
    time.sleep(2)
