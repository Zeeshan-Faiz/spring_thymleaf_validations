# Spring Boot Web Application Documentation

## Overview

Welcome to the Spring Boot Validation Web Application, a project built to showcase the importance of validations and how Spring Boot simplifies the process. This application is designed to demonstrate various validation techniques in a web application context.

## Setup

1. **Initialize the Project:**
   - Visit [Spring Initializer](https://start.spring.io/).
   - Add dependencies: `Spring Web`, `Thymeleaf`, and `Validation`.
   - Generate and download the Maven project.

2. **Import Project:**
   - Import the downloaded project into your favorite IDE.

3. **Run Application:**
   - Run the main class, `DemoValidationApplication.java`.
   - The application will be available at [http://localhost:8080](http://localhost:8080).

## Importance of Validations

Validation is a crucial aspect of web application development, ensuring that data entered by users is accurate, secure, and meets the specified criteria. Effective validations enhance the overall user experience, prevent security vulnerabilities, and maintain data integrity.

## Application Functionalities

### Endpoint: http://localhost:8080

This is the main landing page of the application.

### Functionality 1: Input Validation

This functionality demonstrates how Spring Boot simplifies input validations in a web application.

- **How to Access:**
  -  - Open your browser and navigate to [http://localhost:8080](http://localhost:8080).

- **What it Does:**
  - Presents a form for user input.
  - Applies validations to fields such as name, postal code, and course code.
  - Displays error messages for invalid inputs.


## Sample Code

```java
// Sample code for Input Validation
@Override
public boolean isValid(String theCode, ConstraintValidatorContext theConstraintValidatorContext) {

        boolean result;
        if (theCode != null) {
                result = theCode.startsWith(coursePrefix);
        }
        else {
                result = true;
        }
        return result;
}
