# TTR-Generator
A small teaching blog to show the usablitity of the Type-Token-Ratio Measure (TTR) as an introduction to Natural Language Procesing. If you like this lesson, do star it! :) 

### This is the Solution to the coding challenge posted [here](https://rishavr.github.io/Hand-Coding-Our-Very-Own-Type-Token-Ratio-Generator/) 
 <br><Br>
<div style="text-align:center"><h1>
CODING CHALLENGE 
</h1></div>
<Br>

**STEP 1:** 

##### We will have to import our dependencies. 
For this script, we are using fantastic NLP library called [NLTK](https://www.nltk.org/). 

To install NLTK in your terminal, simply type: 

``` bash
pip install nltk 
```

We will then import nltk and  regex by 
``` python
import nltk as nlp 
import re 
```
**STEP 2:**
Declare a string containing our string for which we need to calculate the TTR. 
``` python
document="""NLP articles are fun. But they are awfully difficult to write. NLP is not difficult, but the articles, wow would awfully make you think of writing NLP Books!"""
```
**STEP 3:**
Remove all special characters using this regex.
``` python
document= re.sub(r'[^\w]', ' ', document)
```
**STEP 4:**
Convert Document to Lower Case
```
document=document.lower()
```
Tokenize the document to generate a list of words
```
tokens=nlp.word_tokenize(document)
```
**STEP 5:**
Group the tokens and find the count value of each token and store in dict types.
```
types=nlp.Counter(tokens)
```
 And finally, find the TTR by dividing the length of dict types by length of list tokens
 ```
TTR= (len(types)/len(tokens))*100
print(TTR)
```

##### And it is that simple! You can now use this simple measure to rank the quality of texts! 

##### Here is a Challenge for You:  

##### Download [This](https://github.com/RishavR/TTR-Generator/tree/master/Corpus-Collection) Corpus (Collection Of Text Files) And Compare The TTR Values Of Each Text File And Plot Them On A Sentence_Rank Vs TTR Graph like this ->

![Generated Graph](https://raw.githubusercontent.com/RishavR/TTR-Generator/master/TTRscore.png)

**You can find the solution here: [https://github.com/RishavR/TTR-Generator ](https://github.com/RishavR/TTR-Generator)**
