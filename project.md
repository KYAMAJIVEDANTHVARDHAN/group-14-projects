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
...
Objective:
Generation of stubs and drivers for object-oriented program testing using class and sequence diagrams.

Features:
Stubs, drivers, testcases creation for testing source code written in java using symbolic execution technique.
Stub and driver patterns generation to support integration testing of aspect-oriented programs.
New test suite generation from existing test suite for improving test suite coverage.
Creates call graph from sequence diagram.
Identification and storage of objects, messages, method calls (from sequence diagram) classes, packages, method signatures (from class diagram).
Creation of stub source code when lower-level modules are missing/in developing stage/not developed.
Creation of driver source code when high level modules (sometimes even for low level ones) are not available.
Alerts tester by generating warning messages if tester specifies to generate stubs but the class under the test do not call any methods of another classes.
Alerts tester by generating warning messages if tester specifies to generate drivers but the class under the test is not called by any methods of other classes.


Support for OO paradigm:
As we know object-oriented paradigm will significantly increase the software reusability, extendibility, inter-operability, and reliability. This is true if and only if systems are tested adequately.
Use for Object oriented program testing: Driver are programs which simulate the behaviors of software components that are the control modules of a under test module. Stubs are programs which simulate the behaviors of software components that are the dependent modules of a under test module. 
Driver	Tested 
Unit	Stub

Strategies of testing for object-oriented software: - 
1. Top-Down
On Top-Down testing process the main control module is used as a test driver, and the stubs are substituted for all modules directly subordinate to the main control module, the subordinate stubs are replaced one at a time with actual modules. 
The tests are conducted as each module is integrated. On completion of each set of tests, another stub is replaced with the real module.
 A Top-Down approach is obviously a White Box method as in-depth knowledge of lower layers of the program's functionality is required for the generation of the stub files. 
2. Bottom-Up
Bottom-Up Testing works in reverse of Top-Down testing. 
In this process the low-level modules are combined into clusters that perform a specific software sub-function. 
The driver is written to coordinate test case input and output. The test cluster is tested. 
Drivers are removed and clusters are combined moving upward in the program structure. 
The advantages with this are that once a layer has been completely tested, it is less likely that any Bug found has occurred in that layer.
