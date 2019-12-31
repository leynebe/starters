# java/maven

* https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html

## Maven project creation

1. Versions when created:

* mvn --version

> Apache Maven 3.6.3 (NON-CANONICAL_2019-11-27T20:26:29Z_root)
> Maven home: /opt/maven
> Java version: 1.8.0_232, vendor: Oracle Corporation, runtime: /usr/lib/jvm/java-8-openjdk/jre
> Default locale: en_US, platform encoding: UTF-8
> OS name: "linux", version: "5.4.6-arch3-1", arch: "amd64", family: "unix"

* java -version

> openjdk version "1.8.0_232"
> OpenJDK Runtime Environment (build 1.8.0_232-b09)
> OpenJDK 64-Bit Server VM (build 25.232-b09, mixed mode)

1. Create the project

`mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false`

1. Add configuration to the maven-jar-plugin in pom.xml so it knows what class to run on execution of the project.

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