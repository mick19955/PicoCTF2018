Problem Description:
```
Using netcat (nc) will be a necessity throughout your adventure. Can you connect to 2018shell.picoctf.com at port 36356 to get the flag?
```

So we are given an URL and a port number. A great tool to connect to any webservice is Netcat, just as the problem states

Its possible to connect to the service throught netcat with the following command 
```
nc 2018shell.picoctf.com 36356
```

The following will be displayed
```
That wasn't so hard was it?
picoCTF{NEtcat_iS_a_NEcESSiTy_9454f3e0}
```
And then the connection closes, but we got our flag.


