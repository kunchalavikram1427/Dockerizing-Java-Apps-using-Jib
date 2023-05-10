# Sample Maven Application


## Using Jib

### Using inline commands
For Jar Packaging
```
mvn compile com.google.cloud.tools:jib-maven-plugin:3.3.1:build -Djib.to.auth.username=<USERNAME>  -Djib.to.auth.password=<PASSWORD/TOKEN> -Dimage=<IMAGE_NAME>
```
For WAR Packaging
```
mvn package com.google.cloud.tools:jib-maven-plugin:3.3.1:build -Djib.to.auth.username=<USERNAME>  -Djib.to.auth.password=<PASSWORD/TOKEN> -Dimage=<IMAGE_NAME>
```

### Using Plugins in POM file
```
<project>
  ...
  <build>
    <plugins>
      ...
      <plugin>
        <groupId>com.google.cloud.tools</groupId>
        <artifactId>jib-maven-plugin</artifactId>
        <version>3.3.1</version>
        <configuration>
          <to>
            <image>myimage</image>
          </to>
        </configuration>
      </plugin>
      ...
    </plugins>
  </build>
  ...
</project>


```


### References
- https://cloud.google.com/blog/products/application-development/introducing-jib-build-java-docker-images-better
- https://github.com/GoogleContainerTools/jib
- https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin#quickstart
- https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin#authentication-methods
- https://maven.apache.org/
- https://maven.apache.org/pom.html
- https://maven.apache.org/settings.html
- https://github.com/GoogleContainerTools/jib/issues/3214
