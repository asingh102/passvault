
## XConfig

IDX is developed based on cloud native microservices architecture where configurations related to each service needs to be centrally stored. Thix provides a consitent way of managing the configuration across the services and provides single point view of configurations.

XConfig (micro)service is responsible for managing configurations for all the services in IDX ecosystem. We will be levereging Spring cloud config service and HASHICORP vault for storing the configuration. Spring config service provides us with great mechanism for storing configurations and Hasicorp's Vault provides us a good way of keeping the sensitive configurations like password, keys etc.

Initial POC will be aimed at achieving following functionalies : 
- Configuration of different services stored in Git repository.
- Configuration for different environment (Dev, Test, prod)
- Sensitive info like password and keys should be stored in Vault
- Configuration versioning
