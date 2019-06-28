
## Password Vault

Shared Accounts is problem which is faced by many organization in case of performing administrator activity. This has been a reason for internal security breaches in many organizations.

IDX Password Vault provides a repository for dynamically generating and storing credentials. Users performing previleged access needs to checkin/checkout passwords for systems for performing the work requiring preveliged access.

### POC

**IMPORTANT :** IDX architecture is based on different microservices exposing secured end points, technical stack can vary depending on requirement of particular service, So any particular technical stack is not a hard requirement.

Spring Boot has been the base technical stack around which IDX is being developed for various services so far. We would like to evaluate  HashiCorp’s Vault is a tool to store, retrieve and secure secrets.

Spring Vault provides Spring abstractions to the HashiCorp’s Vault. We want to utilize Vault functionaly to securly  store and retrieve secrets.

#### Use Case

- User wants to perform previleged activity on a system.

- Password valut generates the password for access to system and resets the password on target system.

- Password valut assigns tha password to user for specified duration. **(Can we specify or capture that from which machine/ip/location user can perform this activity).**

- User performs activity on target system.

- User checks in password to password vault. Password is reset in target system.

