# math454
note for MATH 454 Graph Theory from IIT Spring 2018

##1.1 what is graph

A graph G is a triple consisting of:

- Vertex set V(G).
- Edge set E(G).
- Endpoints.

A **loop** is a edge whose endpoints are equal.

**Multiple edge** are edges having the same pair of endpoints.

**Simple graph** $\Longleftrightarrow$ No multi edge, no loop.

$e = uv$ and here

- e is edge
- u and v are endpoints 
- we say u and v are **adjacent** and are **neighbors**
- write u $\leftrightarrow$ v for u is adjacent to v

**Complement**

**Clique** in a graph is a set of pairwise adjacent vertices

An **independent** set or stable set is a set of pairwise nonajacent vertices.

G is bipartite if V(G) can ve partited into two independent set.

**complete bipartite graph**

**Subgraph**

G is **connected** if every paris of vertices in G has a path between them

**Adjacency matrix**(#edges between two vertices)

- Witten A(G).
- Is the n-by-n matrix in which entry $a_{i,j}$ is the number of edges in G with endpoints{$v_i,v_j$}.

**Incidence matrix**(edge incidence to vertex then 1)

- Written M(G).
- Is the n-by-m matrix in which entry $m_{i,j}$ is 1 if $v_i$ is an endpoint of $e_j$ and otherwise is zero.

![幕快照 2018-03-31 14.34.0](https://ws1.sinaimg.cn/large/006tNbRwgy1fpwm75sm5dj30qq08k0ty.jpg)

**Isomorphism**

- Say G is isomorphic to H 
- Witten $G\cong H$

G is called **self-complementary** is $G\cong H$

A **decomposition** 分解一个G

**The petersen graph**

- No $C_3,C_7,C_{10}$

## 1.2 paths, cycles and trails

**1.2.2. Definition.**

- **Walk**
- **Trail**: walk with no repeated edge(vertex can be shared).
- **Path**
- **Closed path**: same endpoint 
- **Length**: the number of edges

**1.2.5. Lemma.**

Every walk contains a path.

The **components** of a G are its maximal connected subgraphs. A component is a **trivial** if it has no edges. **isolated vertex** is vtx of deg 0.

**cut-edge, cut-vtx** whose deletion can increases the number of components

**Induced subgraph**

- G induced by T
- $G[T] ~for~ G - \overline{T}$

**1.2.14. Theorem. **

- An edge is a cut-edge if and only if it belongs to no cycle.

**1.2.15. Lemma. **

- Every closed odd walk contains an odd cycle.
  - Closed even walk也不一定需要有cycle,回头重复原路返回就行了.

**1.2.8. Theorem. A graph is bipartite is and only if it has no odd cycle**

Closed trail is **circuit**, when a circuit contains all edges in the graph, this is an **Eulerian circuit**

**1.2.26. Theorem.**

 A graph G is Eulerian if and only if it has at most one nontrivial component and its vertices all have even degress.

**Lemma.**

If $\delta(G) \geqslant 2$, then G contains a cycle.

**1.2.27. Proposition.**

 Every graph w/ all even degrees decomposes into cycles.

**1.2.33. Theorem. **

For a connected nontrivail graph with exactly $2k$ vertices with odd degree, the minimum number of trails that decompose it is $max\{k,1\}$.

## 1.3. Vertex degrees and counting

- Degree.
- Max/Min degree.
- **k-regular** if the common degree is k.

The **order** of a graph G is $n(G)$, is the number of vertices in G. 

The **size ** of a graph is $e(G)$, is the number of edges in G

**1.3.3. Proposition.**

- If G is a graph,then $\sum_{v\in V(G)}d(v) = 2e(g)$

**1.3.4. Corollary.**

- Avg degree = $\frac{2e(G)}{n(G)}$
- Number of odd-degree veritces is even

**1.3.7. Definition.**

- In K-cube $Q_k$, **k-dimensional cube** or **hypercube**.


- $n(Q_k) = 2^k$
- $e(Q_k) = k\cdot2^{k-1}$

In k-regular, if X,Y are digraph  , then X = Y.

Max and Min number of edges in n-vertex edges

- Max: $.\frac{n(n - 1)}{2}$
- Min: $n - 1$ (connected n-vertex graph).

**1.3.15 **

if G is simple n-vertex graph with $\delta(G)  \geqslant (n - 1)/2 $, then G is connected, and this is sharp or be possible.

**1.3.19 Every loopless graph G has a bipartie subgraph with at least e(G)/2 edges**

H-free: It does not contain H as an induced subgraph.

**1.3.23. Mantel Theorem. **

The maximum number of edges in a n vertex triangle-free simple graph is $\lfloor n^2/4 \rfloor$.

**Degree sequence:**

- Is the list of vertex degrees, witten as $d_1 \geqslant …  \geqslant d_n$


- No negative integers .
- Sum is even.

loopless graph only if

- Sum is even
- $d_1 \leqslant \frac{1}{2}\sum_{i =1}^nd_i$

**Haven-Hakimi Thm. $d_n$是一组deg seq iff $d_n - 1$也是一组degree sequence**

- 如果减到了最后出现负数那说明全来的sequsence不能组成一个graph

## 1.4 Dericted Graph

- **Underlying subgraph**: is obtained by ignoring direction
- **Weakly connected**: if underlying graph is connected
- **Strongly connected**: $\forall(u,v) \in V^2$, there is a uv-path

Dericted graph $D$ has an Eulerian circuit iff

- $\forall v\in V(D), d^+(V) = d^-(V)$.
- $d^+(V)$ is outdegree, $d^-(V)$ is indegree.
- The underlying graph has <=1 nontrivial component.

A **circle sequence** where evey n-bit string appear exactly once

- **Orientation** of G picks a direction for each edge 
- Orientation of simple G is **oriented graph**.
- Orientation of complete G is **tournament**.
- **King** is a vertex from which every vertex is reachable by a path of lengh at most 2.

**1.4.30 Every tournament has a king**

## 1.X Complement

**1.1.7. Exercise.**

Every vertex of odd degree must be the endpoint of some path in a decomposition into path.

**1.3.5. Exercise.**

- Every graph has an even number of bertices of add degree.
- No graph of odd order is regular with odd degree.

## 2.1 Trees basic properties

- **Acyclic**: graph with no cycle
- **Forest**: an acyclic graph
- **Tree**: connected acyclic graph
- **Leaf**: degree 1 
- **Spanning subgraph**: a subgraph with vertex set V(G)
- **Spanning tree**

**2.1.3 Every tree with >= 2 vertices has >= 2 leaves. Deleting a leaf from a tree yields a tree.**

 **2.1.4 For an n-vertex graph G, the following are equivalent**

- $G$ is connected and has no cycles.
- $G$ is connected and has $n-1$ edges.
- No cycles and $n-1$ edges.
- Each u,v has one u,v-path.

**2.1.5 T is tree:**

- Every edge of a tree is a cut-edge.
- Adding one edge to a tree forms exactly one cycle.
- Every connected graph contains  a spanning tree.

**2.1.6 If T,T' are sp trees of a connected G and $e\in E(T) - E(T')$,then there is an edge $e'\in E(T')-E(T)$ such that T-e+e' is a spanning tree of G**

**2.1.6 $e(T) = k$ and $\delta(G)\geqslant k$, then $G\geqslant T$**

####Distance in trees an graph

- **Distance**: minimum length of a u,v-path, *inf* if there is no path.
- **Diameter** of G is, witten diam(G), $max_{u,v\in V(G)}d(u,v)$
- **Eccentricity** of vertex u ,written $ \epsilon(u)$, is $max_{v\in V(G)}d(u,v)$
- **Radius** is, written rad(G), is $min_{u\in V(G)}\epsilon(u)$

The **center** of G is the subgraph induced by the set of vts w/ min eccentricity. thr center can be either a vtx or edge.

**2.1.14. Theorem. **

Among trees with n vertices, $ D(T)=\sum_{u,v}d(u,v)$ is max by paths and min by stars.

**2.1.15. Lemma. **

If H is a subgraph of G, then $d_G (u,v) \leqslant d_H (u,v)$

**Cayley's formula. With vtx set [n] there are $n^{(n-2)}$ trees**

**Prufer code**

![幕快照 2018-03-31 15.05.2](https://ws4.sinaimg.cn/large/006tNbRwgy1fpwnd4az16j30a004u74c.jpg)

##2.2 spanning trees and enumeration

**2.2.8 Let $\tau(G)$ denote the number of spanning trees of a graph G. If $e\in E(G)$ is  not a loop, then $\tau(G) = \tau(G-e) + \tau(G \cdot e)$**

- 其中左边的那个是去掉e 右边那个是去掉e然后把连接e的两个vtx合并

**2.2.12  $\tau(G) = (-1)^{s+t}det~Q^*$**

![幕快照 2018-03-31 15.15.0](https://ws3.sinaimg.cn/large/006tNbRwgy1fpwnd58k4xj30hk06i74p.jpg )



- If T with m edges, then $K_{2m+1} $can be decomposed into 2m+1 copies of T
- If T is graceful then above yes
- Every T is graceful
- Graceful labeling

## 2.3 optimization and trees

**Kruskal's Algorithm - Min weighted spanning subgraph H**

- Greedy 
- 从最小的开始, 尽量连接剩下的components并缺没有C

**Dijkstra's Algotithm - finds all shortest distance from u**

## 5.1 Vertex coloring and upper bounds

**5.1.1** **Definition**.

- A **k-coloring** of a graph G is labeling $f: V(G) \rightarrow S$, where $|S| = k$(often we use $S = [k]$). 
- The labels are **colors**; the vertices of one color form a **color class**.
- A k-coloring is **proper** if adjacent vertices have different labels. 
- A graph is **k-colorable** if it has a proper k-coloring. 
- The **chromatic number** $\chi(G)$  is the leask k such that G is k-colorables.
- A graph G is **k-chromatic** if $\chi(G) = k$.
- A proper k-coloring of a k-chromatic graph is an **optimal coloring**. 
- If $\chi(H) < \chi(G) = k$ for every proper subgraph H of G, then G is **color-critical** or **k-critical**.
- The **clique number** of a graph G, $\omega(G)$, is the maximum size of a set of pairwise adajacent vertices(clique) in G.
- $\chi(G)≤\Delta(G)+1$, here the 1 can be 0 if connected with complete or odd cycle.

**5.1.7 Proposition**. For each graph G, $\chi(G) ≥ \omega(G)$ and $\chi(G) ≥ \frac{n(G)}{\alpha(G)}$.

- $\alpha(G): $ The independence number of G.
- Second formula: Each color class is an independent set and thus has at most $\alpha(G)$ vertices. 
- 这里的$\alpha(G)$指的是每个独立集中vtx的个数

**Join graph**:  "$\vee$" means make all edges between two graphs.

**5.1.9. Cartesian product**

- $G ~\square ~ H$

- $V(G~\square ~H) = V(G)~\times~V(H)$ 

  ![幕快照 2018-03-29 10.32.1](https://ws3.sinaimg.cn/large/006tNbRwgy1fpu3z2wd8pj30gw096dgr.jpg)

- **5.1.11. Proposition.** $\chi(G~\square~H) = max{\{\chi(G), \chi(H)}\}$

  **5.1.2 Greedy coloring Algorithm**

- 每个vertex从小到大编号
- 每个color从小到大编号
- 从最小的vertex开始涂色，一旦出现需要用新颜色的情况，总是用编号最小的那个颜色

**5.1.13. Proposition.** $\chi(G)≤\Delta(G) + 1$

**5.1.14. Proposition.** If a graph G has degree sequence $d_1≥…≥d_n$, then $\chi(G)≤1+ max_i~min\{d_i,i-1\}$

**5.1.22. Brooks Theorem.** If G is connected graph other than a complete graph or an odd cycle, then $\chi(G) ≤\Delta(G)$.

**Definition. Interval representation.** 

![幕快照 2018-03-29 12.03.1](https://ws3.sinaimg.cn/large/006tNbRwgy1fpu6liwj7gj30ro04qdga.jpg)

**5.1.16. Proposition.** If G is interval, then $\chi(G)=\omega(G)$

## 5.2 Structure of k-chromatic Graphs

**5.2.1. Definition. Mycielski's construction** 

- Produce a simple graph G' containing G.
- Beginning with G having vertex  set $\{v_1,…v_n\}$, add vertices $U = \{u_1,…u_n\}$
- Add edges to make $u_i$ adjacent to all of $N_G(v_i)$ 
- Let $N(\omega)=U$

![幕快照 2018-03-29 16.13.1](https://ws2.sinaimg.cn/large/006tNbRwgy1fpudt41q99j30ha050aac.jpg)

**5.2.7. Turán Graph.**

- $T_{n,r}$ is the complete r-partite graph with n vertices whose partite sets differ in size by at most 1.

**5.2.9. Turán theorem.**

- The maximum number of edges in a $K_{r+1}$-free simple n vertex graph is $e(T_{n,r})$.
- This is the general case of Mantel's theorem.


## 3.1 Matchings and Covers

**3.1.1. Definition.**

- A **matching,written as M**, is a graph H is a set a non-loop edges with no shared endpoints.
- Vertex在M内就说这个vertex is **saturated** by M.
- Otherwise **unsaturated**.
- A **perfect matching **is a graph is a matching that saturated every vertex.

**3.1.4. Definition.**

- Maximal and maximum matching(this is larger)

**3.1.6. Definition.**

- An **M-alternating path** is a path that alternates between edges in M and edges not in M.
- An M -alternating path whose enpoints are unsaturated by M is an **M-augmenting path.**

**3.1.10. Theorem. **

M is a maximum matching in G *iff* G has no M-augmenting path.

**3.1.7. Symmetric difference**.

- Matching case: $M\triangle M'= (M-M')\cup(M'-M)$
- $G\triangle H=(G\cup H)(E(G)\cap H(G))$
- 对edge去同求异

**3.1.9. Lemma**.

M, M' matching, then $M\triangle M'$ forms a disjoint union of **path** or an **even cycle**.

**3.1.11. Hall's Theorem.**

An X, Y-bigraph G has a matching that saturated X iff $|N(S)|≥|S|$ for all $S\subseteq X$.

**3.1.13. Corollary.**

For k>0, every k-regular bipartite graph has a perfect matching.

**3.1.14. Definition.**

A **vertex cover** of a graph G is a set $Q\subseteq V(G)$ that contains at least one endpoint of every edge. 

**3.1.16. Theorem.**

If G is a bipartite graph, then the maximum size of a matching in G equals the minimum size of a vertex cover of G.

**3.1.19. Definition**

An **edge cover **of G is a set L of edges such that every vertex of G is incident to some edge of L.

**3.1.20. Definition.**

- $\alpha(G) $maximum size of independent set. 
- $\alpha'(G)$ maximum size of matching.
- $\beta(G)$ minimum size of vertex cover.
- $\beta'(G)$ minimum size of edge cover.

**3.1.24. Corollary.** 

- If G is a bipartite graph with no isolated vertices then $\alpha(G)=\beta'(G)$.

##3.3 Matching in general graphs

**3.3.1. Definition.**

- A **factor** of a graph G is a spanning subgraph of G.
- **k-factor** is a spanning k-regular subgraph.
- An **odd component** of a graph is a component of odd number of vertex, the number of it is written as $o(H)$.
- **Tutten's theorem.**
  -  G has a perfect matching *iff* $\forall S\subseteq V(G), $ $|S|≥o(G-S)$.

**3.3.9. Theorem.**

Every regular graph of even degree has a 2-factor.

- **3.3.8 Corollary.** Every 3-regular graph with no cut-edge has a 1-factor.

**3.3.7. Tutte's Corollary.**

The largest number of vertices saturated by a matching in G is $min_{S\subseteq V(G)} \{n(G)-d(S)\}$, where $d(S)=o(G-S)-|S|$.

**3.3.3. Theorem.**

A graph G has a 1-factor(equals to perfect matching) *iff* $o(G-S)≤|S|$ for every $S\subseteq V(G)$.

## 3.X Complement

**Wiki.**

A connected graph is **k-edge-connected** if it remains connected whenever fewer than *k* edges are removed.

## 4.1 Cuts and connectivity

**4.1.1. Definition.**

- A **separating set or vertex cut** of graph G is a set $S\subseteq V(G)$ such that $G- S$ has more than one component.
- The **connectivity** of G, written $\kappa(G)$, is the minimum size of a vertex set S such that $G-S$ is disconnected or has only one vertex.
- A graph G is **k-connected** if  $\kappa(G)≥k$.
  - $\kappa(G)≤\delta(G)$
  - $\kappa(Q_k)=k$

**4.1.7. Definition. edge-connectivity.**

- A **disconnecting set** of edges is a set $F\subseteq E(G)$ such that $G-F$ is disconnect.
- A graph is **k-edge-connected** if every disconnecting set has at least k edges.
- The **edge-connectivity** of G, written $\kappa'(G)$, is the minimum size of a disconnecting set. This is for edges.
- **4.1.8. Remark.**
  -  Every edge is a disconnecting set.
  - Disconnecting set, NOT an edge cut.
  - Every minimal disconnecting set is an edge cut.

**4.1.9. Whitney Theorem.**

If G is a simple graph, then $\kappa(G)≤\kappa'(G)≤\delta(G)$.

**4.1.11. Theorem.**

If G is a 3-regular graph, then $\kappa(G)=\kappa'(G)$.

**Definition.**

 A **bond** is a minimal nonempty edge-cut.

**4.1.16. Definition.**

A **block** is a maximal 2-connected subgraph with no cut-vertex.

- Each cut-vtx of H is adj to each block-vertex. 
- The block-cutpoint graph is a tree if G is connected.
  - The leaf blocks of G is 1 and 5 in the given example
  - block的图和block-cutpoint的图之间可以互相转换

## 4.2 k-connected graphs

**4.2.1. Definition.**

Two u,v-path in G are **internally disjoint** if they share no interior vertex.

**4.2.2. Theorem.**

Let G have has at least 3 vertices.

- G is 2-connected $\Longleftrightarrow$ for each pair $u,v\in V(G)$ there exist inernally disjoint u,v-paths in G.

**4.2.3. Lemma.**

If G is a k-connected graph, and G' is obtained from G by adding vertex y with at least k neighbors in G, then G' is k-connected.

**4.2.4. Theorem.**

If $V(G)≥3$, the following condition are equivalent

- G is connected & has no cut-vertex.
- $\forall u,v, $ $\exist$ two interior disjoint uv-path.
- $\forall u,v, $ $\exist$ a cycle containing u&v.
- $\delta(G) ≥1$ & $\forall e,e'$ $,\exist$  a cycle containing e & e'.

**Definition.**

Given $x,y\in V(G)$, and **xy-cut** is $S\subseteq V(G)-\{x,y\}$ s.t. G-S has no xy-path.

- Let $K(x,y)$ = minimum size of an xy-cut.
- Let $\lambda(x,y)$ = maximum number of pairwise internally disjoint xy-paths.
  - Here $K(x,y) ≥ \lambda(x,y)$

**4.2.17. Menger Theorem.**

If x and y are not adjacent, then $K(x,y) = \lambda(x,y)$. 

**4.2.21. Theorem.(more general case)**

$\lambda(G)=min_{x,y}~\lambda(x,y)=K(G)​$.

- $K(G)$ - for digraph, the min #vts needed to delete to leave the graph not strongly connected.

**4.2.14. Robbins. Theorem. **

A graph has a strong orientation iff it is 2-edge-connected.

## 4.3 Network flow

**4.3.2. Definition.**

- The **value** (val(f)) of a flow $f$ is the net flow $f^-(t)-f^+(t)$ into the sink.
- A **maximum flow** is a feasible flow of maximum value.
- A **network** is a digraph with a nonnegative capacity $c(e)$ on each edge and a distinguished **source vertex** s and **sink vertex** t.
- Vertices are also called **nodes**.
- Flow $f$
- A flow is **feaible** if it satisfied the **capacity constraints** $0≤f(e)≤c(e)$
- The **conservation constraints** $f^+(v)=f^-(v)$ for each node $v\notin\{s,t\}$.

**4.3.11. Max-flow Min-cut Theorem.**

In every network, the maximum value of a feasible flow equals the minimum capacity of a source/sink cut.

**4.3.12. Intergrality Theorem.**

- If all capacities in a network are integers, then there is a maximum flow assigning integral flow to each edge.
- Furthermor, some maximum flow can be partitioned into flow of unit value along paths from source to sink.

## 6.1 Embeddings and Euler's formula

**6.1.3. Definition.**

- A graph is **planar** if it has a drawing without crossings.
- A **plane graph** is a particular planar embedding of a planar graph

**6.1.7. Definition.**

**Dual graph**

![幕快照 2018-04-19 12.05.2](https://ws4.sinaimg.cn/large/006tKfTcgy1fqigoydolvj30ge07oq3h.jpg)

**6.1.11. Definition.**

The **length** of a face $l(F)$ in a plane graph G is the total length of the closed walk(s) in G bounding the face.  饶边走

**6.1.13. Proposition.**

$\sum l(F_i) = 2e(G)$.

**6.1.21. Theorem. Euler's formula**

If a connected plane graph G has eactly n vertices, e edges and f faces, then $n-e+f=2$.

**6.1.23. Theorem.** If G is a simple planar graph with at least three vertices. then $e(G)≤3n(G)-6$. If also G is triangle-free, then $e(G)≤2n(G)-4$.

**6.1.16. Theorem**. 

G is a plane graph, TFAE:

- G is bipartite.
- Every face of G has even length $l(F_i)$.
- G* is Eulerian.

**6.1.17. Definition.**

- **Outerplane** graph is a drawing a of a graph in the plane(w/o crossing) such that all vertices lies on the **unbounded face**.

- **Theorem.** If G is outerplance, $\chi(G)≤3$.

- A plane **triangulation** is a simple plane graph where every face is a triangle $\Longleftrightarrow$ Maximal plane simple graph.


## 6.2 Characterization of Planar graphs

A **subdivision** of graph G is a graph obtained from G by a sequence of zero or more elementary subdivision.

**6.2.2 Kuratowski's Theorem.**

A graph is planar *iff* it does not contain a subdivision of $K_5$ or $K_{3,3}.$

## 6.3 Coloring of planar graph

**6.3.1. Theorem.**

Every planar graph is 5-colorable.

## 7.1 Line graph & Edge coloring

**7.1.1. Definition.**

- The **line graph** of G, written $L(G)$, is the simple graph whose vertices are the edges of G, with $ef\in E(L(G))$ when e and f have a common endpoint in G.

![ineGraph_80](https://ws1.sinaimg.cn/large/006tNc79gy1fqofdj9hyeg308q05mt8i.gif)

- A **k-edge-coloring **is $f:E(G) \rightarrow S, |S|=k$(S is colors) it is proper if incident edges received different colors.
- Edge-chromatic number = $\chi'(G) = min~k$, G has a proper k-edge-coloring.
- Fact: $\chi'(G)≥\Delta(G)$.

**7.1.7. Konig's Theorem.**

If G is bipartite , then $\chi'(G)=\Delta(G)$(Class 1).

**7.1.10. Vizing's Theorem. **

If G is a simple graph, then $\chi'(G)≤\Delta(G)+1$(Class 2).

## 7.2 Hamitonian cycles

**7.2.1. Definition.**

- A **Hamitonian cycle** is a spanning cycle.
- A **Hamitonian graph** is a graph with a spanning cycle.
- G is hamitonian $\Longrightarrow$ $\forall S\subseteq V(G)$, $components(G-S)≤|S|$.


**7.2.8. Dirac. Theorem.**

If $n(G)≥3 ~and~\delta(G)≥n(G)/2$, then G is Hamitonian.

**7.2.9. Ore. Lemma.** 

If $\forall uv\notin E(G),~d(u)+d(v)≥n$, then G is Hamitonian.

**7.2.13. Chvatal's theorem.**

Let G has degree sequence, $d_1≤d_2≤…≤d_n$, where $n≥3$, If $\forall~i<n/2$ implies that $d_i>i$ OR $d_{n-i}≥n-i$, then G is Hamilitonian.

**7.2.19. Theorem.**

- $\kappa(G) ≥ \alpha(G)$ $\rightarrow$ G is Hamiltonian(unless $G = K_2$).

**7.3.2. Tait's theorem.**

A simple 2-edge- connected 3-regular plane graph is 3-edge-colorable if and only if it is 4-face-colorable.
