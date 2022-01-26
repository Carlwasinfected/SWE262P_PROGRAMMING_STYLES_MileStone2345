# SWE 262P MileStones
*Team Members: [Can Wang](mailto:canw7@uci.edu), [Ruokun Xu](mailto:ruokunx@uci.edu)*

## Milestone 2

In this project, we add two overload methods at `src/main/java/org.json/XML.java`. The two method signatures are as
follows, the code starts at `line 751` and ends at `line 905`.
- `public static JSONObject toJSONObject(Reader reader, JSONPointer path) throws JSONException`
- `public static JSONObject toJSONObject(Reader reader, JSONPointer path, JSONObject replacement) throws JSONException`

The related four JUnit tests we wrote are added at `src/test/java/org.json.junit/XMLTest.java`, 
starting at `line 1069` and ending at `line1185`. The static resource files for testing are at `src/test/resources/`.
All added test cases have been already been verified correctly and the code has passed the CI process on GitHub.

Regarding the time performance, our improvement is when the user would like to query the sub Json object given a specific path,
the function will break and return early once it finishes the whole parsing process of that sub Json object, instead of
continuing until reach the very end of the whole input.

The building framework we use is `Maven`, so the build script file is `src/pom.xml`.

All four added test cases have been already been verified correctly and the code has passed the CI process on GitHub.


*PS: Thank you for reviewing our work! For any issues, feel free to contact me [here](mailto:canw7@uci.edu).        - Brs, Can*







*-----  Our README ends here-------*

---
---
---
---
---

![Json-Java logo](https://github.com/stleary/JSON-java/blob/master/images/JsonJava.png?raw=true)

<sub><sup>image credit: Ismael Pérez Ortiz</sup></sub>


JSON in Java [package org.json]
===============================

[![Maven Central](https://img.shields.io/maven-central/v/org.json/json.svg)](https://mvnrepository.com/artifact/org.json/json)

**[Click here if you just want the latest release jar file.](https://search.maven.org/remotecontent?filepath=org/json/json/20211205/json-20211205.jar)**


# Overview

[JSON](http://www.JSON.org/) is a light-weight language-independent data interchange format.

The JSON-Java package is a reference implementation that demonstrates how to parse JSON documents into Java objects and how to generate new JSON documents from the Java classes.

Project goals include:
* Reliable and consistent results
* Adherence to the JSON specification 
* Easy to build, use, and include in other projects
* No external dependencies
* Fast execution and low memory footprint
* Maintain backward compatibility
* Designed and tested to use on Java versions 1.6 - 1.11

The files in this package implement JSON encoders and decoders. The package can also convert between JSON and XML, HTTP headers, Cookies, and CDL.

The license includes this restriction: ["The software shall be used for good, not evil."](https://en.wikipedia.org/wiki/Douglas_Crockford#%22Good,_not_Evil%22) If your conscience cannot live with that, then choose a different package.

# If you would like to contribute to this project

For more information on contributions, please see [CONTRIBUTING.md](https://github.com/stleary/JSON-java/blob/master/docs/CONTRIBUTING.md)

Bug fixes, code improvements, and unit test coverage changes are welcome! Because this project is currently in the maintenance phase, the kinds of changes that can be accepted are limited. For more information, please read the [FAQ](https://github.com/stleary/JSON-java/wiki/FAQ).

# Build Instructions

The org.json package can be built from the command line, Maven, and Gradle. The unit tests can be executed from Maven, Gradle, or individually in an IDE e.g. Eclipse.
 
**Building from the command line**

*Build the class files from the package root directory src/main/java*
````
javac org/json/*.java
````

*Create the jar file in the current directory*
````
jar cf json-java.jar org/json/*.class
````

*Compile a program that uses the jar (see example code below)*
````
javac -cp .;json-java.jar Test.java (Windows)
javac -cp .:json-java.jar Test.java (Unix Systems)
````

*Test file contents*

````
import org.json.JSONObject;
public class Test {
    public static void main(String args[]){
       JSONObject jo = new JSONObject("{ \"abc\" : \"def\" }");
       System.out.println(jo.toString());
    }
}
````

*Execute the Test file*
```` 
java -cp .;json-java.jar Test (Windows)
java -cp .:json-java.jar Test (Unix Systems)
````

*Expected output*

````
{"abc":"def"}
````

 
**Tools to build the package and execute the unit tests**

Execute the test suite with Maven:
```
mvn clean test
```

Execute the test suite with Gradlew:

```
gradlew clean build test
```

# Notes

For more information, please see [NOTES.md](https://github.com/stleary/JSON-java/blob/master/docs/NOTES.md)

# Files

For more information on files, please see [FILES.md](https://github.com/stleary/JSON-java/blob/master/docs/FILES.md)

# Release history:

For the release history, please see [RELEASES.md](https://github.com/stleary/JSON-java/blob/master/docs/RELEASES.md)
