
# Smart Transit System - Installation Guide

## 1. Project Overview

Smart Transit is a commuter vehicle tracking system
that provides vehicle location monitoring, estimated
time of arrival (ETA), and fleet demand monitoring.

## 2. Prerequisites

Install the following software:

- Flutter SDK
- Dart SDK
- Node.js and npm
- MySQL Server
- Visual Studio Code
- Android Studio
- Git

## 3. Backend Installation

### Step 1: Open the backend directory

```bash
cd smart_transit_backend
```

### Step 2: Install dependencies

```bash
npm install
```

### Step 3: Configure environment variables

Create a `.env` file using the variables required
by your backend configuration.

Do not publish your actual database passwords,
API keys, or other secrets.

### Step 4: Start the backend

```bash
node server.js
```

The local backend should be available at:

http://localhost:3000

Production backend:

https://smart-transit-backend.onrender.com

## 4. Passenger Application Setup

### Step 1: Open the passenger Flutter project

Open the passenger application folder in VS Code.

### Step 2: Install dependencies

```bash
flutter pub get
```

### Step 3: Run the application

```bash
flutter run
```

## 5. Operator Application Setup

### Step 1: Open the operator Flutter project

Open the operator application folder in VS Code.

### Step 2: Install dependencies

```bash
flutter pub get
```

### Step 3: Run the application

```bash
flutter run
```

## 6. Production Backend

The deployed backend is hosted on Render:

https://smart-transit-backend.onrender.com

## 7. Important Notes

- Configure the correct backend URL in both Flutter applications.
- Configure the MySQL database before running the backend locally.
- Make sure the required environment variables are configured.
- Never upload passwords or secret credentials to GitHub.

## 8. Project Status

Smart Transit is an academic development project
and is currently under development.
