#Effective Network Programming in iOS7

##Bad Examples
-  Stuttering List
-  Perpetual Loader
-  Slow Loader/Front Loader

##Topics

##NSURLConnection: Original networking class
-  Invented in 2K for Safari, made public in 2K3
-  Bad seperation of settings, config, casch
-  Now replaced by NSURLSession

##NSURLSession: Class Family
-  NSURLSession
-  NSURLSessionTask
-  NSURLSessionDownloadTask
    -  provides completion data on downloads
-  NSURLSessionDataTask
    -  represents Get/Put/Post/Delete

Tableview uses the **Flywheel pattern** to make scrolling faster/easier. As cells "scroll off" the screen,, the same cell is filled with new text. It's not a new cell, it's the same set of 12 or so cells, being reconfiged. 
##[AFNetowrking](http://afnetworking.com): New library for iOS7
installed with Cocoapods via gems

##API Design tips
-  Don't expose your internal model
-  Version your API
-  send metadata as headers: OS Version, APp Versino, Device names
-  Have a way to notify (or FORCE) clients to upgrade
-  Page large datasets
-  Build-in HTTP Cacheing support from Day 1
-  Turn on GZIP compression
-  Be careful cacheing user data(I missed this one)
-  Measure (and track over time) your API response times


