# Densest Subgraph

Implementation of the "Densest Subgraph in streaming" algorithm using python.

The algorithm retrieves an approximation of the densest subgraph in a graph defined in a file.

### Algorithm description:

Input : 

	file containing the graph (G) description_ each line of the file contains an edge in the format int,int

	approximation parameter epsilon

Output:  file containing the densest graph approximation

Definitions:

	* H := densest subgraph retrieved so far

	* rho(X) := average degree density of the graph X defined as the numberEdges/numberNodes

	* degree of a node is the number of edges incident to that node

Algo  : 

	* H = G

	* while ( G contains at least one edge )

		remove from G all nodes with degree <= 2*(1+epsilon)rho(G)

		if rho(G) > rho(H): H=G

	* return H
