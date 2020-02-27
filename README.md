# Deutsch-Josza Algorithm
My goal with this repository is to describe one of the projects that I have been working out and successfully replicated call the Deutsch-Joza algorithm. This was one of the first projects that I worked on after starting my focus on quantum computers. The Deutsch-Jozsa algorithm is one of the most basic but genius examples leveraging quantum technology to manufacture a computational speed up. Using the IBM Qiskit interface, I was able to replicate the circuit that would be used to create the quantum speed up proposed by David Deutsch and Richard Jozsa in 1992. Within the article, I wrote about this project and how the math behind it works. I also went into depth about some quantum computational ideas like gates and how the quantum computers are actually speeding up the processes to display the ideas of supremacy.

On this page, I want to try to explain some of the logic I used to code this project.

# The Problem
In difficult terms to understand: We are given a function f, which takes in a string of bits as input and returns either a 0 or 1. For our example, we will be using a 2 qubit string and solving the following problem instead. 
### f({x<sub>0</sub>, x<sub>1</sub>, x<sub>2</sub>,...}) → 0 or 1 , where x<sub>n</sub> is 0 or 1
The guarentee of the function is that it is either balanced or constant where constant functions returns all 0's or all 1's for any input and the balanced function returns values of 0's and 1's based on the inputs. Our task is to determine wheather the function is balanced or constant.

For a more simple explanation: The projects focus is to solve a problem proposed by these two scientists that basically described a situation where there are two types of black box funcitons. With this in mind, your goal is to try to query the black box (this means you don't know what it does) function the least amount of times as possible and find out if the function is a balanced funciton or a constant function.

We need to find out whether the function is constant or balanced. A constant function has two subsets, a function in which no matter the input, the output is 1 or 0. The first type of constant function is the 1 function. If you put in a {1, 0}, you would receive a {1, 1}. The second type of constant function is the 0 function. If you put in a {1, 0}, you would receive a {0, 0}. A balanced function has two subsets as well, both of which depend on the input. The first type of balanced function is the identity function. If you put in a {1, 0}, you would receive a {1, 0}. Your outputs are the same values as your inputs. The second subset of balanced functions is the “NOT” function. If you put in a {1, 0}, you would receive a {0, 1}. Your outputs are the opposite values of your inputs.

## The Functions
In the case of my implimentation, I created specific names for each of these seperate cases. The constant case where the outputs are in the 0 state is created by the command constant0. The user can choose which case they want by just changing the function name at the top of the code to change the type of blackbox function. Depending on the type of function that is called, there are different gates that are applied to the circuit to replicate how this black box would normally react. The constant1 command for the operator function would replicate the constant function making the outputs a 1, the balanced0 command for the operator function woudl replicate the "NOT" function creating an output that is opposite to the input and the final balanced function which is the balanced1 function would just output the exact same values as the input. 

# Implimentation of The Algorithm
I recreated this circuit in the jupyter notebook program on my computer. We are going to be creating a quantum circuit on the IBM platform through [code](https://github.com/Aryaan962/deutsch-josza-algorithm/edit/master/Python%20Code) and simulate how it would act and give results. I will be showing the simulated results and the actual results if it were to run the code on a quantum computer.

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)
