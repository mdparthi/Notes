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
        - simply evnet driven as links makes the respective call
    - Resource based uri
        - eg. weatherinfo.com/pin/12345
        - consumer of rest api has to know the uri's
    - HTTP Methods : GET, POST, PUT, DELETE, HEAD, POSITIONS
    - Metadata
        - HTTP Status Codes ( 200 - success, 501- Internsl server, 404 - not found)
    - Format
        - xml, json, txt usually added to HTTP Header usint "content-type"
        - content negotiation ( when server responds with client request specific format )
    - Designing of messenger application
    - Resource uri's ( instance uri's & collection uri's)
        - instance uri's has unique id's
        - common uri entities (eg. /messages/{messageId}, /profiles/{profileId}) first level entity
        - best practise : think of resource as a static calls , nouns in the resources
        - resource relations ( messages and comments) 
        - eg. /messages/{messageId}/comments/{commentId} /messages/1/comments/2 second level entity
     - Collection Uri's
        - /messages, /messages/{messageId}/comments  ( all messages and all comments)
        - filter or paginate : /messages?offset=30&limit=10 ( standard way to provide filer is using query params)
        - filter : /messages?year=2014&offset=30&limit=10
     - HTTP Methods 
        - /getMessages.do?id=10 is action based not like Restful /messages/10
        - Use right http method for the right operation
     - Idempotence
        - GET : read only | nothing happens for multiple request and it is safe
        - PUT,POST,DELETE : write | most of the time it can be called multiple times
        - eg. count = 100; though we repeat it does not make any change
        - Repeatable Operation ( GET, DELETE eg. deleting a message (/message/id ,  same with PUT) are IDEMPOTENT
        - Non-Repeatable Operation ( POST eg. multiple call may create duplicate information) are NOT IDEMPOTENT
     - HTTP Response 
        - HTTP Content, Response ( xml, json)
        
     - Richardson Maturity Model
        - Level 0 (Swamp of POX)
            - One URI for all the operations
            - Request body contains all the details 
        - Level 1
            - Resource URI per message , per profile
        - Level 2
            - Using different HTTP Methods and status codes accordingly
        - Level 3
            - Implementing the HATEOAS ( Response has links that client can use)
     - JaxRs ( Jersey, RESTeasy, RESTlet)
        - contains interfaces and annotations from the package javax.ws.rs
        - Jersey is the Reference Implementation
        
            
