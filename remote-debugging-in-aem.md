# Remote Debugging in AEM 

* Start AEM with following in JVM Parameters

```
java -Xmx2g -agentlib:jdwp=transport=dt_socket,address=5402,server=y,suspend=n -jar cq-author-p4502.jar 

```
```
-Xrunjdwp loads the JPDA reference implementation of JDWP
* transport-dt_socket is the name of the transport to use in connecting to debugger
* server=y  > means listen for a debugger application to attach
* address=5402  > means listen for a connection at this address (no host = this port on add interfaces)
* suspend=n  > means do not wait for a debugger to attach
```

* Set up Debug Configuration
** Add Java Remote Application
** Provide Project path , AEM Server location and host.
