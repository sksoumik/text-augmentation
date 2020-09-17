# text-augmentation

The codes have been adapted and slightly modified from [this](https://github.com/jasonwei20/eda_nlp) repositiory. 

## Augmentation Techniques
 - Synonym replacement
 - Random deletion
 - Random word swap
 - Random word insertion

## Installation

    $ git clone git@github.com:sksoumik/text-augmentation.git
    $ cd text-augmentation
    $ pip install -U nltk
    $ python
    >>> import nltk; nltk.download('wordnet')

## Directory Structure of The Project
```
.
├── data
└── src
```

Place the data in the `data/` directory in the following formet in a `.txt` file: 

    1   neil burger here succeeded in making the mystery of four decades back the springboard for a more immediate mystery in the present 
    0   it is a visual rorschach test and i must have failed 
    0   the only way to tolerate this insipid brutally clueless film might be with a large dose of painkillers

## Run the project

Let's say, 
 - Your input data file name is `input_data.txt`
  - You want to save the augmented data in a file called `output.txt`,
  - You want `15` augmented data for each line/text sentence.
  - You can also specify the alpha parameter, which approximately means the percent of words in the sentence that will be changed      
(default    is    `0.1` or `10%`)  
Then, run the following command: 

<br/>

    $ python src/data_augmentation.py --input=data/input_data.txt --output=data/output.txt --num_aug=15 --alpha=0.05


