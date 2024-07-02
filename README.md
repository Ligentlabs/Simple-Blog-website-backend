# BlogWebsite

A simple blog website project created using Amplication. This project includes features to manage users, blog posts, comments, and categories, with authentication handled via JWT.

## Features

- User Authentication (Admin access)
- Create, Read, Update, and Delete (CRUD) operations for Posts
- Commenting on Posts
- Categorization of Posts

## Getting Started

### Prerequisites

- Node.js and npm installed
- An Amplication account
- A relational database (e.g., PostgreSQL, MySQL)

### Installation

1. **Clone the repository:**

   git clone https://github.com/your-username/blog-website.git
   cd blog-website

2. **Install dependencies:**

   npm install

3. **Configure environment variables:**
   Create a `.env` file in the root directory and add your configurations. For example:

   DATABASE_URL=your-database-url
   JWT_SECRET=your-jwt-secret

4. **Run the application:**

   npm run start

## Usage

- **Admin Registration and Login:**
  - Admin can register and login to manage the content.
- **Posts Management:**
  - Create, Read, Update, and Delete posts.
- **Commenting:**
  - Users can comment on posts.
- **Categories:**
  - Posts can be categorized using different categories.

## API Endpoints

The REST API for managing the resources includes:

- **User Endpoints:**
  - `POST /auth/login`: Login for users
- **Post Endpoints:**
  - `GET /posts`: Get all posts
  - `POST /posts`: Create a new post
  - `GET /posts/:id`: Get a single post
  - `PUT /posts/:id`: Update a post
  - `DELETE /posts/:id`: Delete a post
- **Comment Endpoints:**
  - `GET /posts/:postId/comments`: Get all comments for a post
  - `POST /posts/:postId/comments`: Create a comment
  - `DELETE /comments/:id`: Delete a comment
- **Category Endpoints:**
  - `GET /categories`: Get all categories

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## To-do

Here's a list of things that can be improved or added:

- Unit tests
- Front-end integration
- Improved error handling
- Advanced user roles and permissions

## License

MIT

## Amplication Setup

To set up this project in Amplication:

1. Create a new project in Amplication
2. Define the following data models (entities):
   - User
   - Post
   - Comment
   - Category
3. Set up the necessary relations between these entities:
   - User to Post (one-to-many)
   - Post to Comment (one-to-many)
   - Post to Category (many-to-many)
4. Configure the API endpoints and permissions as described in the API Endpoints section

Note: While Amplication can generate much of the boilerplate code for your application, you may need to customize some aspects to fully implement all the features described in this README. For example, you might need to add custom logic for user authentication and authorization.
