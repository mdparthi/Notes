- static inner class
- serialization
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
- https://www.javaworld.com/article/2072752/the-java-serialization-algorithm-revealed.html
- https://www.mkyong.com/java/java-custom-annotations-example/

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
    - Hypertext conatins Hyperlinks
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
        - Headers and Message Body
        - Headers : Message Length, Data, Content Type
     - Status Codes
        - 200 : OK , 404 : Not Found, starts from 100 to 599
        - Code starts with 1xx : Information , 2xx : Success, 200 : OK, 201 : Created, 204 : No Content
        - 3xx : Redirects , 302 : Found, 307 : Temp Redirect, 304 : Not Modified
        - 4xx : Client Error, 400 : Bad Request, 401 - UnAutorized, 403 - Forbidden, 404 : Not Found , 415 - Unsuported media type
        - 5xx : Server Errror, 500:Internal Server Error, 
     - HATEOAS : Hypermedia As The Engine Of Application State
        - similar to hyperlinks to navigate to different page
        - for Restful webservice we can include the additoinal uri's in the response
        - eg. { commentUri : "/messages/10/comments" }
        - or { href : "messages/1" }
        - rel (relational) attribute 
        - add new property to json called " links " 
        
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
        
 *Lambda Expression*
    - Functional Programming
    - Anonymous class
    - Type Inference
        
            
