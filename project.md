Key Points:
	"Stubs and Drivers Generating Tool" is a web-application for generating stubs and drivers for unit testing.
	Stubs and Drivers works as a substitute for the missing or unavailable module in software testing process. 
	They are specifically developed, for each module, having different functionalities.
	Although, it provides ease to carry out of individual components, without concerning the availability of other modules. 
	But it is a time-consuming process, as it requires to develop dummy for each missing module.
	The tool will process a call graph to identify which classes need to create stubs or which classes need to create drivers.
	A call graph is a kind of control flow graph which shows a relationship between subroutines inside the program.


SUMMARY:
Stubs and Drivers Generation Tool is a web application in JS and PHP to automate the building of Stubs and Drivers using just UML diagrams (In specific only class and sequence diagrams). It is used to speed up unit testing of software applications. Stub is a piece of source code that acts as the class that is being called by the method (or a class) requiring to be tested. The Driver is the source code that contains hard wired inputs to stimulate the requirements of the method, calls the method to be tested and displays the output to be compared with expected output. Before the creation of the tool there were background researches done that had demerits.
The research to automate testing of a java application used a three-step process to create stub-driver but required the java source code which meant that stub and driver can’t be created until source code was written for the classes involved.  Another research provided a stub and driver pattern, after analysing the aspect-oriented program provided as input but didn’t give the method to generate the stubs and drivers. Yet another research was capable of generating a new set of test cases from an already existing one using UML diagram. The problem lies in the fact that it needs the existing test suite to be generated manually.
The tool presented in this paper can generate stubs and drivers from sequence and class diagrams inputted as XML files. It does this through the following process. A tester (a human) first inputs the XML files into the application to be stored in a database. The tool then reads the sequence diagram to identify the objects, messages and method calls. Then it proceeds to process the class diagram to find and store the packages, classes and method signatures in its database. The call graph is now created using the elements extracted from the sequence diagram, which is basically the pattern in which classes call other classes through methods. The tester chooses the classes for which the stub and driver is to be generated. He then can make the choice to use stubs generation tool which drives the application to generate stubs for mentioned classes. If these classes do not call any other classes’ methods the tool returns a warning message. Similar thing happens when the driver generation tool is clicked where drivers for required classes are generated after analysing the call graph. If the class under test is not called by methods of any other class then the tool returns a error. Final step of the process is where the app asks the user for the source code in which the stub and driver is to be generated. The user can choose to generate the stubs or the drivers. The tool also allows the modification of the stubs and drivers created in the specified language, by the user according to his needs before using it for testing.


Objective:
Generation of stubs and drivers for object-oriented program testing using class and sequence diagrams.

Features:
    • Stubs, drivers, testcases creation for testing source code written in java using symbolic execution technique.
    • Stub and driver patterns generation to support integration testing of aspect-oriented programs.
    • New test suite generation from existing test suite for improving test suite coverage.
    • Creates call graph from sequence diagram.
    • Identification and storage of objects, messages, method calls (from sequence diagram) classes, packages, method signatures (from class diagram).
    • Creation of stub source code when lower-level modules are missing/in developing stage/not developed.
    • Creation of driver source code when high level modules (sometimes even for low level ones) are not available.
    • Alerts tester by generating warning messages if tester specifies to generate stubs but the class under the test do not call any methods of another classes.
    • Alerts tester by generating warning messages if tester specifies to generate drivers but the class under the test is not called by any methods of other classes.


Support for OO paradigm:
As we know object-oriented paradigm will significantly increase the software reusability, extendibility, inter-operability, and reliability. This is true if and only if systems are tested adequately.
Use for Object oriented program testing: Driver are programs which simulate the behaviors of software components that are the control modules of a under test module. Stubs are programs which simulate the behaviors of software components that are the dependent modules of a under test module. 
Driver
Tested 
Unit
Stub

Strategies of testing for object-oriented software: - 
1. Top-Down
    • On Top-Down testing process the main control module is used as a test driver, and the stubs are substituted for all modules directly subordinate to the main control module, the subordinate stubs are replaced one at a time with actual modules. 
    • The tests are conducted as each module is integrated. On completion of each set of tests, another stub is replaced with the real module.
    •  A Top-Down approach is obviously a White Box method as in-depth knowledge of lower layers of the program's functionality is required for the generation of the stub files. 
2. Bottom-Up
    • Bottom-Up Testing works in reverse of Top-Down testing. 
    • In this process the low-level modules are combined into clusters that perform a specific software sub-function. 
    • The driver is written to coordinate test case input and output. The test cluster is tested. 
    • Drivers are removed and clusters are combined moving upward in the program structure. 
    • The advantages with this are that once a layer has been completely tested, it is less likely that any Bug found has occurred in that layer.
    

Positive points:
•	In general, during the development of any object-oriented software, it will have a lot of classes and methods which are called within the class or between different classes. So it takes quite a lot of time for creating stubs and drivers for each object and class and eventually for testing the software. So an automated testing tool is being provided which helps us a lot with testing and saves time.
•	We only need to provide class diagram and sequential diagram and respective call graph is being created and based on our choice of which class to test and source code type, stubs and drivers are automatically generated and thus it makes it simple for the tester.
•	In the previous available tools for stubs and drivers generation, even though they can be generated from the program flow but as source code is needed to determine the program flow, they cannot be generated until source code is finished but in mentioned tool, it is developed in such a way that the source code is not necessary to be finished before for stubs and drivers generation.
•	The software is developed in such a way that, A warning message will be delivered for a class under test if we choose to generate stub but that class is not calling any methods of other classes or if we choose to generate driver but that class’ methods are not being called by any other classes.
•	The tool is supporting object oriented programs developed with aspect oriented approach which aims to increase modularity.
•	An editor is also being provided to modify the generated source code so that we can add our constraints like minimum and maximum values, specify the return type, etc., to it and the tester can also export the generated source code so that it could be tested in future.
•	This software can also compare the source code to the UML diagram in XML format and use original test suite as source code template and can create new test suite with increased coverage compared to the original test suite.
Negative points:
•	As the automated test suite regeneration technique only improves the coverage of original suite by using syntax of original test suite as source code template but cannot create the test suite itself initially, we have to manually create test suite before using this tool.
•	JUnit is being used for testing the source code of generated stubs and drivers but Junit is designed to work best only for a number of small tests which may affect as the software being checked will have a lot of classes.
•	Even though concrete stubs related to abstract classes are mentioned in the research, the tool did not cover class diagrams that contain abstract and inner classes, interfaces and inheritance concepts including overriding.
•	The tool is not checking whether the sequential diagram is consistent with the class diagram or not.


PROPOSED SOLUTIONS/IMPROVEMENTS:
The paper presents a technology for generating stubs and drivers for objected oriented programs. The tool is right now capable of uploading. Class and sequence diagrams in XML and then generating the stubs and drivers. But there are some limitations like
1) our tool does not cover class diagrams that contains abstract and inner classes.
2) our tool also doesn't cover overloading and inheritance.
3)Also out tool check that whether sequence diagram is consistent with class diagram.
To overcome above limitations we can we use the following solutions:
1) We can improvise the processing of the XML files so that we consider about the abstract and inner classes also.
2)XML files should also be processed properly so that we can include overloading and inheritance in final source code.
3) We need to set up a intermediate process which checks whether class diagrams a consistent with sequence diagrams or not.


FUTURE WORKS
For the future work we can add the following features like:
1)We can enhance the feature of managing uploaded diagrams.
2)We can also set up a feature to manage generated source code.
3)We can also address the above limitations and improvise them such as considering consistency of sequence and class diagrams and also processing XML files more accurately.


Conclusion:
The process of software testing cannot be completed with incomplete components and modules. Therefore, to ensure the accuracy as well as effectiveness of testing it is vital to create "Stubs and Drivers Generating Tools". It creates stubs and drivers that fulfill the requirements of incomplete or undeveloped modules and act as pseudo modules or codes that are called in for testing the functionality of major modules. Testers can automate the unit testing without tool. It is capable for uploading sequence and class diagrams in XML file format, creating a call graph, generating stubs and drivers, editing stubs and drivers source code, and automated specifying signature values. But it has also some limitations in generating stubs and drivers from a class diagram with abstraction, inheritance,  interface class as well as overloading. It allows a tester to select only one class under test for generating them while generated drivers do not include test input values. 

