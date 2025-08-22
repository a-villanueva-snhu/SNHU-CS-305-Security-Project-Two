# SNHU-CS-305-Security-Project-Two
The final project for CS 305

**Secure REST Service for Artemis Financial**

This project is a Java Spring Boot application refactored to enhance security for a fictional client, Artemis Financial. The primary goals were to remediate critical dependency vulnerabilities, implement secure communication protocols, and add a cryptographic hashing feature for data integrity.

**Key Features **
Vulnerability Remediation: Upgraded the Spring Boot framework from an insecure version (2.2.4) to a modern, secure version (3.3.3), resolving numerous critical CVEs in core dependencies.

Secure Communication (HTTPS): Configured the application to use the HTTPS protocol with a self-signed TLS certificate, ensuring all data transmitted between the client and server is encrypted.

Cryptographic Hashing: Implemented a /hash REST endpoint that provides a SHA-256 checksum for any given string, allowing for data integrity verification.

Secure Coding Practices: Refactored code to follow best practices, including using a dedicated controller for web logic, adding input validation to prevent DoS attacks, and implementing secure error logging.

**Technologies Used **
Java 17

Spring Boot 3.3.3

Apache Maven

OWASP Dependency-Check for vulnerability scanning

Java Keytool for certificate management

_**Getting Started**_
**Prerequisites**
Java Development Kit (JDK) 17 or newer

Apache Maven

**How to Run**
Build the application:

Bash

mvn clean install
Run the application:

Bash

java -jar target/rest-service-0.0.2-SNAPSHOT.jar
The server will start on port 8443.

Test the Hashing Endpoint:
Open a web browser and navigate to the following URL to get the SHA-256 hash of "HelloArtemis":

https://localhost:8443/hash?data=HelloArtemis
