
SUMMARY:
Stubs and Drivers Generation Tool is a web application in JS and PHP to automate the building of Stubs and Drivers using just UML diagrams (In specific only class and sequence diagrams). It is used to speed up unit testing of software applications. Stub is a piece of source code that acts as the class that is being called by the method (or a class) requiring to be tested. The Driver is the source code that contains hard wired inputs to stimulate the requirements of the method, calls the method to be tested and displays the output to be compared with expected output. Before the creation of the tool there were background researches done that had demerits.
The research to automate testing of a java application used a three-step process to create stub-driver but required the java source code which meant that stub and driver can’t be created until source code was written for the classes involved.  Another research provided a stub and driver pattern, after analysing the aspect-oriented program provided as input but didn’t give the method to generate the stubs and drivers. Yet another research was capable of generating a new set of test cases from an already existing one using UML diagram. The problem lies in the fact that it needs the existing test suite to be generated manually.
The tool presented in this paper can generate stubs and drivers from sequence and class diagrams inputted as XML files. It does this through the following process. A tester (a human) first inputs the XML files into the application to be stored in a database. The tool then reads the sequence diagram to identify the objects, messages and method calls. Then it proceeds to process the class diagram to find and store the packages, classes and method signatures in its database. The call graph is now created using the elements extracted from the sequence diagram, which is basically the pattern in which classes call other classes through methods. The tester chooses the classes for which the stub and driver is to be generated. He then can make the choice to use stubs generation tool which drives the application to generate stubs for mentioned classes. If these classes do not call any other classes’ methods the tool returns a warning message. Similar thing happens when the driver generation tool is clicked where drivers for required classes are generated after analysing the call graph. If the class under test is not called by methods of any other class then the tool returns a error. Final step of the process is where the app asks the user for the source code in which the stub and driver is to be generated. The user can choose to generate the stubs or the drivers. The tool also allows the modification of the stubs and drivers created in the specified language, by the user according to his needs before using it for testing.

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

