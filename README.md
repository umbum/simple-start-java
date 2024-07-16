$ mkdir -p src/main/java
$ mv HelloWorld.java src/main/java/
$ echo 'plugins {
    id("java")
}

tasks.jar {
    manifest {
        attributes(
            "Main-Class" to "HelloWorld"
        )
    }
}' > build.gradle.kts
$ echo 'rootProject.name = "simple_start"' > settings.gradle.kts
$ ./gradlew build
$ java -jar build/libs/simple_start.jar
Hello, World!