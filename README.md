# Trendify Clothing Store

A modern Android application for an online clothing store built with Kotlin and Android Architecture Components.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Building the Project](#building-the-project)
- [Running the Application](#running-the-application)
- [Project Architecture](#project-architecture)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## 📱 Overview

Trendify is a cutting-edge Android application that provides a seamless shopping experience for clothing store customers. The app enables users to browse through a curated collection of fashion items, manage their shopping cart, and complete purchases with ease.

The project is designed using modern Android development practices with a focus on clean architecture, maintainability, and user experience.

## ✨ Features

- **Product Browsing**: Explore a comprehensive catalog of clothing items
- **Advanced Filtering**: Filter products by category, size, color, and price
- **Shopping Cart**: Add/remove items and manage quantities
- **User Authentication**: Secure login and registration system
- **Order Management**: View order history and track purchases
- **Payment Integration**: Secure payment gateway integration
- **User Profiles**: Manage personal information and preferences
- **Wishlist**: Save favorite items for later
- **Push Notifications**: Stay updated with order and promotional notifications

## 🛠 Tech Stack

- **Language**: Kotlin
- **Min SDK**: API 21+
- **Target SDK**: Latest Android version
- **Build System**: Gradle (Kotlin DSL)
- **Architecture Pattern**: MVVM + Clean Architecture
- **UI Framework**: Android Jetpack Components

### Key Technologies

- **Jetpack Components**:
  - Navigation
  - LiveData & ViewModel
  - Room Database
  - DataStore
  - WorkManager

- **Networking**:
  - Retrofit (HTTP client)
  - OkHttp (Network interceptor)

- **Dependency Injection**:
  - Hilt / Dagger 2

- **Testing**:
  - JUnit 4
  - Mockito
  - Espresso (UI Testing)

## 📁 Project Structure

```
Trendify_clothing_store/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/trendify/
│   │   │   │   ├── data/              # Data layer (repositories, models)
│   │   │   │   │   ├── local/         # Local database
│   │   │   │   │   ├── remote/        # API services
│   │   │   │   │   └── repository/    # Repository implementations
│   │   │   │   ├── domain/            # Domain layer (use cases, entities)
│   │   │   │   │   ├── model/
│   │   │   │   │   └── usecase/
│   │   │   │   ├── presentation/      # UI layer (activities, fragments, viewmodels)
│   │   │   │   │   ├── ui/
│   │   │   │   │   ├── viewmodel/
│   │   │   │   │   └── adapter/
│   │   │   │   └── di/                # Dependency injection
│   │   │   ├── res/                   # Resources (layouts, strings, colors, drawables)
│   │   │   └── AndroidManifest.xml
│   │   ├── test/                      # Unit tests
│   │   └── androidTest/               # Instrumented tests
│   └── build.gradle.kts               # Module-level build configuration
├── build.gradle.kts                   # Project-level build configuration
├── settings.gradle.kts                # Project settings
├── gradle.properties                  # Gradle properties
├── gradlew                            # Gradle wrapper (Linux/Mac)
├── gradlew.bat                        # Gradle wrapper (Windows)
└── README.md
```

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Java Development Kit (JDK)**: Version 11 or higher
- **Android Studio**: Latest stable version (2023.1 or higher)
- **Android SDK**: API level 21 or higher
- **Gradle**: 7.4 or higher (included with Android Studio)
- **Git**: For version control

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/Trendify_clothing_store.git
cd Trendify_clothing_store
```

### 2. Open in Android Studio

1. Launch Android Studio
2. Click **File** → **Open**
3. Navigate to and select the project folder
4. Android Studio will detect and sync the Gradle project automatically

### 3. Configure Local Properties

Ensure your `local.properties` file contains the correct SDK path:

```properties
sdk.dir=/path/to/your/Android/SDK
```

### 4. Sync Gradle

In Android Studio:
- Click **File** → **Sync Now** or use the sync button in the top bar
- Wait for all dependencies to download and build

## 🔨 Building the Project

### Build APK

```bash
./gradlew build
```

### Build Release APK

```bash
./gradlew assembleRelease
```

### Build Debug APK

```bash
./gradlew assembleDebug
```

### Run Tests

```bash
# Unit tests
./gradlew test

# Instrumented tests
./gradlew connectedAndroidTest
```

## ▶️ Running the Application

### Using Android Studio

1. Connect an Android device via USB or launch an emulator
2. Click the **Run** button (green play icon) in the toolbar
3. Select your target device
4. The app will build and launch on the device

### Using Command Line

```bash
./gradlew installDebug
adb shell am start -n com.trendify/.MainActivity
```

### System Requirements for Running

- **Physical Device**: Android device with API level 21+
- **Emulator**: Android Virtual Device (AVD) with API level 21+
- **RAM**: Minimum 4GB recommended for smooth emulation
- **Storage**: Approximately 500MB free space for app and dependencies

## 🏗 Project Architecture

This project follows **Clean Architecture** principles with **MVVM** (Model-View-ViewModel) pattern:

### Layers

1. **Presentation Layer (UI)**
   - Activities, Fragments, and Composables
   - ViewModels for state management
   - UI adapters and utilities

2. **Domain Layer (Business Logic)**
   - Use cases containing business logic
   - Interface definitions for repositories
   - Entity models independent of framework

3. **Data Layer (Data Management)**
   - Repository implementations
   - Local database access (Room)
   - Remote API calls (Retrofit)
   - Data models and mappers

### Benefits

- **Separation of Concerns**: Each layer has distinct responsibilities
- **Testability**: Easy to write unit and integration tests
- **Maintainability**: Changes in one layer don't affect others
- **Scalability**: Easy to add new features without affecting existing code
- **Reusability**: Business logic can be reused across different UI layers

## 📦 Dependencies

### Core Android Libraries

```kotlin
// Jetpack Navigation
androidx.navigation:navigation-fragment-ktx
androidx.navigation:navigation-ui-ktx

// Jetpack Lifecycle
androidx.lifecycle:lifecycle-runtime-ktx
androidx.lifecycle:lifecycle-viewmodel-ktx
androidx.lifecycle:lifecycle-livedata-ktx

// Room Database
androidx.room:room-runtime
androidx.room:room-ktx

// DataStore
androidx.datastore:datastore-preferences

// WorkManager
androidx.work:work-runtime-ktx
```

### Networking

```kotlin
// Retrofit
com.squareup.retrofit2:retrofit
com.squareup.retrofit2:converter-gson

// OkHttp
com.squareup.okhttp3:okhttp
com.squareup.okhttp3:logging-interceptor
```

### Dependency Injection

```kotlin
// Hilt
com.google.dagger:hilt-android
com.google.dagger:hilt-compiler
```

### Testing

```kotlin
// JUnit
junit:junit

// Mockito
org.mockito.kotlin:mockito-kotlin

// Espresso
androidx.test.espresso:espresso-core
```

For a complete list of dependencies, refer to `build.gradle.kts` and `gradle.properties`.

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

### Getting Started

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style Guidelines

- Follow Kotlin naming conventions
- Use meaningful variable and function names
- Write clear comments for complex logic
- Keep functions small and focused
- Use proper error handling

### Testing Requirements

- Write unit tests for business logic
- Write UI tests for critical user flows
- Ensure all tests pass before submitting PR
- Aim for at least 80% code coverage

### Commit Messages

Follow conventional commit format:
- `feat: Add new feature`
- `fix: Fix bug in feature`
- `docs: Update documentation`
- `refactor: Refactor code structure`
- `test: Add or update tests`

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

