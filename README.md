This module builds an Alfresco amp which outputs log messages in a json format. This is achieved by using in log4j.properties:

```log4j.appender.Console.layout=net.logstash.log4j.JSONEventLayoutV1``` 

from the external dependency:

```('net.logstash.log4j:jsonevent-layout:1.7')```

To build the amp:

```./gradlew amp```

To start up various versions of Alfresco with this amp installed:

```./gradlew check```

Due to the healthcheck defined in the image, an unsuccessful start of Alfresco will make the check fail.
