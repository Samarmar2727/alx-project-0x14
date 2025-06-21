# ALX Project 0x14: Reading API Documentation

## API Overview

The MoviesDatabase API lets you search for movies, TV shows, genres, and people. You can get info like titles, ratings, cast, crew, and similar shows.

## Version

v2

## Available Endpoints

- `/titles`: List of movies and shows.
- `/titles/{id}`: Details of a specific title.
- `/genres`: List of genres.
- `/titles/{id}/cast`: Cast info.
- `/titles/{id}/crew`: Crew info.
- `/titles/{id}/similar`: Similar titles.

## Request and Response Format

**Request:**

````http
GET /titles?titleType=movie&year=2023
Headers:
  X-RapidAPI-Key: YOUR_API_KEY
  X-RapidAPI-Host: moviesdatabase.p.rapidapi.com

**Response:**
```json
{
  "results": [
    {
      "id": "tt1234567",
      "titleText": { "text": "Movie Name" },
      "releaseDate": { "year": 2023 },
      "primaryImage": { "url": "https://example.com/image.jpg" },
      "ratingsSummary": { "aggregateRating": 8.5 }
    }
  ]
}

## Authentication
Use the following headers in every request:

- `X-RapidAPI-Key`: Your personal API key from RapidAPI.
- `X-RapidAPI-Host`: `moviesdatabase.p.rapidapi.com`

## Error Handling
- `401 Unauthorized`: API key is missing or invalid.
- `403 Forbidden`: Access denied due to plan restrictions.
- `404 Not Found`: The requested resource doesn’t exist.
- `429 Too Many Requests`: You exceeded the rate limit.

## Usage Limits and Best Practices
- Respect the rate limits to avoid being blocked.
- Cache responses where possible to reduce load.
- Always check response codes before using data.
- Paginate requests when dealing with large datasets.

````
