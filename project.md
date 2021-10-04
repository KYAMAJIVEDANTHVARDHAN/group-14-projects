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
