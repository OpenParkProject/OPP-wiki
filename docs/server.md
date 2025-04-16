# Server

The OPP server consists of a set of microservices that work together to provide the OPP functionality.

The server is composed of the following components:
- Web server
- Application server
- Authentication provider
- Database
- Payment Service

## Web Server
The Web Server is an Nginx server that serves the web client static files and acts as a reverse proxy to the application server as well as the authentication provider.

## Application Server and Authentication Provider
The Application Server is written in Go and is responsible for handling the business logic of the OPP. It communicates with the database and the payment service to perform operations such as creating orders, processing payments, and managing users.
The Authentication Provider is responsible for managing user authentication and authorization. It uses JWT-based Bearer tokens to authenticate users and provide access to the OPP API.

Both the Application Server and the Authentication Provider follows the OpenAPI specification defined in the [API section](api.md). The Authentication Provider logic is described in the [Authentication section](auth.md).

## Database
The database is a PostgreSQL database that stores all the data for the OPP. It is used to store user information, orders, payments, and other data required by the application server.

## Payment Service
The Payment Service is a microservice that handles payment processing. It communicates with the application server to process payments and send the results back to the application server.

## Push Notification Provider
During the project definition, a Push Notification for fines was defined. The idea was that when the controller issues a fine, the system sends a push notification to the user.
However, since we did not want to rely on APN or FCM, and since this notification is normally rather infrequent, we decided to use a polling mechanism instead.
A more suitable solution would be to use email or SMS notifications, but this would require a more complex setup and is not part of the current implementation.