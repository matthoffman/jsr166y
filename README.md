jsr166y
=======

A fork of [Doug Lea's jsr166y library](http://gee.cs.oswego.edu/cgi-bin/viewcvs.cgi/) with _very_ minor modifications in support of distributed fork-join algorithms.

Modifications: 

1.) I changed the package, to prevent confusion (and so it can load in Java 7+ JDKs cleanly)
   I used my name to make it clear who had munged Doug Lea's perfectly good library; hopefully no one sees it as 
   taking any form of undue credit. 

2.) I made the "fork()" method in ForkJoinTask non-final. 
   One way of bolting multi-node distribution onto FJ is to extend ForkJoinTask, and do something clever and 
   distributed when forking a new task.  There are other options, of course, but making that method non-final makes
   that particular option possible.


