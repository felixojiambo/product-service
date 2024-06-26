Product Service

Overview

Product Service is a Spring Boot application designed to manage products in an e-commerce platform. It provides a RESTful API for creating and retrieving product information. The application uses MongoDB as its database and leverages Testcontainers for integration testing.

Features

- Product Creation: Allows users to create new products with details such as name, description, and price.
- Product Retrieval: Provides an endpoint to retrieve all products stored in the database.
- Integration Testing: Utilizes Testcontainers to run integration tests with a MongoDB instance in a Docker container.

Getting Started

Prerequisites

- Java 17 or higher
- Maven 3.8 or higher
- Docker

 Running the Application

1. Clone the repository:
   ```
   git clone https://github.com/felixojiambo/product-service.git
   ```
2. Navigate to the project directory:
   ```
   cd product-service
   ```
3. Run the application:
   ```
   mvn spring-boot:run
   ```

Running Tests

To run the integration tests, execute the following command:

```
mvn test
```

This will start a MongoDB instance in a Docker container, run the tests, and then stop the container.

API Endpoints

### Create Product

- URL: `/api/product`
- Method: `POST`
- Data Params:
 - `name` (string)
 - `description` (string)
 - `price` (decimal)
- Success Response:
 - Code: `201 Created`
 - Content: `Product created successfully`

Get All Products

- URL: `/api/product`
- Method: `GET`
- Success Response:
 - Code: `200 OK`
 - Content: JSON array of products

Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you find any bugs or have suggestions for improvements.

License

This project is licensed under the MIT License. See the `LICENSE` file for details.
