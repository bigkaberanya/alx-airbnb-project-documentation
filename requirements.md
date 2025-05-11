# í³„ Backend Requirement Specifications

## í·© 1. User Authentication

### í³Œ Feature Overview:
Enables users (Guests and Hosts) to register, log in, and manage sessions securely.

### í´— API Endpoints:
- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/auth/profile`
- `PUT /api/auth/profile`
- `POST /api/auth/logout`

### í³¥ Input Specification:
#### Registration (`/register`)
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "strongpassword",
  "role": "guest"
}
{
  "email": "john@example.com",
  "password": "strongpassword"
}
{
  "token": "jwt-token-string",
  "user": {
    "id": "123",
    "email": "john@example.com",
    "role": "guest"
  }
}
{
  "title": "Cozy Apartment",
  "description": "Nice place near the city center.",
  "location": "Kigali",
  "price": 50,
  "amenities": ["wifi", "pool"],
  "max_guests": 4
}
{
  "id": "p_001",
  "title": "Cozy Apartment",
  "host_id": "u_001",
  "created_at": "2025-05-11T10:00:00Z"
}
{
  "property_id": "p_001",
  "start_date": "2025-06-01",
  "end_date": "2025-06-05"
}
{
  "booking_id": "b_001",
  "status": "confirmed",
  "total_price": 250
}

---


