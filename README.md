# CI Jenkins Maven Demo

A small Java Maven project created for a DevOps/Jenkins Continuous Integration lab.

## What it does
The application demonstrates a simple `add()` method:
- `2 + 3 = 5`
- JUnit automatically tests that the result is correct.

## Build
Requires Java 21 and Maven.

```bash
mvn -B clean verify
```

The build creates a JAR in `target/`.

## Run
After building:

```bash
java -cp target/ci-jenkins-maven-demo-1.0-SNAPSHOT.jar com.example.App
```

## Jenkins
Use a Jenkins Freestyle project:
- Git repository: this repository
- Branch: `*/main`
- Build step: Execute Windows batch command
- Command: `mvn -B clean verify`
- Archive artifacts: `target/*.jar`
