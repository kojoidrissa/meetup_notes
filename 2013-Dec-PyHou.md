#2013 Dec PyHouston Meetup Notes: Python in the Cloud

##My questions for the group
-  Developing for Windows: should I get a cheap Windows laptop?
-  IronPython: If I want to see what I can do with this, do I NEED a Windows machine? What else do I need beyond [IronPython](http://ironpython.net)? Do I have to buy any .Net stuff?
    -  No, it can download it all for free! With a Windows machine

##Main presentation

###If you only remember 2(3) things!!
1.  [boto](https://github.com/boto/boto): Python interface to Amazon Web Services
2. [StarCluster](http://star.mit.edu/cluster/): an open source cluster-computing toolkit for Amazon’s Elastic Compute Cloud (EC2) released under the LGPL license
3. Prepare for failure; build in retries; decorators are great

###Hadoop
MapReduce. I need to look into this more. Also, [PyDoop](http://pydoop.sourceforge.net/docs/)

Move your computation as close to your data as possible. Lots of cloud providers also provide "Big Data". Spin up a server within that cloud and things get faster and better.
