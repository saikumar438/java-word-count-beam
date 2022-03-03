# Saikumar Mylavarapu

# java-word-count-beam
Repo for word count

## command to generate a Maven project that contains Beam’s WordCount examples
mvn archetype:generate `
 -D archetypeGroupId=org.apache.beam `
 -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
 -D archetypeVersion=2.36.0 `
 -D groupId=org.example `
 -D artifactId=word-count-beam `
 -D version="0.1" `
 -D package=org.apache.beam.examples `
 -D interactiveMode=false
 
 ## Open the directory 
 dir .\src\main\java\org\apache\beam\examples
 
 ## Run a pipeline
 mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
 -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner
