# Project 02 - Link Searching and Community Discovery

**Due: Friday March 13, 2020 @ 11pm**

## Overview

Assume you have a graph that represents some type of relationship between two people.  For example, it could represent friendship in a social network like Facebook.  Or it could represent co-authorship of a paper, article, or book.  In these examples, we are considering the edges to be undirected. However, in social networks that have a "follow"-type relationship between two individuals, the edges would be directed.  You'll implement a set of algorithms related to searching the graph and community discovery. 

Example network input: 

```text
[7]
A
B
C
D
E
F
G
[undirected]
A - B
A - C
B - C
B - D
D - G
D - F
D - E
G - F
E - F
```

You'll read in a control file that will contain a set of commands to be processed by your project. 
* `or` - Open a file for reading.  Takes one argument - the file name. 
  * ex: `or g1.txt`
* `ow` - set the output file.  Takes one argument - the name of the file. 
  * ex: `ow g1-output.txt`
* `dfs` - Depth first search.  Takes one argument - the start node. 
  * ex: `dfs E`
  * Output: To come
* `bfs` - Breadth first search. Takes one argument - the start node.
  * ex: `bfs G`
  * Output: To come
* `mc` - Make a Connection with the smallest number of introductions.  Takes two arguments - the two people to attempt to connect. 
  * ex: `mc A D`
  * Output: A set of introductions that need to be made in order for person A to be introduced to person D.  
    * Ex: `{(A - B), (B - D)}`
* `dc` - Discover Communities.  No arguments.  Implement the [Girvan-Newman algorithm](https://en.wikipedia.org/wiki/Girvan%E2%80%93Newman_algorithm) a set of reasonably well connected communities.  You will define "reasonably". 
  * Output: a set of communities, each community identified by its members presented in alphabetic order.
  * Additional Resources on Girvan-Newman Algorithm:
    * Chapter 10 Section 2 of [Mining Massive Data Sets](http://infolab.stanford.edu/~ullman/mmds/book0n.pdf)
    * [Social and Information Network Analysis Course Slide Deck 14](http://snap.stanford.edu/class/cs224w-2010/slides/14-communities_annot.pdf)
    * Girvan M. and Newman M. E. J., [Community structure in social and biological networks](https://www.pnas.org/content/99/12/7821), Proc. Natl. Acad. Sci. USA 99, 7821–7826 (2002).  


You will need to create your CLion project in this repository as well as add in the GitHub Actions file.  Be sure to modify the CMakeLists.txt file to copy any input files to the build directory.  You can use the one from Project 01 as an example. Same goes for Actions .yaml file. 
