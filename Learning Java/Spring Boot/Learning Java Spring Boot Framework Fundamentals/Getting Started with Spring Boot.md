
In this section I explored the fundamentals of Spring Boot and how to set up a 
development environment to build Spring applications efficiently. I learned everything 
from project creation and structure to debugging and configuration.

## Introduction To Spring Boot

- Spring Boot is a framework that simplifies Java application development by handling configuration, dependency management, and embedded servers.
- It allows us to quickly build production ready applications with minimal setup.

## Setting Up the Development Environment

To build a Spring Boot application we need:
- **Java Development Kit (JDK)** - Spring Boot  requires Java  17 or later.
- **An Editor or IDE** - Popular choices include:
	- IntelliJ IDEA (Recommended)
	- Eclipse
	- VS Code
- **A Build Tool** - Spring supports
	- **Maven** - More widely used and has been around longer.
	- **Gradle** - More modern, concise, and optimized for performance.

## Creating a Spring Boot Project

We  can generate a Spring Boot project in two ways:
- **Spring Initializr** [start.spring.io](start.spring.io) - A web-based tool to configure and generate a Spring Boot project.
- **Directly in IntelliJ IDEA (Ultimate)** - IntelliJ provides built-in support for creating and configuring Spring Boot projects.

## Understanding the Project Structure

A Spring Boot project consists of:
- `src/main/java` - Contains the application code.
- `src/main/resources` - Stores configuration files (application.properties or application.yml)
- `pom.xml` or `build.gradle` - Manages project dependencies using Maven or Gradle

## Dependency Management

- Spring Boot simplifies dependency management through **Spring Boot Starters**, which bundle commonly used libraries
- Maven and Gradle handle versioning automatically, reducing the need for manual dependency updates.

## Running Spring Boot Applications

Spring Boot provides multiple ways to run an application
- Using You editor of choice's **Run** button
- From the terminal
	- Maven - `mvn spring-boot:run`
	- Gradle - `gradle task bootRun`