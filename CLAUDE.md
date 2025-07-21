# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Klytopia is an Authorization Server built with Spring Boot 3.5.3 and Java 24. The project follows standard Maven structure and is designed as part of the Apexentile suite of applications.

## Architecture

- **Framework**: Spring Boot 3.5.3 with Java 24
- **Build Tool**: Maven with wrapper scripts (`mvnw` and `mvnw.cmd`)
- **Package Structure**: `com.apexentile.klytopia`
- **Key Dependencies**:
  - Spring Boot Starter Web (REST API)
  - Spring Boot Starter Data JPA (database access)
  - Spring Boot Starter Cache (caching layer)
  - Spring Boot Starter Actuator (monitoring endpoints)
  - Lombok (code generation)

## Development Commands

### Build and Run
```bash
./mvnw clean compile                    # Compile the project
./mvnw spring-boot:run                  # Run the application
./mvnw clean package                    # Build JAR file
```

### Testing
```bash
./mvnw test                             # Run all tests
./mvnw test -Dtest=KlytopiaApplicationTests  # Run specific test class
```

### Other Maven Commands
```bash
./mvnw clean                            # Clean build artifacts
./mvnw dependency:tree                  # Show dependency tree
./mvnw spring-boot:build-image         # Create OCI container image
```

## Code Structure

- **Main Application**: `src/main/java/com/apexentile/klytopia/KlytopiaApplication.java`
- **Configuration**: `src/main/resources/application.properties`
- **Tests**: `src/test/java/com/apexentile/klytopia/`
- **Static Resources**: `src/main/resources/static/`
- **Templates**: `src/main/resources/templates/`

## Important Notes

- Uses Maven wrapper - always use `./mvnw` instead of `mvn`
- Lombok is configured with annotation processing
- Project uses Spring Boot Actuator for health checks and monitoring
- No database configuration present yet - likely using in-memory H2 for development