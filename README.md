# Safari Rush Hour Cluster Dataset

This repository contains a dataset of clusters for the game Safari Rush Hour. Clusters were obtained as integer values obtained from a random uniform distribution as integers, unranked into a set of rows and columns and solved through Iterative Deepening A* with Transposition Tables (IDA*+TT) or Retrograde Analysis.

## Contents

**idastar_seed_11111.csv** - A list of 56,541 clusters, solved by iterating through all of their boards and running IDA*+TT.
**idastar_seed_22222.csv** - A list of 34,527 clusters, solved by iterating through all of their boards and running IDA*+TT.
**retrograde_seed_11111.csv** - A list of 162,324 clusters, solved through Retrograde Analysis.
**retrograde_seed_22222.csv** - A list of 169,228 clusters, solved through Retrograde Analysis.

## How to read the data

The data comes in .csv format with the character **;** being used as the delimitator. The files contain six columns of information, explained below.

### Cluster identifier

The identifier consists of two parts, a *hexadecimal number* and a *decimal digit*, separated by the character **_**. 

The hexadecimal number corresponds to the distribution of pieces along the rows and columns. The unranked form can be obtained by converting the number from hexadecimal to a base-6 number, which results in 14 digits. 

Each one of the digits of this number corresponds to the distribution of a row and column.
+ 0 corresponds to an empty row or column.
+ 1 corresponds to a row and column with one 3x1 piece.
+ 2 corresponds to a row and column with one 3x1 piece and a 2x1 piece.
+ 3 corresponds to a row and column with one 2x1 piece and one 3x1 piece.
+ 4 corresponds to a row and column with one 2x1 piece.
+ 5 corresponds to a row and column with two 2x1 pieces.

The decimal digit corresponds to the number of 2x2 pieces that are **not** the rover present in the boards within the cluster.

### Legal
This is a binary variable describing if a cluster is legal or not.

## Dataset Information

Clusters were obtained randomly as integer values from an uniform distribution.

There are in total 331,552 clusters in this dataset. 
321,428 of the clusters in this dataset exceed the number of pieces in the physical version of the game or cannot be physically constructed due to overlapping pieces, marked as illegal. 
2,608 of the clusters in this dataset do not have at least one board within it that has a solution.
7,516 of the clusters in this dataset were legal and has at least one board with in that has a solution.

