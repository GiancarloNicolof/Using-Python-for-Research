# Case Study 06: Social Network Analysis

- **What is a path in a network?**
	> A sequence of edges connecting two nodes.

- **What is a connected component in a network?**
	> A group of nodes and their edges for which a path exists between each node in the component.

- **Consider the following code:**
	```python
	G = nx.Graph()
	G.add_nodes_from(1,2,3,4)
	G.add_edges_from((1,2), (3,4))
	G.number_of_nodes()
	G.number_of_edges()
	```
	What does this return?
	> This code contains an error.

- **How many nodes and edges are included in the karate club network (as described in Video 4.3.3)?**
	> 34 nodes, 78 edges

- **What does `G.degree(0) is G.degree()[0]` return?**
	> `True`

- **What function in `networkx` (imported as `nx`) plots a network?**
	>`nx.draw`

- **How many components do you expect in a Erdös-Rényi graph with `n=10` and `p=1`?**
	> 1

- **How many components do you expect in a Erdös-Rényi graph with `n=10` and `p=0`?**
	> 10

- **Consider the following code:**
	```python
	D = {1:1, 2:2, 3:3}
	plt.hist(D)
	```
	What will this plot?
	> This code contains an error. (Answer is outdated. plt.hist works with dictionaries)

- **How do the degree distributions in `nx.erdos_renyi_graph(100, 0.03)` and `nx.erdos_renyi_graph(100, 0.30)` compare?**
	> The latter distribution has a greater mean on average.

- **As described in Video 4.3.6, which network has more nodes?**
	> `G2`

- **As described in Video 4.3.6, which network has mode edges?**
	> `G1`

- **For an iterator object `X`, what does `X.__next__()` do?**
	> Returns the next value in `X`, if it exists.

- **For a given network `G`, what does `len(G)` return?**
	> The number of nodes.

- **Graphs `G1` and `G2` are defined as in Video 4.3.7. Which graph contains the largest connected component?**
	> `G1`

- **Graphs `G1` and `G2` are defined as in Video 4.3.7. Which graph contains the greatest fraction of its nodes in its largest connected component?**
	> `G1`