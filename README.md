# Greenlight JSON API

Greenlight is a JSON API for retrieving and managing information about movies. You can think of its core functionality as being similar to the [Open Movie Database API](https://www.omdbapi.com/).

---

## Features

The Greenlight API will support the following endpoints and actions:

| Method | URL Pattern                        | Action                                           |
|--------|------------------------------------|-------------------------------------------------|
| GET    | `/v1/healthcheck`                  | Show application health and version information |
| GET    | `/v1/movies`                       | Show the details of all movies                 |
| POST   | `/v1/movies`                       | Create a new movie                              |
| GET    | `/v1/movies/:id`                   | Show the details of a specific movie            |
| PATCH  | `/v1/movies/:id`                   | Update the details of a specific movie          |
| DELETE | `/v1/movies/:id`                   | Delete a specific movie                         |
| POST   | `/v1/users`                        | Register a new user                             |
| PUT    | `/v1/users/activated`              | Activate a specific user                        |
| PUT    | `/v1/users/password`               | Update the password for a specific user         |
| POST   | `/v1/tokens/authentication`        | Generate a new authentication token             |
| POST   | `/v1/tokens/password-reset`        | Generate a new password-reset token             |
| GET    | `/debug/vars`                      | Display application metrics                     |

---

## Technology Stack

The Greenlight API is built with the following tools and technologies:

- **Backend**: Go
- **Database**: PostgreSQL
- **Deployment**: Digital Ocean (Linux server)

## Deployment

At the end of the project, the Greenlight API will be deployed to a Linux server hosted on Digital Ocean. The deployment process will involve:

- Configuring a production-ready PostgreSQL database.
- Setting up the Go binary on the server.
- Configuring TLS/SSL for secure communication.

This project is still in the works. This README will be updated once deployment is completed.

## Acknowledgements

This project is intended for learning purposes only. This project is part of the book ["Let's Go Further"](https://lets-go-further.alexedwards.net/) by Alex Edwards. It serves as a practical guide to building production-ready applications with Go. All rights for the book's content belong to the author.
