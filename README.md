based on https://github.com/Netflix/zuul

- run <code>app-config</code> and <code>discovery</code> servers
- run <code>rating</code> and <code>book</code> service
- run this application  
<code>mvn spring-boot:run</code>

### Test Application
- because of gateway.properties from app-config server
<code>zuul.routes.book-service.path=/book-service/**</code>  
going to <code>http://localhost:3333/book-service/books</code>  
returns the same thing as <code>http://localhost:8083/books/</code>