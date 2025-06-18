# Welcome to Open Park Project

Open Park Project is a modern, cloud-native solution for managing parking spaces, fines, and tickets. The system provides intuitive interfaces for car drivers, parking controllers, and administrators.

## Key Features

- **For Car Drivers**: Register vehicles, purchase parking tickets, receive notifications, and (hopefully not) pay fines
- **For Controllers**: Monitor parking zones, issue fines, and validate parking tickets
- **For Administrators**: Manage users, parking zones, and system settings

## System Architecture

OPP is built using a microservices architecture, deployed as stateless containers for optimal scalability and reliability. The system uses:

- RESTful APIs for communication between components
- JWT-based authentication
- PostgreSQL databases for data persistence
- Modern frontend interfaces for web and mobile

## Getting Started

- Check the [API Documentation](api.md) for integration details
- Read the [Requirements Document](req.md) to understand project scope
- Explore [Server](server.md) and [Client](client/intro.md) implementations

## Project Status

Open Park Project is an open-source initiative developed at Politecnico di Torino. It's released under the [GPL-3.0 License](license.md) and welcomes contributions from the community.

