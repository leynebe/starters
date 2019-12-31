# java/maven

* https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html

## Maven project creation

1. Create the project

`mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false`

2. Add configuration to the maven-jar-plugin in pom.xml so it knows what class to run on execution of the project.

```
<configuration>
	<archive>
		<manifest>
			<addClasspath>true</addClasspath>
			<classpathPrefix>lib/</classpathPrefix>
			<mainClass>com.mycompany.app.App</mainClass>
		</manifest>
	</archive>
</configuration>
```