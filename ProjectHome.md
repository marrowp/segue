# **Segue for R:** #
# Parallel R #
# In the cloud #
# Two lines of code! #

# Note: Segue runs on Mac or Linux. Not currently on Windows... maybe soon! #

[Pronunciation:](http://dictionary.reference.com/browse/segue) sey-gwey or seg-wey


An R language segue into parallel processing on Amazon's Web Services. Includes a parallel lapply function for the Elastic Map Reduce (EMR) engine called emrlapply(). This is NOT a map reduce project but it uses Hadoop Streaming on Amazon's EMR in order to get simple parallel computation ala cart. This is NOT a big data package. If you are CPU bound this might be a useful package. If you are IO bound, this is not the package you are looking for. Segue has a simple goal: Parallel functionality in R; two lines of code; in under 15 minutes. No shit.

If you are looking for a full map/reduce framework for R, you really should [look at Rhipe.](http://www.stat.purdue.edu/~sguha/rhipe/doc/html/index.html) Rhipe is a great resource, but with very different goals from Segue. Segue exists to allow simple parallel processing with a fast & easy setup on AWS Elastic Map Reduce. Rhipe is a general Hadoop interface for R including access to Hadoop File System.

If you already have a Rocks cluster or MPI cluster or a Magic Pony cluster, then you don't need Segue. Segue is for using Amazon's EMR to build a parallel engine for R. If you already have a cluster you should use Snow or some other tool.

To use Segue, you will need to have an Amazon Web Services account AND you will have to have the Elastic Map Reduce service activated. To see if you have the EMR service on, [just follow this link.](https://aws-portal.amazon.com/gp/aws/developer/subscription/index.html?productCode=ElasticMapReduce)

To ensure that your EMR clusters actually go away when you use stopCluster(yourCluster) you should check on their status using the [EMR Administration Dashboard from Amazon.](https://console.aws.amazon.com/elasticmapreduce/home) I'd hate you to accidentally leave machines running and get a surprise bill from Amazon!

This code is VERY alpha still. It needs more error checking and, of course, more testing. But I'm using it myself on a regular basis. If you run into any snags or have questions, comments, etc, feel free to email me: cerebralmastication at the gmail.

For an intro to Segue, Jeffry Breen [has an excellent introduction blog post](http://jeffreybreen.wordpress.com/2011/01/10/segue-r-to-amazon-elastic-mapreduce-hadoop/) where he illustrates some basic functionality of the Segue package.

The Segue project as a Google Groups page at: http://groups.google.com/group/segue-r

Special thanks to Q Ethan McCallum ( http://www.exmachinatech.net/ ) who came to this project as soon as he heard about it and has contributed ideas and code.