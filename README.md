# Car Service Management System

A desktop application written in C++ using Qt for managing customers, workers, services, and orders in a car service environment.

The application includes user authentication, multiple user roles, role-based access to different parts of the interface, and file-based data storage.

## Overview

This project was created as part of an Object-Oriented Programming course.

Its goal was to design a larger desktop application using object-oriented principles and a graphical user interface.

The system models different types of users and gives them access to different functionality depending on their role.

The project demonstrates work with:

- C++
- Qt Widgets
- Qt Designer
- Object-oriented programming
- User authentication
- Role-based access
- File input/output
- Application state management
- CMake

## Features

- Desktop graphical user interface
- User login system
- Multiple user types
- Role-based interface access
- Individual customer accounts
- Company customer accounts
- Worker accounts
- Service management
- Order management
- User-specific order loading
- File-based data storage
- Qt resource handling
- CMake-based build system

## User Roles

The application supports multiple types of users.

### Individual Customer

Individual customers can log into the application and access functionality intended for regular car-service clients.

### Company Customer

The system also supports company accounts, allowing business customers to use the application separately from individual users.

### Worker

Workers have access to functionality intended for managing service-related information and customer orders.

The application changes the available interface depending on the type of user who is currently logged in.

## Authentication

The application contains a dedicated login dialog.

Users are loaded when the application starts.

After successful authentication, the currently logged-in user is stored by the application and the interface is adjusted depending on the user's role.

This allows different user types to access different parts of the system.

## Order Management

The system loads order data from files and displays orders associated with the currently logged-in user.

This allows customers to see information relevant to their own account.

Workers can access additional functionality for working with customer orders and service-related data.

## Service Management

The application works with service data representing services available in the car service system.

These services are loaded and used throughout the application when working with customer orders.

## Technologies

- C++
- C++17
- Qt
- Qt Widgets
- Qt Designer
- CMake
- Object-oriented programming
- File I/O

## Project Structure

```text
car-service-management-system/
│
├── main.cpp
├── mainwindow.cpp
├── mainwindow.h
├── mainwindow.ui
│
├── logindialog.cpp
├── logindialog.h
├── logindialog.ui
│
├── resources.qrc
├── resources/
│
├── users.txt
├── orders.txt
│
└── CMakeLists.txt
```

### Main Files

- `main.cpp` — application entry point
- `mainwindow.cpp` / `mainwindow.h` — main application logic
- `mainwindow.ui` — main Qt interface
- `logindialog.cpp` / `logindialog.h` — authentication logic
- `logindialog.ui` — login interface
- `resources.qrc` — Qt resource configuration
- `resources/` — application resources
- `users.txt` — user data
- `orders.txt` — order data
- `CMakeLists.txt` — build configuration

## Object-Oriented Design

The application was designed using object-oriented programming principles.

Different types of users are represented separately, and the program changes its behavior depending on the authenticated user's role.

The project applies concepts such as:

- Classes and objects
- Inheritance
- Encapsulation
- Separation of responsibilities
- Interaction between GUI components and application logic

## Building the Project

### Requirements

To build the project, you need:

- A C++ compiler with C++17 support
- Qt 5 or Qt 6
- CMake 3.16 or newer

### Clone the Repository

```bash
git clone https://github.com/hannahkuklovska/car-service-management-system.git
cd car-service-management-system
```

### Create a Build Directory

```bash
mkdir build
cd build
```

### Configure the Project

```bash
cmake ..
```

### Build

```bash
cmake --build .
```

After the project has been built successfully, run the generated application executable.

Depending on the operating system and build configuration, the executable may be located inside the `build` directory.

## Application Flow

A typical application flow is:

1. Start the application.
2. The login dialog is displayed.
3. Enter user credentials.
4. The application identifies the user type.
5. The main interface is opened.
6. Available features are enabled according to the user's role.
7. Relevant services and orders are loaded.

## Screenshots

Create an `images` folder in the repository and add screenshots of the application.

Recommended screenshots:

```text
images/
├── login.png
├── customer-view.png
├── worker-view.png
└── orders.png
```

Then display them in the README:

### Login

![Login screen](images/login.png)

### Customer View

![Customer interface](images/customer-view.png)

### Worker View

![Worker interface](images/worker-view.png)

### Order Management

![Order management](images/orders.png)

## Data Storage

The current version of the project uses text files for storing application data.

This keeps the project simple and allows the main focus to remain on object-oriented design, application logic, and the Qt interface.

For a larger production application, the text-file storage could be replaced with a database.

## What I Learned

Through this project, I gained experience building a larger desktop application in C++.

In particular, I practiced:

- Designing an application using object-oriented programming
- Working with classes and different user types
- Building graphical interfaces with Qt
- Using Qt Designer
- Connecting interface components to application logic
- Implementing authentication
- Implementing role-based behavior
- Reading and storing application data using files
- Managing application state
- Organizing a multi-file C++ project
- Using CMake to configure and build an application

## Possible Improvements

Future improvements could include:

- Replacing text-file storage with a database
- Password hashing and improved authentication security
- Stronger input validation
- Improved error handling
- Automated tests
- Better separation between UI and business logic
- Improved order filtering and search
- Editing and deleting orders
- Additional service-management functionality
- User account management
- Persistent application settings
- Improved visual design

## Author

Hannah Kuklovska
