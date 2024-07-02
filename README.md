## User Validation Project

This project demonstrates the use of Java Bean Validation (JSR 380) to validate user data. The project uses Hibernate Validator as the implementation of the Bean Validation specification to validate user data against predefined constraints.

## Prerequisites
- JDK 8 or higher
- Maven or Gradle for dependency management

## Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/Bhushanseelan/UserDataValidator-using-Hibernate.git
    cd user-validation
    ```

2. Add dependencies to your `pom.xml` (for Maven):
    ```xml
    <dependency>
        <groupId>javax.validation</groupId>
        <artifactId>validation-api</artifactId>
        <version>2.0.1.Final</version>
    </dependency>
    <dependency>
        <groupId>org.hibernate.validator</groupId>
        <artifactId>hibernate-validator</artifactId>
        <version>6.0.13.Final</version>
    </dependency>
    <dependency>
        <groupId>org.glassfish</groupId>
        <artifactId>javax.el</artifactId>
        <version>3.0.0</version>
    </dependency>
    ```

3. Compile the project:
    ```bash
    mvn clean install
    ```

## Running the Project
1. Run the `UserValidation` main class:
    ```bash
    mvn exec:java -Dexec.mainClass="UserValidation"
    ```

## Project Structure

src
├── main
│ ├── java
│ │ └── UserValidation.java
│ └── resources
│ └── META-INF
│ └── validation.xml
└── test
└── java
└── UserValidationTest.java

## User Data Validation
The `UserValidation` class performs the following steps:
1. Creates a `ValidatorFactory` and a `Validator` instance.
2. Validates an invalid `User` object and prints constraint violations.
3. Validates a valid `User` object and prints the result.
4. Uses the utility method `getPastOrFutureDate` to generate dates for testing.

## Utility Methods
- `getPastOrFutureDate(int days)`: Generates a `Date` object that is either in the past or future relative to the current date. A positive `days` value generates a future date, while a negative value generates a past date.

## Technologies Used
- Java
- JSR 380 (Java Bean Validation)
- Hibernate Validator
- Maven

