 # Seapay

 ## Description

Seapay is a fintech app consists of 4 different services
  - API gateway
    - API gateway service routes all requests to other services
  - User account
    - User account service takes care of user management: user creation, get user data, etc
  - Wallet
    - Wallet service handles all wallet functionalities: update balance, get balance, create wallet, etc
  - Transaction
    - Transaction service manage all transaction data

The project itself has 4 modules
 - seapay-api
   - a module that abstracts interface for all services
 - seapay-common
   - a module that groups all common functionalities used by all services
 - seapay-domain
   - the bussiness logic for all services goes here
 - seapay-monolith
   - an entry point of our monolithic app, including all handlers
  
 ## Prerequisites
  
In order to build and run this microservices, you need these requirements:
  
  1. Java, with minimum version 8
  2. PostgreSQL
  3. Linux/UNIX operating system
  
 ## Usage

 ### How to build
 
 1. Make sure to fulfill the configs on environment variables on `/seapay-domain/src/main/resources/application.yml`
 2. Build all microservices with this command
     ```
     make all
     ```

 ### How to run
 #### Run monolith program

   ```
   make run-monolith
   ```

 #### Run microservice
 To run the services, you can run this script:

1. To run gateway service
   ```
   make run-gateway
   ```

2. To run user service
   ```
   make run-user
   ```
3. To run wallet service
   ```
   make run-wallet
   ```
4. To run transaction service
   ```
   make run-transaction
   ```
