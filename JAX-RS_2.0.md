# What is REST ?
* REST Representational state transfer
* URL + HTTP verb + HTTP body = REST
* Resources are usually represented in JSON (You can also use XML, JSON is used much more)

# Request Types -> CRUD

* CREATE -> POST
* READ -> GET
* UPDATE -> PUT
* DELETE -> DELETE

# HATEOAS (Pronounce: හෙයිටොස්)
* Hypermedia As The Engine Of Application State
* Dynamically navigate the rest API
* Response to a certain resource may provide links to more related resources
* Not standardized
* Supported by JAX-RS

# JAX-RS 2.0
* JavaEE 7
* POJOs exposed as web services
* Mappings, Annotations, ...
* Higher level than HttpURLConnection
* Asnyc client and server processing
* Natural integration with business logic
* No blocking on requests
* Provider extensions (Entity, Context, Exception mapping)
* Filters and interceptors
* Extensive API ::: JSR 339
* Bean validation

# Maven
* Manage project dependencies
* Cargo plug-in -> Handle deployment
* `mvn clean package cargo:run`

# Bookshop REST Service
```
POST   /books               - Create a book from HTTP Payload
POST   /books/:isbn         - Create a book with given ISBN + HTTP Payload
GET    /books               - Read all the books
GET    /books/:isbn         - Only the book with given ISBN is returned
PUT    /books/:isbn         - Update
DELETE /books/:isbn         - Delete
GET    /books/:isbn/authors - Get authors for given book
GET    /authors             - Get all authors
```

# URLs
```
localhost:8081/rest-server/api/books
--------------
    Domain
	         -----------
	         Context Root
	                      ----
	                     Base URL
	                           --------
	                           Resource  
	  
```

