# Snowstorm Java Client

This project provides a Java client for interacting with **Snowstorm**, a terminology server developed by **Snomed International**. It is based on OpenAPI specifications and utilizes the `openapi-generator-maven-plugin` to automatically generate the client code. The client is built with **WebClient**, leveraging **Spring Boot 3** for asynchronous and reactive web service interaction.

## Features

- **Generated from OpenAPI Spec:**
    - Automatically generates client code from the provided OpenAPI specification (`snowstorm.json`).
- **Spring Boot 3 Support:**
    - Uses the latest **Spring Boot 3** framework for enhanced performance and modern features.
- **Reactive WebClient:**
    - Built with **WebClient** to handle asynchronous, non-blocking requests.
- **Configurable Options:**
    - Serializes BigDecimal values as strings for precision.
    - Supports Java model serialization.
    - Container types default to non-null values.
- **Flexible Configuration:**
    - Customizes packaging, model name prefixes, and package locations for generated code.

## Project Structure

- **API Package:**
    - `au.csiro.snowstorm-client.api`: Contains the generated API client classes.
- **Model Package:**
    - `au.csiro.snowstorm-client.model`: Contains the generated data models.
- **Invoker Package:**
    - `au.csiro.snowstorm-client.invoker`: Contains utility classes for making API calls.

## Prerequisites

- **Java 17**
- **Maven**

## How to Use

1. **Generate the Client Code:**
    - The OpenAPI Generator Maven plugin is configured to generate the client code from the `snowstorm.json` OpenAPI specification located in `src/main/resources/`.
    - To generate the code, run:

   ```bash
   mvn openapi-generator:generate
