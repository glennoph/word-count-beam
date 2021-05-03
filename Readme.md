# Word Count Beam example
## Background
[Apache Beam Get Started Java](https://beam.apache.org/get-started/quickstart-java/)

### Generate Code
```shell
mvn archetype:generate \
      -DarchetypeGroupId=org.apache.beam \
      -DarchetypeArtifactId=beam-sdks-java-maven-archetypes-examples \
      -DarchetypeVersion=2.29.0 \
      -DgroupId=org.example \
      -DartifactId=word-count-beam \
      -Dversion="0.1" \
      -Dpackage=org.apache.beam.examples \
      -DinteractiveMode=false
```
### Examples
[WordCount.java](./src/main/java/org/apache/beam/examples/WordCount.java)

[MinimalWordCount](src/main/java/org/apache/beam/examples/MinimalWordCount.java)

[DebuggingWordCount](src/main/java/org/apache/beam/examples/DebuggingWordCount.java)

### Run Example - WordCount.java

Build
```shell
mvn clean compile
```

Execute
```shell
mvn  exec:java -Dexec.mainClass=org.apache.beam.examples.WordCount     \
 -Dexec.args="--inputFile=in/lorem-ipsum.txt --output=out/counts" \
 -Pdirect-runner
```