#  Optional activities

1. Create two APIs: one for managing "Cars" and another for "Car Buyers."
2. Implement all necessary endpoints for each API, including:
   - Adding a new item
   - Retrieving all items
   - Retrieving a single item
   - Updating an item
   - Deleting an item
3. Test all the endpoints using Postman.

Here are the details for the models:

**Car Model**:

- When a user adds a new car, they will provide the following information in JSON format:
```json
{
  "make": "Toyota",
  "model": "Camry",
  "year": 2022,
  "color": "Silver",
  "price": 25000
}
```
- Each car includes the following attributes:
  - `make` (e.g., "Toyota")
  - `model` (e.g., "Camry")
  - `year` (e.g., 2022)
  - `color` (e.g., "Silver")
  - `price` (e.g., 25000 USD)

**Buyer Model**:

- When a user adds a new Buyer, they will provide the following information in JSON format:
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "123-456-7890",
  "address": "123 Main St",
  "budget": 30000
}
```

- Each car buyer includes the following attributes:
  - `name`
  - `email`
  - `phone`
  - `address`
  - `budget` (e.g., 30000 USD)
  - `purchaseDate` (if applicable)
  - `purchasedCar` (a reference to the car the buyer purchased, if applicable)

