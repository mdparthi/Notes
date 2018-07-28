- static inner class
- derive abstract factory example from project
- why to make method arguments and variables as final
- immutable and mutable
- String pool
- Collections
- Streams, Lambda
- use of Annotation and how it works
- how to cache http request ( how it benefits RESTFul Webservice)

------
- https://thecuriousdev.org/achieve-thread-safety-immutability/

-------
*Design Pattern*
- Creational Pattern
  - Singleton
  - Factory Method
  - Abstract Factory
  - Builder
  - Dependency Injection

- Structural Pattern
  - Adapter Pattern
  - Decorator Pattern
  - Facade Pattern
  - Proxy Pattern  ( need to understand more example)
  
- Behavioral Pattern
  - Observer Pattern
  - Chain of Responsibility Pattern
  - Iterator Pattern
  - Strategy Pattern


*RESTful Webservice*

- expose to the internet
- it is one of the type of webservice 
- light weight , works on http
- webservice characteristics
    - browser <- client code <- webservice ( server)
    - protocol :  for RESTful is none - the data format can be xml, json, txt
    - http exchange : with any http methods there is no rule but there are recommendations
    - service definition : for SOAP it is WSDL | for REST there are no specific standard documentation 
    - SOAP webservice follows SOAP Specification | for REST there are no speification
 - REST : REpresentational state Transfer an architectural style
    - Rest follows most of the HTTP Specification
    - Hypertest conatins Hyperlinks
    - traditional    
        - eg. weartherinfo.com/weathersearch.do?pin=12345 ( it is not resource based, but it is action based)
    - Resource based uri
        - eg. weatherinfo.com/pin/12345
    - HTTP Methods
        - GET, POST, PUT, DELETE
    - Metadata
        - HTTP Status Codes ( 200 - success, 501- Internsl server, 404 - not found)
    - Format
        - xml, json, txt usually added to HTTP Header usint "content-type"
        - content negotiation ( when server responds with client request specific format )
        
