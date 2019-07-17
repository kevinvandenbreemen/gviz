[![Pub Package](https://img.shields.io/pub/v/gviz.svg)](https://pub.dartlang.org/packages/gviz)
[![Build Status](https://travis-ci.org/kevmoo/gviz.svg?branch=master)](https://travis-ci.org/kevmoo/gviz)

A simple Dart package for writing
[GraphViz](http://www.graphviz.org/)
[dot files](http://www.graphviz.org/doc/info/lang.html).

# Example Tasks with Graphs
## Add a Sub-graph

```
GViz graph = GViz();
Gviz subGraph = Gviz(name: 'SG');   //  Needs to have a name other than parent graph
subGraph
..addNode('A')
..addNode('B')
..addNode('C');

subGraph
..addEdge('A', 'B')
..addEdge('B', 'C')
..addEdge('C', 'A');

graph.addSubgraph(subGraph);
graph.addEdge('1', 'A');
```

