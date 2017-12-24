# README #

This README would normally document whatever steps are necessary to get your application up and running.

### What is this project for? ###

The project contains APIs that can be used to hash various data types in Java. This project contains different hashing functions like xxHash, FarmHash, CityHash and MurmurHash3.

### How do I get set up? ###

Open the project in IntelliJ IDE, Open tool windows for Gradle and SBT (it can be accessed via view --> Tool Windows).

* Dependencies - junit (4.12), guava (18.0/19.0) 
* SBT compile can be done by following ways:

	1. Using 'compile' command under SBT Task in Tool Windows
	2. Creating a new configuartion (Run --> Edit Configuration --> '+' --> SBT--> 'compile' / 'clean compile' as task)
	
* Gradle build can be done by following ways:
	1. Using 'build' command under Gradle Task in Tool Windows
	2. Creating a new configuartion (Run --> Edit Configuration --> '+' --> Gradle --> 'build' / 'clean build' as task) 
	3. Right click on build.gradle and select Run 'build'
* Tests can be run by following ways:
	1. By right clicking on the test folder (under src/test) and select Run 'All Tests'
	2. Creating a new configuartion (Run --> Edit Configuration --> + Gradle/SBT--> 'clean test' as task)
	
### Eclipse AST ###

How to run the project:

1. Run the java file / zero-allocation-hashing /src/main/java/eclipse/ast/parser/ASTParserClass.java by right clicking on the java file and selecting Run 'ASTParserClass.main()'
2. Back up of all the java files will be created in this path /zero-allocation-hashing/src/main/old_java/
3. Execution of this main class creates the AST and the AST is parsed and various visitors are written in this class, through this every node will be visited.
4. After Execution of the above main class instrumentation statements are added in the java classes that are in /zero-allocation-hashing/src/main/java/net/openhft/hashing
5. After instrumentation this code, Gradle Script can be run by Right click on build.gradle and select Run 'build' or by Creating a new configuartion (Run --> Edit Configuration --> '+' --> Gradle --> 'build' / 'clean build' as task)
6. Test cases can be executed by right clicking on the zero-allocation-hashing/src/test/java/net/openhft/hashing/net/openhft/hashing/ and by selecting Run 'All Tests' or by Creating a new configuartion (Run --> Edit Configuration --> + Gradle--> 'clean test' as task)
7. The Trace File will be created in zero-allocation-hashing/TraceFile.txt

### Contribution guidelines ###

New java files added:

* ASTParserClass.java 
* CreateBackup.java 
* CreateInstrumStmt.java 
* InstrumentationTemplate.java 
* ExpressionParametersDaoImpl.java

### Contribution guidelines ###

* Additonal 3 test (classes) have been added:

1. HashValCompareTest.java :- To test whether the hash values obtained using various hashing methods using the same keys is unique and different
2. XxHashArrayCollisionTest.java :- To test whether the hash values of the elements in the two arrays (hashes of hexadecimal numbers multiplied by different numbers ) are same or different
3. xxHashSeqValTest.java :- To test whether the hash value is not null when the input string is empty.
