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

## Local Development

- Setup postgresql, create a database called `greenlight` and set the database DSN to env variable `GREENLIGHT_DB_DSN`. This can also be stored in `.envrc` file in project root.
- Make sure the postgresql service is running with the active DSN
- Run `make db/migrations/up` to create tables for the API
- Install Golang and run `go mod tidy` to install dependencies
- Run `make run/api` to run the API locally
- You can now make requests to the Greenlight API in the specified port (default, 4000) using curl or postman.
- Look at the API spec above to try out different API endpoints.

## Learning Outcomes

- HTTP server setup and configuration
- Parsing command line flags from external input to CLI
- Implementing middlewares
- Setting up database and running migrations
- Implementing pagination, sorting and text search
- Using background services to send an email or perform graceful shutdown
- Implementing user registration and token based authentication and authorization
- Configuring CORS as a middleware.
- Writing Makefile for easy to understand CLI commands.

## Acknowledgements

This project is intended for learning purposes only. This project is part of the book ["Let's Go Further"](https://lets-go-further.alexedwards.net/) by Alex Edwards. It serves as a practical guide to building production-ready applications with Go. All rights for the book's content belong to the author.
