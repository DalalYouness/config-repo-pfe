# Configuration Repository for the PFE Microservices

This service is part of my final master's degree project (PFE), developed as part of my graduation work.

## Overview

This repository acts as the centralized configuration center for the microservices of the application. It contains the shared Spring Boot configuration and the service-specific property files used to configure database access, application ports, and Kafka messaging.

The project includes the following services:

- Identity Service
- Provider Content Service
- Booking and Review Service
- Notifications Service

## Repository Contents

- `application.properties` : shared application configuration such as database credentials and Kafka bootstrap server.
- `identity-service-pfe.properties` : configuration for the identity service.
- `provider-content-service-pfe.properties` : configuration for the provider-content service.
- `booking-and-review-service-pfe.properties` : configuration for the booking and review service, including Kafka producer settings.
- `notifications-service-pfe.properties` : configuration for the notifications service, including Kafka consumer settings.

## Shared Configuration

The main shared configuration contains:

- MySQL datasource username and password
- Hibernate `ddl-auto` setting
- SQL logging enabled
- Kafka bootstrap server configuration

## Service Configuration Highlights

### Identity Service
- Runs on port `8081`
- Connects to the MySQL database `identity-pfe-db`

### Provider Content Service
- Runs on port `8082`
- Connects to the MySQL database `provider-content-db`

### Booking and Review Service
- Runs on port `8083`
- Connects to the MySQL database `booking-and-review-db`
- Uses Kafka producer configuration for sending events

### Notifications Service
- Runs on port `8084`
- Connects to the MySQL database `notification-db`
- Uses Kafka consumer configuration to receive and process events from the message broker

## Technology Stack

- Spring Boot
- Spring Data JPA
- MySQL
- Apache Kafka
- Docker-friendly service configuration

## Purpose

This repository ensures that each microservice can be configured independently while maintaining a common set of environment parameters for the entire system. It supports the deployment and communication flow between the backend services in the final project architecture.

## Notes

This configuration repository is intended to support the application infrastructure of the final master's degree project and is organized for easy service-level configuration management.
