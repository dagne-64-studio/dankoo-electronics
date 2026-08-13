# DANKOO ELECTRONICS - API Reference

## Base URL

```
http://localhost:3001/api
```

## Authentication

Use JWT tokens in the Authorization header:

```
Authorization: Bearer <token>
```

## Authentication Endpoints

### Register User

```
POST /auth/register
```

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "SecurePassword123!",
  "firstName": "John",
  "lastName": "Doe"
}
```

**Response:**
```json
{
  "id": "uuid",
  "email": "user@example.com",
  "firstName": "John",
  "lastName": "Doe",
  "token": "jwt_token",
  "refreshToken": "refresh_token"
}
```

### Login

```
POST /auth/login
```

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "SecurePassword123!"
}
```

### Logout

```
POST /auth/logout
```

### Refresh Token

```
POST /auth/refresh
```

## Products Endpoints

### List Products

```
GET /products?page=1&limit=20&category=uuid&brand=uuid&minPrice=0&maxPrice=100000&rating=3&sort=newest
```

**Response:**
```json
{
  "data": [
    {
      "id": "uuid",
      "sku": "HP-LPT-001",
      "name": "HP ProBook 450 G10",
      "slug": "hp-probook-450-g10",
      "description": "Professional laptop",
      "price": 50000,
      "discountPrice": 45000,
      "rating": 4.5,
      "reviewCount": 25,
      "isFeatured": true,
      "images": ["url1", "url2"]
    }
  ],
  "total": 100,
  "page": 1,
  "limit": 20
}
```

### Get Product Details

```
GET /products/:id
```

### Search Products

```
GET /products/search?q=laptop&limit=10
```

### Create Product (Admin)

```
POST /products
```

**Request Body:**
```json
{
  "sku": "HP-LPT-001",
  "name": "HP ProBook 450 G10",
  "description": "Professional laptop",
  "categoryId": "uuid",
  "brandId": "uuid",
  "price": 50000,
  "discountPrice": 45000,
  "metaTitle": "HP ProBook 450 G10",
  "metaDescription": "Professional laptop for business",
  "specifications": {
    "cpu": "Intel i7",
    "ram": "16GB",
    "storage": "512GB SSD"
  }
}
```

### Update Product (Admin)

```
PATCH /products/:id
```

### Delete Product (Admin)

```
DELETE /products/:id
```

## Categories Endpoints

### List Categories

```
GET /categories
```

### Create Category (Admin)

```
POST /categories
```

### Update Category (Admin)

```
PATCH /categories/:id
```

### Delete Category (Admin)

```
DELETE /categories/:id
```

## Shopping Cart Endpoints

### Get Cart

```
GET /cart
```

### Add to Cart

```
POST /cart/items
```

**Request Body:**
```json
{
  "productId": "uuid",
  "quantity": 1
}
```

### Update Cart Item

```
PATCH /cart/items/:id
```

**Request Body:**
```json
{
  "quantity": 2
}
```

### Remove from Cart

```
DELETE /cart/items/:id
```

## Orders Endpoints

### Create Order

```
POST /orders
```

**Request Body:**
```json
{
  "customerName": "John Doe",
  "customerEmail": "john@example.com",
  "customerPhone": "+251912345678",
  "deliveryAddress": "Main Street 123",
  "city": "Addis Ababa",
  "region": "Addis Ababa",
  "country": "Ethiopia",
  "paymentMethod": "chapa",
  "couponCode": "SAVE10"
}
```

### Get User Orders

```
GET /orders
```

### Get Order Details

```
GET /orders/:id
```

### Update Order (Admin)

```
PATCH /orders/:id
```

**Request Body:**
```json
{
  "status": "confirmed"
}
```

## Reviews Endpoints

### Get Product Reviews

```
GET /products/:id/reviews
```

### Create Review

```
POST /products/:id/reviews
```

**Request Body:**
```json
{
  "rating": 5,
  "title": "Excellent product",
  "content": "Very satisfied with this purchase"
}
```

## Wishlist Endpoints

### Get Wishlist

```
GET /wishlist
```

### Add to Wishlist

```
POST /wishlist
```

**Request Body:**
```json
{
  "productId": "uuid"
}
```

### Remove from Wishlist

```
DELETE /wishlist/:id
```

## AI Assistant Endpoints

### Get Recommendations

```
POST /ai/recommend
```

**Request Body:**
```json
{
  "budget": 50000,
  "purpose": "programming",
  "category": "laptops"
}
```

### Compare Products

```
POST /ai/compare
```

**Request Body:**
```json
{
  "productIds": ["uuid1", "uuid2", "uuid3"]
}
```

## Admin Endpoints

### Dashboard Stats

```
GET /admin/stats
```

### Sales Analytics

```
GET /admin/analytics/sales?startDate=2024-01-01&endDate=2024-12-31
```

### Inventory Management

```
GET /admin/inventory
PATCH /admin/inventory/:id
```

## Error Responses

```json
{
  "statusCode": 400,
  "message": "Error message",
  "error": "Bad Request"
}
```

## Status Codes

- `200` - Success
- `201` - Created
- `400` - Bad Request
- `401` - Unauthorized
- `403` - Forbidden
- `404` - Not Found
- `500` - Server Error
