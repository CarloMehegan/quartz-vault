Tags: #flashcards #notes #LING220
Created: Friday, Mar 4
[[International Phonetic Alphabet (IPA)]]

# Syntax I
Phrase structure rules 
-> (ps) rules
Phrase structure grammar

Making models


### Lexical and Phrasal Categories
##### lexical categories
also called parts of speech
different languages have different lexical categories
looking specifically at English lexical categories
the following set is not exhaustive

1. determiner (abbrev. DET)
- come before nouns
- ex. "the" "a" "this" "that"
- not an open category

2. nouns (N)
- open category
	- can invent new nouns
- structurally can tell something is a noun differently from how we conceptually tell something is a noun
	- structurally, nouns can be made plural, can be replaced with pronouns

3. adjectives (ADJ)
- open category
- structurally, is capable of coming between a determiner and a noun
	- ex. "the reddish pen"
	- "reddish" is the adjective and goes between "the" and "pen"
- structurally, can be made comparative or superlative
	- "redder" "reddest" "the most red"

4. verbs (V)
- "every language has verbs"
- open category
- structurally, <mark style="background: #FFB8EBA6;">missed one lol</mark> 
- structurally, can be put in past tense

5. preposition (P)
- ex. "on" "by" "around"
- to test if a word is a preposition
	- "right ___ the corner"
	- "right ___ determinant noun"

There are likely more lexical categories in English that we will come across

##### phrasal categories
built around a single word, called "the head" of the phrase
1. Noun Phrase (NP)
	- a noun is the head of the phrase
2. Prepositional Phrase (PP)
	- preposition head
3. Verb Phrase (VP)
	- verb head
4. Sentences (S)

--- 

"a woman walked the little dog down the street"
we can agree this is an English sentence
can we figure out how sentences are put together and write rules for sentences using this sentence?

### Constituency
Constituents of a sentence are the parts of a sentence
"Constituents are strings of closely related words"

Looking at: "a woman walked the little dog down the street"
What are the constituents?

DET  N          V      DET ADJ  N      P     DET   N
"a woman walked the little dog down the street"

##### constituent tests
1. Substitution test
If we can replace a group of words with one word, then we know that is a closely related string of words. There are different kinds of substitution:
- Pronoun replacement
	- ex. replace "the little dog" with "him"
	- "a woman walked him down the street"
	- this shows that "the little dog" is a constituent
	- we can see that "little" is more related to "dog" than it is related to "down", for example

- "Prepositional proform" replacement
	- this just means replacing "there" and "then"
	- want to try and stretch the substitution for as many words as possible to find a constituent
	- ex. replace "down the street" with "there"
	- "a woman walked the little dog there"
	- this is as far as you can stretch the substitution without changing the meaning
	- "a woman walked there" would change the meaning too much
	- "a woman walked the little dog down there" can still stretch the substitution farther

- "do so" "did so" replacement
	- ex. replace "walked the little dog down the street" with "did so"
	- "a woman did so"
	- this is as far as you can stretch the subtitution without changing the meaning


2. Movement test
Try moving a group of words to the front of the sentence in order to find constituents
- ex. move "down the street" to the front
- "down the street, a woman walked the little dog"
- ex. move "the little dog"
- "the little dog, the woman walked down the street"
- these sentences could exist in a conversation
- if the second example does not feel right to a listener, we can still see that "the little dog" is a constituent from the pronoun replacement test


3. Wh? test
Ask a "who, what, when, where" question, and the answer is a constituent
- ex. "who walked the little dog down the street?"
	- a woman
- ex. "a woman walked what down the street?"
	- the little dog
- ex. "a woman walked the little dog where?"
	- down the street
- The answer is exactly what was substituted


Now, we analyze these constituents and their relations in order to make rules


### Phrase Structure Rules
How are these phrases put together? What rules allow a speaker to generate these phrases?
Parentheses means optional

##### NP - Noun Phrases
- (Determinant) - (Adjective) - Noun
- Determinant before the noun
- If there's an adjective, it goes between the determinant and noun
- Determinants and adjectives are both optional, could be just a noun in a noun phrase

##### PP - Prepositional Phrases
- Preposition - (Determinant) - (Adjective) - (Noun)
- aka Preposition - Noun Phrase
- We can show how these phrases enclose each other

##### VP - Verb Phrases
- Verb - (Noun Phrase) - (Prepositional Phrase)
- Only verb is essential but the optional parts are used in this order

##### S - Sentence
- Noun Phrase - Verb Phrase

##### Summary:
NP -> (Det) (Adj) N (PP)
PP -> P NP
VP -> V NP PP
S -> NP VP

##### TREE 
- A tree diagram aka a syntax tree
- Lines should be straight and come to points
- Tree drawn out on paper handout



---
### Flashcards
- 


### Related Topics
- Next: [[Syntax II]]



### Intangibles (to be rewritten)
-Missed the first parts of class need to fill that in and check google drive notes


DET  N          V      DET ADJ  N      P     DET   N
"a woman walked the little dog down the street"
remember to write this out!!!!

- add picture of tree drawn on handout

- during syntax II notes found that NP are not just
	- NP -> (Det) (Adj) N
- they can be
	- NP -> (Det) (Adj) N (PP)
- these rules will be revised again later