## 4. Spring Boot DevTools



## Installing DevTools

Add DevTools Dependency: Make sure you have the spring-boot-devtools

dependency in your pom.xml or build.gradle file.

```
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-devtools</artifactId>
<optional>true</optional>
</dependency>
```
```
After this, set the IntelliJ settings to allow restarting.
```

## IDE Configuration

1. File/Settings/Build,Execution,Deployment/Compiler

```
“Build Project automatically” (checked)
Any changes in above files will automatically build the project
```
2. File/Settings/Advanced Settings/

```
Compiler.”Allow auto-make to start even if developed” (checked)
```

## Automatic Restart

Automatically restarts the application whenever files on the
classpath change. This is faster than a full restart and only
reloads the changed parts.

Uses two class loaders: one for the base classes that don't change
(typically libraries) and another for the classes that do change
(application code). When a change is detected, only the latter is
reloaded, making the restart faster.


## Useful configurations for Dev-tools

spring.devtools.restart.enabled=false

spring.devtools.restart.exclude=static/**,public/**

spring.devtools.restart.pollInterval = 20

spring.devtools.restart.quietPeriod=



