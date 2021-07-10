Fun with xargs
--------------

All of a sudden I wanted to know the size of some binary file I know there is
this unix command called `du` that will give me the size of the file,  
eg. `du -h file`  
Output:  
`4k    file`  
but the problem is, I dont know where the file is! luckily I know one command  
called `which` that will give me the exact location of the file on the filesystem.  
eg. `which bash`  
Output: `/bin/bash`  
So I think finding the file is not really a problem. But how can I combine
these commands? It turns out there is a unix command call `xarg` how the way
it works is it standard inputs can be pass as parameter to other commands  
eg. `which bash | xargs du -h`  
Output: `720k    /bin/bash`  