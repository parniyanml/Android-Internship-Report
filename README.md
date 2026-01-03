# Android Development Internship Report

## Overview
This repository contains the documentation and technical summary of the internship conducted at Kasra Engineering Company (Kasra Kimiyagaran Sarzamin Rayaneh). The internship focused on the development, optimization, and testing of enterprise-level Android applications used for attendance and human resource management.

**Intern:** Parniyan Malekzadeh
**Department:** Electrical and Computer Engineering
**Supervisor:** Mr. Mahmoud Bagheri (CTO)
**Duration:** Summer 2024

## Company Background
Kasra Engineering Company is a provider of software and hardware solutions for traffic control and human resource management. With over two decades of experience, the company serves major organizations including the Ministry of Oil and Iran Khodro, offering products such as attendance systems, nutrition management software, and mobile applications.

## Technical Scope
The primary objective of this internship was to contribute to the development of the company's Android applications while mastering modern development tools and practices. The work adhered to the following technical stack and methodologies:

### Technology Stack
* **Language:** Kotlin
* **IDE:** Android Studio
* **Version Control:** Git, GitHub
* **API Testing:** Postman
* **CI/CD:** Jenkins
* **Documentation:** Dokka

### Architecture & Libraries
* **Architecture Pattern:** MVVM (Model-View-ViewModel)
* **Networking:** Retrofit, Gson
* **Database:** Room (SQLite abstraction)
* **Concurrency:** Kotlin Coroutines, LiveData
* **Image Loading:** Glide
* **Dependency Injection:** Manual implementation for scoping
* **UI/UX:** XML, ConstraintLayout, Material Design, Navigation Component

### Testing & Optimization
* **Unit Testing:** JUnit, Mockito
* **UI Testing:** Espresso
* **Profiling:** Android Profiler, LeakCanary
* **Analytics:** Firebase Analytics, Crashlytics

## Key Contributions

### 1. Attendance Management Module
Developed a new feature module allowing users to view and manage their attendance records.
* Implemented a `RecyclerView` to display daily attendance logs.
* Integrated filtering capabilities using Date Pickers and Spinners to sort records by date and status.
* Managed data flow using Repository patterns to separate data sources from UI logic.

### 2. Offline Synchronization
Implemented robust offline-first capabilities to ensure application functionality without internet connectivity.
* Utilized Room database to cache API responses locally.
* Designed a synchronization algorithm to update local data with the server upon network reconnection.
* Leveraged `SafeArgs` for secure data passing between fragments.

### 3. Asynchronous Operations
Refactored legacy code and implemented new features using Kotlin Coroutines to prevent UI blocking on the main thread.
* Replaced standard callbacks with `suspend` functions and `viewModelScope`.
* Handled heavy I/O operations (database writes and network requests) on background dispatchers.

### 4. Quality Assurance and Performance
* **Testing:** Wrote unit tests for business logic (e.g., attendance calculation) and UI tests for interaction verification.
* **Memory Management:** Identified and resolved memory leaks using LeakCanary; optimized `ConstraintLayout` hierarchies to reduce rendering time.
* **Network Optimization:** Implemented caching strategies in Retrofit to reduce bandwidth usage.

## Technical Implementation Details

### MVVM Architecture
The project strictly followed the Model-View-ViewModel architecture to ensure separation of concerns:
* **Model:** Managed data handling via Room entities and Retrofit service calls.
* **ViewModel:** Held UI-related data using LiveData, surviving configuration changes.
* **View:** Fragments and Activities responsible solely for rendering the UI and capturing user input.

### Coroutines Implementation
A significant portion of the internship focused on mastering Coroutines for asynchronous programming. The implementation utilized `launch` and `async` builders to handle concurrent tasks efficiently, replacing complex threading models and AsyncTasks.

## Documentation
Codebases were documented using KDoc standard comments, and API reference documentation was generated automatically using Dokka. A comprehensive user guide was also created to assist future developers with setup and deployment.

## References
* Android Developer Documentation
* Kotlin Language Documentation
* Kasra Engineering Internal Documentation
