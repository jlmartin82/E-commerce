# E-Commerce Back End with Object-Relational Mapping (ORM)

Welcome to the E-Commerce Back End project! In this project, you'll build the backend for an e-commerce site using Express.js and Sequelize to interact with a MySQL database. The goal is to create a robust and functional API that handles various CRUD (Create, Read, Update, Delete) operations for categories, products, and tags.

## Table of Contents

- [Introduction](#e-commerce-back-end-with-object-relational-mapping-orm)
- [Walkthrough](#walkthrough)
- [Getting Started](#getting-started)
- [Database Models](#database-models)
- [Associations](#associations)
- [API Routes](#api-routes)
- [Seeding the Database](#seeding-the-database)
- [Syncing Sequelize to Database](#syncing-sequelize-to-database)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Walkthrough

[Ecomm Aug 12, 2023 3_33 PM.webm](https://github.com/jlmartin82/E-commerce/assets/129562637/479db70f-9800-41d0-996d-8c98627ec371)




[Ecommerc.webm](https://github.com/jlmartin82/E-commerce/assets/129562637/c8c2bee2-4425-44ba-bb11-f9a6e4464991)




## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies using `npm install`.
3. Create a `.env` file in the project root directory and add your MySQL username, password, and database name as environment variables:
4. Create your database using the provided `schema.sql` file.

## Database Models

This project requires the following database models with specific attributes:

- **Category**
  - id (Integer, Primary Key)
  - category_name (String, Not Null)

- **Product**
  - id (Integer, Primary Key)
  - product_name (String, Not Null)
  - price (Decimal, Not Null)
  - stock (Integer, Not Null, Default: 10)
  - category_id (Integer, Foreign Key referencing Category)

- **Tag**
  - id (Integer, Primary Key)
  - tag_name (String)

- **ProductTag**
  - id (Integer, Primary Key)
  - product_id (Integer, Foreign Key referencing Product)
  - tag_id (Integer, Foreign Key referencing Tag)

## Associations

This project requires the following associations between the models:

- A product belongs to a category, and a category can have many products.
- A product belongs to many tags, and a tag belongs to many products.

## API Routes

Complete the API routes in `product-routes.js`, `tag-routes.js`, and `category-routes.js` to perform CRUD operations using Sequelize models.

## Seeding the Database

After creating the models and routes, use the command `npm run seed` to seed the database with initial data.

## Syncing Sequelize to Database

The Sequelize models should be synced with the MySQL database on server start. Ensure that your `server.js` file includes the necessary code to achieve this.

## Usage

1. Install the dependencies: `npm install`
2. Create the `.env` file and set your database credentials.
3. Create the database using `schema.sql`.
4. Seed the database using `npm run seed`.
5. Start the server: `npm start`
6. Use a tool like [Insomnia](https://insomnia.rest/) or [Postman](https://www.postman.com/) to test the API endpoints.

## Contributing

Contributions are welcome! If you find any issues or have improvements to suggest, feel free to create a pull request.

## License

This project is licensed under the [MIT License](LICENSE).











