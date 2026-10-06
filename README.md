# Car Service Management System

A desktop application written in C++ using Qt for managing users, services, and orders in a car service environment.

The application includes authentication, multiple user roles, and a graphical user interface that changes depending on the currently logged-in user.

## Overview

This project was created as part of an Object-Oriented Programming course.

Its goal was to design a larger desktop application using object-oriented principles and a graphical user interface. The system models different types of users and gives them access to different parts of the application depending on their role.

The project demonstrates work with:

- C++
- Qt Widgets
- Qt Designer
- Object-oriented programming
- Role-based access
- File input/output
- Application state management
- CMake

## Features

- Desktop graphical user interface
- User login system
- Support for multiple user types
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

Users are loaded when the application starts. After successful authentication, the currently logged-in user is stored by the application.

The interface is then adjusted depending on the authenticated user's role, allowing different user types to access different parts of the system.

## Order Management

The system loads order data from files and displays orders associated with the currently logged-in user.

This allows users to see information relevant to their own account.

Workers can access additional service-related functionality intended for working with customer orders.

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
ProjOOP/
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
