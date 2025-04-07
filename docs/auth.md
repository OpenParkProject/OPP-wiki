# Authentication
Authentication is done through the `/sessions` endpoints. These endpoints are forwarded to the [auth service](https://github.com/OpenParkProject/OPP-common/openapi.yaml) by the nginx server.

Auth service creates JWT tokens for the user and returns it to the client. The client stores the JWT token in local storage and sends it with every request to the backend. The backend validates the JWT token using the public key exposed by the auth service.

```mermaid
sequenceDiagram
    actor User
    participant Auth as Auth Service
    participant Backend as Backend API
    
    %% Authentication flow
    User->>Auth: Login/Register
    Auth->>Auth: Generate and sign JWT
    Auth->>User: Return JWT token
    
    %% API request flow
    User->>Backend: Request with Bearer Token
    Backend->>Auth: Verify token (public key)
    Auth->>Backend: Token validation result
    
    alt Valid Token
        Backend->>User: Return requested resource
    else Invalid Token
        Backend->>User: Return 401 Unauthorized
    end
```

## JWT Token Structure
Depending on the user role, the generated JWT token will have different permissions. The following roles are supported:
- admin
- controller
- driver

WIP