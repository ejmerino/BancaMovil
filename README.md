# Mobile Banking Application 🏦

This project is a **Mobile Banking Application** built with **Android Studio** for the frontend and **Spring Boot** for the backend. It also uses **PostgreSQL** as the database to store and manage user data and transactions.

## Technologies Used:
- **Frontend**: Android Studio (Dart/Flutter)
- **Backend**: Spring Boot
- **Database**: PostgreSQL

## Features:
- User Authentication
- Account Balance Management
- Transaction History
- Transfer Funds
- Logout and Session Management
- Card Management

---

## Setup Instructions

Follow these steps to set up the project on your local machine.

### 1. Backend (Spring Boot):
- Clone the repository and navigate to the backend folder.
- Make sure you have **Java** and **Maven** installed on your machine.
- Open the project in **IntelliJ IDEA** or your preferred Java IDE.
- Run the application in your IDE. By default, it will run on **port 8080**.

### 2. Frontend (Android Studio):
- Open the project in **Android Studio**.
- Make sure you have **Flutter** and **Dart** installed and configured.
- Select your preferred device (either a physical device or an emulator).
- Before running the app, change the backend IP and port in the **ApiConfig.dart** file located in `lib/config/ApiConfig.dart`.

```dart
// api_service.dart
class ApiConfig {
  //static const String ip = "10.40.30.120"; // Example IP
  static const String ip = "192.168.56.1";  // Your backend IP
  static const String port = "8080";        // Your backend port
  static String baseUrl = "http://$ip:$port"; // Full URL for API requests
}
```
- After updating the ApiConfig.dart file, you can run the mobile application.
- The frontend should now be able to communicate with the backend.

### 3. Database Setup
- Install and set up PostgreSQL on your machine.
- Create a database called banca_movil in PostgreSQL.

```sql
CREATE DATABASE banca_movil;
```

- Make sure that the database connection details in Spring Boot configuration in application.properties are correct.

### 4. Run the Application
- Once everything is set up, you can run the backend (Spring Boot) and frontend (Android Studio) simultaneously.
- The mobile app should now be able to interact with the backend, perform transactions, and manage user data.

### NOTES:

- Ensure that both the mobile app and the backend API are running on the same network if you're using a physical device.
- Adjust the IP address in ApiConfig.dart to match the IP of the machine where the backend is running if using a different network.

