# BillingApp 💸

![BillingApp](https://img.shields.io/badge/BillingApp-v1.0-blue)  
BillingApp is a robust and user-friendly application designed to simplify billing and invoicing. Built with Spring Boot and React, it enables users to create, manage, and track invoices, handle customer data, and maintain product inventory. Ideal for small businesses, freelancers, or anyone seeking an efficient billing solution.

## ✨ Features

- **Invoice Generation** 📄: Create professional invoices with customizable templates.
- **Customer Management** 👥: Easily store and manage customer information.
- **Product Inventory** 📦: Track products with pricing and stock details.
- **Bill Tracking** ✅: Monitor paid and unpaid invoices with status updates.
- **Export Options** 📤: Download invoices as PDF or share via email.
- **Responsive Interface** 🎨: Seamless experience across devices with React.

## 🛠️ Tech Stack

- **Frontend**: React ⚛️, Tailwind CSS 🎨
- **Backend**: Spring Boot 🌱, Java ☕, Lombok 🛠️
- **Database**: MySQL 🗄️
- **Other Tools**: Maven 📦, Git 🗃️, Postman 📬

## 📋 Entities

The application is built around the following core entities:

- **Customer** 👤
  - `id`: Unique identifier (Long)
  - `name`: Customer's full name (String)
  - `email`: Customer's email address (String)
  - `phone`: Contact number (String)
  - `address`: Billing address (String)

- **Product** 📦
  - `id`: Unique identifier (Long)
  - `name`: Product name (String)
  - `price`: Unit price (Double)
  - `stock`: Available quantity (Integer)
  - `description`: Product details (String)

- **Invoice** 📝
  - `id`: Unique identifier (Long)
  - `customerId`: Reference to Customer (Long)
  - `products`: List of Product IDs and quantities (List)
  - `total`: Total amount (Double)
  - `status`: Paid, Unpaid, or Pending (Enum)
  - `createdAt`: Invoice creation date (LocalDateTime)

## 🌐 API Endpoints

Key API endpoints for interacting with the application (served under `/api/v1`):

| **Method** | **Endpoint**                    | **Description**                        |
|------------|---------------------------------|----------------------------------------|
| GET        | `/api/v1/customers`             | Retrieve all customers                 |
| POST       | `/api/v1/customers`             | Create a new customer                  |
| GET        | `/api/v1/customers/{id}`        | Get customer by ID                     |
| PUT        | `/api/v1/customers/{id}`        | Update customer details                |
| DELETE     | `/api/v1/customers/{id}`        | Delete a customer                      |
| GET        | `/api/v1/products`              | Retrieve all products                  |
| POST       | `/api/v1/products`              | Create a new product                   |
| GET        | `/api/v1/products/{id}`         | Get product by ID                      |
| PUT        | `/api/v1/products/{id}`         | Update product details                 |
| DELETE     | `/api/v1/products/{id}`         | Delete a product                       |
| GET        | `/api/v1/invoices`              | Retrieve all invoices                  |
| POST       | `/api/v1/invoices`              | Create a new invoice                   |
| GET        | `/api/v1/invoices/{id}`         | Get invoice by ID                      |
| PUT        | `/api/v1/invoices/{id}`         | Update invoice details                 |
| DELETE     | `/api/v1/invoices/{id}`         | Delete an invoice                      |

## 🚀 Installation

Follow these steps to set up the project locally:

1. **Prerequisites**:
   - Java 17+ ☕
   - Node.js 18+ 📦
   - MySQL 8.0+ 🗄️
   - Maven 📦

2. **Clone the Repository**:
   ```bash
   git clone https://github.com/GURUPRASATH-OG/BillingApp.git
   cd BillingApp
   ```

3. **Set Up the Backend**:
   - Navigate to the backend directory (e.g., `backend`):
     ```bash
     cd backend
     ```
   - Configure MySQL:
     - Create a database named `billingapp`.
     - Update `src/main/resources/application.properties` with your MySQL credentials:
       ```properties
       spring.datasource.url=jdbc:mysql://localhost:3306/billingapp
       spring.datasource.username=your_username
       spring.datasource.password=your_password
       spring.jpa.hibernate.ddl-auto=update
       ```
   - Build and run the Spring Boot application:
     ```bash
     mvn clean install
     mvn spring-boot:run
     ```

4. **Set Up the Frontend**:
   - Navigate to the frontend directory (e.g., `frontend`):
     ```bash
     cd frontend
     ```
   - Install dependencies and start the React app:
     ```bash
     npm install
     npm start
     ```

5. **Access the Application**:
   - Backend API: `http://localhost:8080/api/v1`
   - Frontend: `http://localhost:3000`

## 🎮 Usage

1. **Create an Invoice** 📝:
   - Navigate to the "Invoices" section in the React frontend.
   - Click "New Invoice," select a customer, and add products.
   - Save or export the invoice as a PDF.

2. **Manage Customers** 👥:
   - Add or edit customers in the "Customers" section.
   - View customer details for quick reference.

3. **Track Inventory** 📦:
   - Manage products in the "Products" section.
   - Update stock levels and pricing as needed.

## 🏗️ Project Structure

- **Backend** (Spring Boot):
  - `entity`: JPA entities (e.g., Customer, Product, Invoice)
  - `dto`: Data Transfer Objects for API requests/responses
  - `mapper`: Mapping between entities and DTOs
  - `repository`: Spring Data JPA repositories
  - `service`: Business logic and service layers
  - `controller`: REST API controllers
  - Uses Lombok to reduce boilerplate code

- **Frontend** (React):
  - Component-based structure with Tailwind CSS for styling
  - API integration with backend via Axios or Fetch

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository 🍴.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request 📥.

Please ensure your code adheres to the project’s coding standards and includes tests.

## 📜 License

This project is licensed under the [MIT License](LICENSE).

## 📬 Contact

For questions or feedback, reach out to [GURUPRASATH-OG](https://github.com/GURUPRASATH-OG) or open an issue on this repository.

---

Happy billing! 🎉