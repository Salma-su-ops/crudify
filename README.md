# Crudify - Full-Stack Product Management System

A modern full-stack CRUD application built with Spring Boot and React.

## Tech Stack

**Backend:** Java 17, Spring Boot 3.5.3, Spring Data JPA, PostgreSQL, Flyway, Maven  
**Frontend:** React 19.1.0, React Router DOM, Axios, Context API, Responsive CSS

## Screenshots

### Authentication System
| Registration | Login |
|-------------|-------|
| ![Register](crudify-client/src/assets/images/register.png) | ![Login](crudify-client/src/assets/images/login.png) |

### Product Management Interface
![Product Management](crudify-client/src/assets/images/product-management.png)

### CRUD Operations
| Add Product | Search Products |
|------------|-----------------|
| ![Add Product](crudify-client/src/assets/images/add-product.png) | ![Search Products](crudify-client/src/assets/images/search-product.png) |

### Delete Confirmation
| Delete Dialog | Delete Process |
|--------------|----------------|
| ![Delete Confirmation](crudify-client/src/assets/images/delete1.png) | ![Delete Product](crudify-client/src/assets/images/delete-product2.png) |

## Prerequisites

- Java 17+, Node.js 16+, PostgreSQL 12+, Git

## Quick Start

### 1. Database Setup
```sql
CREATE DATABASE crudify_db;
```

### 2. Backend Setup
```bash
cd crudify-server
mvnw.cmd spring-boot:run    # Windows
./mvnw spring-boot:run      # Linux/Mac
```
Backend runs on `http://localhost:8080`

### 3. Frontend Setup
```bash
cd crudify-client
npm install
npm start
```
Frontend runs on `http://localhost:3000`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/products` | Get all products |
| POST | `/api/products` | Create product |
| PUT | `/api/products/{id}` | Update product |
| DELETE | `/api/products/{id}` | Delete product |
| GET | `/api/products/search?name={name}` | Search products |

## Features

**Backend:** 
- RESTful API with full CRUD operations
- Input validation with custom error messages
- Global exception handling with structured responses
- Database migrations with Flyway
- CORS configuration for frontend integration
- Security configuration for development

**Frontend:** 
- Responsive grid layout with modern CSS
- Real-time CRUD operations with instant updates
- Search functionality with case-insensitive filtering
- Form validation with client-side feedback
- Loading states and error handling
- Context API state management with useReducer

**Additional Features:**
- Sample data seeding for testing
- Search by product name
- Delete confirmation dialogs
- Responsive design for mobile devices
- Clean separation of concerns architecture

## Testing

1. Test API: `curl http://localhost:8080/api/products`
2. Test UI: Open `http://localhost:3000` and test CRUD operations

## Troubleshooting

- **Java not found**: Install Java 17 and set JAVA_HOME
- **Database error**: Check PostgreSQL service and credentials in `application.properties`
- **Port conflicts**: Stop services on ports 8080/3000 