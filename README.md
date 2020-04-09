# Override port in Spring Cloud with system property

when ConfigServerApplication is started, config is available at (this is in module cloud-config)
```
http://localhost:7777/random-port-default.yml
```

if RandomPortApplication is started with e.g. (this is in module random-port-service)
```
-Dserver.port=60066
```
the random port from Config is overridden

It is important to note that `spring.cloud.config.override-system-properties=false` needs to be in a property source returned from config server.