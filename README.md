# Node Backend CRUD (Node.js + Express + MongoDB)

A beginner REST API for managing **products**, built with Node.js, Express and Mongoose (MongoDB Atlas), using the model / route / controller pattern.

## Project structure
```
index.js                          # server + DB connection
models/product.model.js           # Mongoose schema
controllers/product.controller.js # CRUD logic
routes/product.route.js           # route definitions
postman/node-crud.postman_collection.json
.env.example
```

## Setup (macOS)
```bash
# 1. Install Node (skip if installed)
brew install node

# 2. Install dependencies
npm install

# 3. Configure environment
cp .env.example .env
# edit .env and paste your MongoDB Atlas connection string

# 4. Run
npm run dev      # with nodemon (auto-reload)
# or
npm start
```
Expected output: `Connected to database!` and `Server is running on port 3000`.

## API endpoints
| Method | Endpoint            | Description        |
|--------|---------------------|--------------------|
| GET    | /                   | Health message     |
| GET    | /api/products       | List all products  |
| GET    | /api/products/:id   | Get one product    |
| POST   | /api/products       | Create a product   |
| PUT    | /api/products/:id   | Update a product   |
| DELETE | /api/products/:id   | Delete a product   |

Product body: `{ "name": "Keyboard", "quantity": 10, "price": 49.99, "image": "url" }`

## Testing with Postman
Import `postman/node-crud.postman_collection.json`, then set the `id` collection variable after creating a product.
