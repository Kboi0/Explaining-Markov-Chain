# Explaining-the-Markov-Chain
## Tutorial Overview
This tuorial will give you a basic understanding of the Markov Chain model and show you an example of it being used in a c++ text generator.
## What is a Markov Chain?
Named after the Russian Mathematician, Andrey Markov, a Markov Chain is a stochastic model that describes a sequence of possible events, but the probability of each event is dependent only on the state attained in the previous event. 
# How Does it Work?
## At the Base Level
Given some number of states, each state has a percentage chance to change to 0 or more other states. Usually you get these starting percentages from actual data and then use them to generate data of similar types.
## Regarding the Example
### Methodology
First the program will analyze the text we give it, keeping track of each word it finds, what comes after that word, and how many times that word came next.  
  
When analyzing the poem “The Road Not Taken” by Robert Frost, here are the words that come after “and” and their frequency:
  
Sorry 	-1  
Be 	    -1   
Looked 	-1   
Having 	-1  
Wanted  -1  
Both 	  -1   
Ages 	  -1   
I 	    -1  
That 	  -1    
  
    
After all the counts are gathered up, they are then converted to probabilities by dividing the count of each word by the total sum of words found.   
  
Sorry 	11%  
Be 	    11%  
Looked  11%  
Having 	11%  
Wanted  11%  
Both 	  11%   
Ages 	  11%   
I 	    11%  
That 	  11%  
  
Now that the probabilities are known, the program can start to generate text. The first thing it does is pick a word purely at random, having it serve as the first word in the text.  
  
Then, using the probabilities of which words come after that word, it chooses the next word. This repeats until as long as desired.
### Implementation  
Utilizing arrays, vactors, maps, and hashing, the code sample provided consists of many parts. The sample is based on Github User: Atrix256's implementation.
#### Learning Stage
Here we count the words in our data and their frequency, afterward turning them into cumulative probablilities.
#### Data Generation Stage
Selects a random starting state, then chooses the next state using weighted options. 
#### File Output
This is where the program reads the file into memory and performs the operation, generating both an output file and a statistics file. 

# How is it Useful?
I have only demonstrated a small bit of what Markov Chains are capable of. The nature of the model allows for many things to be considered when applying it to the real world. 
  
Other applications are as follows:  
Make an ai that plays games such as Chutes and Ladders, or Tic Tac Toe  
An ai that solves mazes  
Extrapolate probabilities in Thermodynamics  
Markov Chains make up a significant portion of the study of Quantum Mechanics  
Hidden Markov Chains are used in Bioinformatics, like speech recognition  
Economic studies.   
# Further Reading
See the Markov Chain text generator in your favorite language:  
https://rosettacode.org/wiki/Markov_chain_text_generator  
  
  The math heavy side of things:  
https://brilliant.org/wiki/markov-chains/  
  
  Find  definitions and the history of the Markov Chain model and its creator here:
https://en.wikipedia.org/wiki/Markov_chain  
  
  A wonderful series of graphics that illustrate the Markov Chain model:  
https://setosa.io/ev/markov-chains/  
  
This code sample is what this tutorial is based on. I felt it offered a lot of information about the Markov Chain model and also included cool features such as statistics for whatever documemnt you want to use:  
https://github.com/Atrix256/TextMarkovChain 




