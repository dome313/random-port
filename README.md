# Cannot override port in Spring Cloud with system property

when ConfigServerApplication is started, config is available at 
```
http://localhost:7777/random-port-default.yml
```

if RandomPortApplication is started with e.g.
```
-Dserver.port=60066
```
the random port from Config is not overridden