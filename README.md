📚 Book CRUD API – Spring Boot

A simple RESTful API built with Spring Boot that allows you to manage books — Create, Read, Update, and Delete (CRUD) operations.
Perfect for learning Spring Boot, JPA, and REST API development.

🚀 Features

➕ Add a new book
📖 Get all books
🔍 Get a book by ID
✏ Update book details
❌ Delete a book

🛠️ Tech Stack

Java 17+
Spring Boot 3+
Spring Data JPA
Hibernate
MySQL (or H2 for in-memory testing)
Maven

📂 Project Structure
Book-CRUD-API/
│── src/main/java/com/example/demo/
│   ├── controller/   # API endpoints
│   ├── model/        # Book entity
│   ├── repository/   # JPA repository interface
│   ├── service/      # Business logic
│   └── BookCrudApiApplication.java  # Main class
│
│── src/main/resources/
│   ├── application.properties  # Database config
│
└── pom.xml

⚙️ Setup & Run

1️⃣ Clone the Repository

git clone https://github.com/lokeshh301/SpringBoot_API.git

cd SpringBoot_API

2️⃣ Configure Database (MySQL)

src/main/resources/application.properties: properties

spring.datasource.url=jdbc:mysql://localhost:3306/bookdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
(For testing, you can switch to H2 in-memory DB)

3️⃣ Build & Run

mvn spring-boot:run

🔗 API Endpoints

GET	/api/books	Get all books	-
GET	/api/books/{id}	Get book by ID	-
POST	/api/books	Add a new book	{ "title": "Book Name", "author": "Author Name", "price": 9.99 }
PUT	/api/books/{id}	Update a book	{ "title": "Updated Title", "author": "Updated Author", "price": 12.99 }
DELETE	/api/books/{id}	Delete a book	-

🧪 Testing


Use Postman or cURL to test endpoints.

Example:
curl -X GET http://localhost:8080/api/books

📜 License
This project is licensed under the MIT License – feel free to use and modify it.

💡 Author
Lokeshkumar
