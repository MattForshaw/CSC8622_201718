# Day Four: JUnit 5 Example pom.xml

If you are wishing to use [JUnit 5](http://junit.org/junit5/) through Maven, please add the following `build` block to your `pom.xml` file. You can run your test within IntelliJ without this step, but this will be required in order to build and automatically run your tests using Maven on the command line.

    <?xml version="1.0" encoding="UTF-8"?>
    <project xmlns="http://maven.apache.org/POM/4.0.0"
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
        <modelVersion>4.0.0</modelVersion>

        <groupId>com.mattforshaw.csc8622</groupId>
        <artifactId>aphasia-writing</artifactId>
        <version>1.0-SNAPSHOT</version>

        <properties>
            <maven.compiler.target>9</maven.compiler.target>
            <maven.compiler.source>9</maven.compiler.source>
        </properties>

        <build>
            <plugins>
                <plugin>
                    <artifactId>maven-surefire-plugin</artifactId>
                    <version>2.19</version>
                    <dependencies>
                        <dependency>
                            <groupId>org.junit.platform</groupId>
                            <artifactId>junit-platform-surefire-provider</artifactId>
                            <version>1.0.2</version>
                        </dependency>
                        <dependency>
                            <groupId>org.junit.jupiter</groupId>
                            <artifactId>junit-jupiter-engine</artifactId>
                            <version>5.0.2</version>
                        </dependency>
                    </dependencies>
                </plugin>
            </plugins>
        </build>

        <dependencies>
            <dependency>
                <groupId>org.junit.jupiter</groupId>
                <artifactId>junit-jupiter-api</artifactId>
                <version>RELEASE</version>
            </dependency>
            <dependency>
                <groupId>org.junit.jupiter</groupId>
                <artifactId>junit-jupiter-api</artifactId>
                <version>RELEASE</version>
            </dependency>
        </dependencies>


    </project>
