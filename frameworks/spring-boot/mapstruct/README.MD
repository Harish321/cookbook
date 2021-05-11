Map struct library helps to create mapper interface 

type : 
    Interface


maven-dependency:
    ```<dependency>
			<groupId>org.mapstruct</groupId>
			<artifactId>mapstruct</artifactId>
			<version>1.3.1.Final</version> 
	    </dependency>```


maven-plugin:
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.5.1</version>
            <configuration>
                <source>1.8</source>
                <target>1.8</target>
                <annotationProcessorPaths>
                    <path>
                        <groupId>org.mapstruct</groupId>
                        <artifactId>mapstruct-processor</artifactId>
                        <version>1.3.1.Final</version>
                    </path>
                    <path>
                        <groupId>org.projectlombok</groupId>
                        <artifactId>lombok</artifactId>
                        <version>1.18.4</version>
                    </path>
                </annotationProcessorPaths>
            </configuration>
        </plugin>



annotations:

    1. @Mapper
        - This annotaions goes on the interface declarion, this helps spring to consider this interface as map struct interface and mapstruct-processor uses this annotation to generate implementation class at compile time / run time
    
    2. @Mappings
        - This annotaion goes on top of the method inside interface, This is a collection annotaion to hold @Mapping annotations Ex : @Mappings({ @Mapping(xxxxxx)}).

    3. @Mapping
        - This annotation goes on top of the mrthid inside interface, or inside @Mappings annotation as an entry, this annotation helps to define custom binidings for traget and source i.e different propery in target can be mapped to different propery in source.
         Ex : @Mapping(source="somekey",target="someotherkey")



Examples :
1. Defining

2. Usage
