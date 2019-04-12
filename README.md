# Rule Based Bangla Stemmer

## Installation
    pip install py_bangla_stemmer

## Usage
    from py_bangla_stemmer import BanglaStemmer
    
    stemmer = BanglaStemmer()
    stemmer.stem('জনপ্রিয়তা')  # 'জনপ্রি'
    stemmer.stem(' সেটাই')    # 'সে'

## Rules Documentation (Only for Development)
Following documentations are for the further development of the stemmer. There is a file in 
`py_bangla_stemmer/resources` folder named `common.rules`. Bellow are the information required 
to know to change the rules.

#### `X + n :` 
When X appears at the end of a word and word length is at least n, remove it
#### `Y -> Z + n :` 
When Y appears at the end of a word and word length is at least n, replace it with Z
#### `Y.Z -> A.B + n :`
When Y, followed by some character a, followed by Z appears at the end of a word 
and word length is at least n, replace it with AaB    
