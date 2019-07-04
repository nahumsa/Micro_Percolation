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
In order to get the data

### ⋅⋅1




