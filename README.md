# dockerTutorial-Container-Communication

This repository contains a simple Node.js application demonstrating container communication within a Docker environment. The application provides a basic API to manage favorites and retrieve data from the Star Wars API (SWAPI).

## Prerequisites

- Docker installed on your system

## Getting Started

Follow these steps to get the project up and running on your local machine:

1. **Clone this repository:**
   git clone https://github.com/Olabayoji/dockerTutorial-Container-Communication.git

2. **Navigate to the project directory:**
   cd dockerTutorial-ContainerCommunication

3. **Build the Docker image:**
   docker build -t docker-complete .

4. **Run the Docker container:**
   docker run -p 3000:3000 docker-complete

## Usage

### API Endpoints

- `GET /favorites`: Retrieve all favorites stored in the database.
- `POST /favorites`: Add a new favorite. Requires a JSON object with `name`, `type`, and `url`.
- Example:

```json
{
  "name": "Luke Skywalker",
  "type": "character",
  "url": "https://swapi.dev/api/people/1/"
}
```

- `GET /movies`: Retrieve Star Wars movies data from SWAPI.
- `GET /people`: Retrieve Star Wars characters data from SWAPI.

## Dependencies

- [Express](https://www.npmjs.com/package/express) - Web framework for Node.js
- [Body-parser](https://www.npmjs.com/package/body-parser) - Middleware for parsing JSON
- [Axios](https://www.npmjs.com/package/axios) - HTTP client for Node.js
- [Mongoose](https://www.npmjs.com/package/mongoose) - MongoDB object modeling tool
