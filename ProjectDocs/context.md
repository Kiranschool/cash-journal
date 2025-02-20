# Cash Journal Project Context

## Project Overview
Cash Journal is a personal finance journal and calendar application built with Spring Boot and React. The application uses MongoDB for data persistence and implements a modern web architecture.

## Technology Stack
- Backend: Spring Boot 3.4.2
- Frontend: React
- Database: MongoDB
- Build Tool: Maven
- Java Version: 17

## Project Structure
```
cash-journal/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/cashjournal/app/
│   │   │       ├── controller/
│   │   │       │   ├── AuthController.java
│   │   │       │   ├── TestController.java
│   │   │       │   └── WebController.java
│   │   │       ├── model/
│   │   │       │   └── User.java
│   │   │       ├── repository/
│   │   │       │   └── UserRepository.java
│   │   │       ├── service/
│   │   │       │   └── UserService.java
│   │   │       ├── dto/
│   │   │       │   ├── LoginRequest.java
│   │   │       │   └── SignupRequest.java
│   │   │       ├── config/
│   │   │       │   └── SecurityConfig.java
│   │   │       └── CashJournalApplication.java
│   │   ├── resources/
│   │   │   ├── static/
│   │   │   ├── templates/
│   │   │   │   ├── login.html
│   │   │   │   ├── signup.html
│   │   │   │   └── home.html
│   │   │   └── application.properties
│   │   └── frontend/
│   └── test/
└── pom.xml
```

## Current Implementation Status

### Backend Components
1. **Authentication System**
   - Basic user registration and login functionality
   - MongoDB-based user storage
   - Password storage currently in plain text (Security Issue)

2. **Security Configuration**
   - Basic Spring Security setup
   - CSRF disabled
   - All endpoints currently permitted

3. **API Endpoints**
   - `/api/auth/signup` - User registration
   - `/api/auth/login` - User authentication
   - `/test` and `/ping` - Test endpoints
   - `/home` - Welcome page after login

### Frontend Components
1. **Login Page**
   - Basic HTML/CSS implementation
   - Form validation
   - API integration with backend

2. **Home Page**
   - Welcome message with user's name
   - Navigation bar with links
   - Logout functionality
   - Basic dashboard layout
   - Responsive design

## Current Issues and TODOs

### Security Issues
1. **Password Storage**
   - Critical: Passwords are stored in plain text
   - TODO: Implement BCrypt password encoding
   - TODO: Add password validation and strength requirements

2. **Authentication**
   - TODO: Implement JWT token-based authentication
   - TODO: Add proper session management
   - TODO: Implement remember-me functionality

3. **Security Headers**
   - TODO: Implement proper CORS configuration
   - TODO: Enable CSRF protection
   - TODO: Add security headers (X-Frame-Options, etc.)

### Feature Gaps
1. **User Management**
   - TODO: Implement password reset functionality
   - TODO: Add email verification
   - TODO: Implement user profile management

2. **Frontend Development**
   - TODO: Complete React implementation
   - TODO: Add proper state management
   - TODO: Implement responsive design
   - TODO: Add dashboard widgets
   - TODO: Implement transaction management UI

3. **Data Validation**
   - TODO: Add proper input validation
   - TODO: Implement DTO validation using @Valid
   - TODO: Add custom validators

### Technical Debt
1. **Testing**
   - TODO: Add unit tests for services
   - TODO: Add integration tests
   - TODO: Implement E2E testing

2. **Documentation**
   - TODO: Add API documentation using SpringDoc OpenAPI
   - TODO: Add proper code documentation
   - TODO: Create user documentation

3. **Monitoring and Logging**
   - TODO: Implement proper logging strategy
   - TODO: Add monitoring using Spring Boot Actuator
   - TODO: Set up error tracking

## Next Steps
1. Address critical security issues, especially password storage
2. Complete the React frontend implementation
3. Add comprehensive test coverage
4. Implement proper error handling and validation
5. Add API documentation
6. Set up proper logging and monitoring

## Recent Changes
- Initial project setup
- Basic authentication system implementation
- MongoDB integration
- Basic frontend templates
- Added home page with welcome message
- Implemented basic navigation structure

## Potential Improvements
1. Implement proper exception handling using @ControllerAdvice
2. Add caching for better performance
3. Implement rate limiting
4. Add API versioning
5. Set up CI/CD pipeline
6. Add dashboard widgets and statistics
7. Implement transaction management features
