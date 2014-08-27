# GLO (Graph-Level Operations)
by Charles D. Stolper, Minsuk (Brian) Kahng, Zhiyuan (Jerry) Lin, Florian Foerster, Aakash Goel, John Stasko, and Duen Horng (Polo) Chau at Georgia Tech


## What is GLO?



## Software Requirements

* You only need a modern web browser, such as Google Chrome or Firefox.
 

## How to run the prototype

### To run with Chrome:
* With command line:
```
python -m SimpleHTTPServer 8000 
(8000 will be your port number. You can use any.)
```
* Open Chrome, then connect to the following URL:
```
http://localhost:8000/gui.html
```

### To run with Firefox:
* Just open the file `gui.html` with Firefox.


## How to play with the prototype
* Choose a operation from the left pane `Select GLOs` and drag it to the next pane `Applied GLOs`.
* You will see the main view changed. 
* The bottom pane shows the history of graphs.
* For more information, see our papers in the publications section below or check out our YouTube video: https://www.youtube.com/watch?v=a7ZkZRU6VBM


## How to apply your graph data
* Create a directory in the directory `data/`
* Place two csv files into the directory you just created.
  * nodes.csv: a list of nodes with some attributes. It should include the following 3 columns:
    * id: unique identifier (integer starting with 0)
    * label: name of each node
    * modularity_class: main category (group) for nodes (integer starting with 0)
    * (optional) degree: degree of nodes
    * (optional) betweenness_centrality: betweenness centrality values of nodes
  * edges.csv: a list of edges (edges list format). It should contain 5 columns: 
    * source: source node's ID
    * target: target node's ID 
    * type: Undirected or Directed
    * id: unique identifier for edges
    * weight: weights for edges

* Replace the line 14 of the file `js/les_mis_demo.js` by 
```
var source = “YOUR_DIRECTORY_NAME”
```

## Notes
* Since all the computations are performed in client-side, we recommend to use graphs up to 1000 nodes.
* It only supports pre-defined attributes. Our current prototype does not automatically detect attributes from data.


## Publications
* GLO-STIX: Graph-Level Operations for Specifying Techniques and Interactive eXploration by Charles D. Stolper, Minsuk (Brian) Kahng, Zhiyuan (Jerry) Lin, Florian Foerster, Aakash Goel, John Stasko, and Duen Horng (Polo) Chau. IEEE Transactions on Visualization and Computer Graphics, 2014.
* GLOs: Graph-Level Operations for Exploratory Network Visualization by Charles D. Stolper, Florian Foerster, Minsuk Kahng, Zhiyuan Lin, Aakash Goel, John Stasko, and Duen Horng (Polo) Chau. 
In Proceedings of the 32nd ACM SIGCHI Conference on Human Factors in Computing Systems (CHI 2014 Extended Abstracts), pp. 1375-1380. ACM, 2014.
