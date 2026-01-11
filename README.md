# Album API: HW1a

A simple REST API built with Go and Gin for CS 6650: Scalable Distributed Systems.

## How to Run

1. Make sure Go is installed
2. Navigate to the project folder
3. Run:
```
   go get .
   go run .
```
4. Server starts at `localhost:8080`

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /albums | Returns all albums |
| GET | /albums/:id | Returns a specific album |
| POST | /albums | Adds a new album |

## Testing with curl

Get all albums:
```
curl http://localhost:8080/albums
```

Get album by ID:
```
curl http://localhost:8080/albums/2
```

Add new album:
```
curl http://localhost:8080/albums --header "Content-Type: application/json" --request "POST" --data '{"id": "4","title": "Kind of Blue","artist": "Miles Davis","price": 29.99}'
```

## Notes

This uses in-memory storage for learning purposes. In a real distributed system, a shared database would be needed so all servers can access the same data.
