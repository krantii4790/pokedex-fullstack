# Pokemon Search Engine - Pokedex

## Overview

Pokemon Search Engine is a full-stack web application that allows users to search for Pokémon by name and view detailed information about them.

The application consists of:

* **Spring Boot Backend** (REST API)
* **React + Vite Frontend** (User Interface)

The backend fetches Pokémon data from the official PokeAPI and uses an in-memory caching mechanism to improve performance for repeated requests.

---

## Features

### Backend

* RESTful API built using Spring Boot
* Integration with the official PokeAPI
* In-memory caching for faster repeated searches
* Cache expiry and maximum cache size configuration
* Proper error handling and response management
* Clean layered architecture (Controller → Service → Client → Cache)

### Frontend

* Search Pokémon by name
* Display Pokémon image
* Display Pokémon types
* Display Pokémon abilities
* Display Pokémon stats
* Display Pokémon moves
* Responsive and user-friendly UI
* React-based component architecture

---

## Tech Stack

### Backend

* Java 17
* Spring Boot
* Maven
* REST APIs
* Caffeine Cache

### Frontend

* React.js
* Vite
* Axios
* HTML5
* CSS3

### External API

* PokeAPI
* https://pokeapi.co/

---

## Project Structure

```
pokedex-fullstack
│
├── pokedex-backend
│   ├── controller
│   ├── service
│   ├── client
│   ├── cache
│   ├── model
│   └── resources
│
├── pokedex-frontend
│   ├── src
│   ├── components
│   ├── api
│   └── assets
│
└── README.md
```

---

## API Endpoint

### Get Pokemon Details

```http
GET /api/pokemon/{name}
```

### Example

```http
GET /api/pokemon/pikachu
```

### Sample Response

```json
{
  "id": 25,
  "name": "pikachu",
  "height": 4,
  "weight": 60,
  "types": ["electric"]
}
```

---

## Caching Strategy

The backend implements an in-memory caching mechanism to improve response time.

### Cache Features

* Cache Key: Pokémon Name
* Automatic Expiry (TTL)
* Maximum Cache Entries
* Faster repeated searches
* Reduced external API calls

---

## Running the Project Locally

### Backend Setup

Navigate to backend folder:

```bash
cd pokedex-backend
```

Run application:

```bash
./mvnw spring-boot:run
```

Or:

```bash
mvn spring-boot:run
```

Backend runs on:

```text
http://localhost:7272
```

---

### Frontend Setup

Navigate to frontend folder:

```bash
cd pokedex-frontend
```

Install dependencies:

```bash
npm install
```

Run application:

```bash
npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

## Testing

Try searching the following Pokémon:

* pikachu
* charizard
* bulbasaur
* squirtle
* eevee
* gengar
* dragonite
* mewtwo
* snorlax
* lucario

---

## Design Considerations

* Clean REST API design
* Layered architecture
* Performance optimization through caching
* Extensible code structure
* Separation of concerns
* Responsive UI

---

## Future Enhancements

* Search suggestions/autocomplete
* Pokemon comparison feature
* Advanced filtering by type
* Pagination support
* Persistent cache using Redis
* Docker deployment

---

## GitHub Repository

Repository Link:

```text
https://github.com/Krantikumar4211/pokedex-fullstack
```

---

## Author

**Krantikumar Dilip Patil**

B.Tech Artificial Intelligence & Data Science

GitHub:
https://github.com/Krantikumar4211
