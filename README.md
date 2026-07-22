# Expense Tracker Pro

A complete enterprise-grade expense tracking application built with Java Spring Boot and React.

## 🚀 Features

### Authentication
- User Registration and Login
- JWT-based Authentication
- Refresh Token Mechanism
- BCrypt Password Encryption
- Role-Based Authorization (ADMIN, USER)

### Dashboard
- Total Income and Expense Overview
- Remaining Balance Calculation
- Monthly Summary Statistics
- Recent Transactions Feed
- Interactive Charts and Graphs
- Real-time Statistics

### Income Management
- Add Income Transactions
- Update Income Records
- Delete Income Entries
- Search and Filter Capabilities

### Expense Management
- Add Expense Transactions
- Update Expense Records
- Delete Expense Entries
- Search and Filter Capabilities

### Category Management
- Create Custom Categories
- View All Categories
- Update Category Details
- Delete Categories
- Pre-loaded Default Categories

### Reports and Analytics
- Monthly Reports
- Weekly Reports
- Yearly Reports
- Category-wise Analysis
- Export to PDF
- Export to Excel

### User Settings
- Update User Profile
- Change Password
- Upload Avatar/Profile Picture
- Dark Mode Toggle

## 🛠 Technology Stack

### Backend
- **Java 21** - Latest Java version
- **Spring Boot 3** - Framework
- **Spring Security** - Authentication & Authorization
- **Spring Data JPA** - Data Access
- **Hibernate** - ORM
- **JWT** - Token-based Authentication
- **MySQL** - Database
- **Lombok** - Code Generation
- **Swagger/OpenAPI** - API Documentation
- **Maven** - Build Tool

### Frontend
- **React** - UI Library
- **Vite** - Build Tool
- **Tailwind CSS** - Styling
- **Axios** - HTTP Client
- **React Router** - Navigation
- **Context API** - State Management

### DevOps
- **Docker** - Containerization
- **Docker Compose** - Orchestration
- **GitHub Actions** - CI/CD

## 📋 Prerequisites

- Java 21 JDK
- Node.js 18+
- MySQL 8.0+
- Docker & Docker Compose (optional)
- Maven 3.8+

## 🔧 Installation

### Backend Setup

1. **Navigate to backend directory**
   ```bash
   cd backend
   ```

2. **Create MySQL Database**
   ```bash
   mysql -u root -p < src/main/resources/schema.sql
   ```

3. **Configure Database Connection**
   Edit `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/expense_tracker
   spring.datasource.username=root
   spring.datasource.password=your_password
   ```

4. **Build and Run**
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

Backend will start on `http://localhost:8080`

### Frontend Setup

1. **Navigate to frontend directory**
   ```bash
   cd frontend
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Configure API Endpoint**
   Create `.env.local`:
   ```
   VITE_API_BASE_URL=http://localhost:8080
   ```

4. **Start Development Server**
   ```bash
   npm run dev
   ```

Frontend will start on `http://localhost:5173`

## 🐳 Docker Setup

### Using Docker Compose (Recommended)

```bash
# Build and start all services
docker-compose up -d

# Stop all services
docker-compose down
```

Services will be available at:
- Backend: `http://localhost:8080`
- Frontend: `http://localhost:3000`
- MySQL: `localhost:3306`

## 📚 API Documentation

Swagger UI is available at: `http://localhost:8080/swagger-ui.html`

## 🔐 Authentication

### Register User
```bash
POST /api/auth/register
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

### Login
```bash
POST /api/auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "password123"
}
```

Response:
```json
{
  "token": "eyJhbGciOiJIUzI1NiIs...",
  "refreshToken": "eyJhbGciOiJIUzI1NiIs...",
  "user": {
    "id": 1,
    "email": "john@example.com",
    "firstName": "John",
    "lastName": "Doe",
    "role": "USER"
  }
}
```

## 📊 Project Structure

```
expense-tracker-pro/
├── backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/expensetracker/
│   │   │   │       ├── controller/
│   │   │   │       ├── service/
│   │   │   │       ├── entity/
│   │   │   │       ├── dto/
│   │   │   │       ├── repository/
│   │   │   │       ├── security/
│   │   │   │       ├── config/
│   │   │   │       ├── exception/
│   │   │   │       ├── util/
│   │   │   │       └── validation/
│   │   │   └── resources/
│   │   │       ├── application.properties
│   │   │       ├── schema.sql
│   │   │       └── data.sql
│   │   └── test/
│   └── pom.xml
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── layouts/
│   │   ├── services/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── utils/
│   │   ├── styles/
│   │   └── App.jsx
│   ├── public/
│   ├── package.json
│   └── vite.config.js
├── docker-compose.yml
├── Dockerfile (backend)
├── Dockerfile (frontend)
├── .gitignore
├── LICENSE
└── README.md
```

## 🧪 Testing

### Backend Tests
```bash
cd backend
mvn test
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 📖 Architecture

### Backend Architecture
- **MVC Pattern**: Model-View-Controller separation
- **Repository Pattern**: Data access abstraction
- **Service Layer**: Business logic
- **DTO Pattern**: Data Transfer Objects
- **Global Exception Handling**: Centralized error handling
- **JWT Security**: Token-based authentication

### Frontend Architecture
- **Component-Based**: Reusable React components
- **Context API**: State management
- **Custom Hooks**: Reusable logic
- **Protected Routes**: Route guards

## 🔄 CI/CD Pipeline

GitHub Actions workflows:
- Build and Test on Push
- Deploy to Production
- Code Quality Checks

## 📝 License

MIT License - see LICENSE file for details

## 👥 Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📧 Support

For support, please create an issue in the repository.

---

**Built with ❤️ by Expert Software Architects**
