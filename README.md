# Cluster finder algorithm and Finite Size Scalling
In this code it is done the finite size scalling of the percolation 
problem. It is observed that the percolation problem is a toy model 
for second order phase transitions, this can be seen in this 
[code](https://github.com/nahumsa/Percolation). 


We will work on the Microcanonical ensemble, that means we start with
an empty grid and we occupy empty squares of the grid. We need to 
take track of the size of all clusters (Occupied squares that are 
connected) and check if a cluster percolates (If it wraps onto itself).


It is used two order parameters: 

- P_inf: Size of percolating cluster / Number of occupied cells
- Susceptibility: size of clusters squared excluding the percolating cluster

This process is divided in two parts:

1) Run an algorithm to get order parameters for various system sizes.
2) Do the finite Size Scalling analysing the data.

### 1. Find Union Algorithm
In order to get the data it is created a code that uses dictionaries for each cluster. 
This is not the optimal way to do this because it scales with (N²).
It can be implemented in different ways that speed up the code, for [example](https://arxiv.org/abs/cond-mat/0005264).
If you run the code you will create the data needed for the finite size scaling on a folder named 'Data' with subfolders
for each lattice size.

### 2. Finite Size Scalling 
If we simulated an infinite size lattice (Thermodinamic Limit) all our order parameters would be equal, but due to 
our simulation being finite they are not equal, so we need to scale our problem using our system sizes.
First it is needed to convert our data that is acquired using the microcanonical ensemble, to the canonical ensemble using the binomial distribution to do that. So after that the idea is to find those scalling parameters all methods are shown in the code.
