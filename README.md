# Address Book App

A RESTful API built with Spring Boot for managing contacts.

## Tech Stack

- Java 17
- Spring Boot 4.0.3
- MySQL
- Lombok
- Maven

## Getting Started

### Prerequisites

- Java 17+
- Maven
- MySQL

### Setup

1. Clone the repository
2. Configure your database in `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/<your_db>
   spring.datasource.username=<username>
   spring.datasource.password=<password>
   ```
3. Build and run:
   ```bash
   mvn spring-boot:run
   ```

The app starts on `http://localhost:8080`.

## API Endpoints

Base URL: `/addressBook`

| Method | Endpoint       | Description          |
|--------|----------------|----------------------|
| GET    | `/addressBook`      | Get all contacts     |
| GET    | `/addressBook/{id}` | Get contact by ID    |
| POST   | `/addressBook`      | Add a new contact    |
| PUT    | `/addressBook/{id}` | Update a contact     |
| DELETE | `/addressBook/{id}` | Delete a contact     |

## Contact Model

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "address": "123 Main St",
  "city": "Springfield",
  "state": "IL",
  "zip": "62701",
  "phoneNumber": "555-1234",
  "email": "john.doe@example.com"
}
```

## Project Structure

```
src/main/java/com/example/demo/
├── controller/   AddressBookController.java
├── model/        Contact.java
├── service/      AddressBookService.java
└── AddressBookApplication.java
```
