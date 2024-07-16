$ javac HelloWorld.java
$ xxd HelloWorld.class
$ echo "Main-Class: HelloWorld" > MANIFEST.MF
$ jar cfm HelloWorld.jar MANIFEST.MF HelloWorld.class
$ java -jar HelloWorld.jar
Hello, World!
