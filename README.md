# Node-API Project

## Overview

This project is a Node.js API that allows users to view, edit, delete posts, update user statuses, and manage user authentication including registration and login. The project has been implemented using three different methods: HTTP, Socket.io, and GraphQL. User actions are authorized using JSON Web Tokens (JWT).

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Usage](#usage)
  - [HTTP Endpoints](#http-endpoints)
  - [Socket.io Implementation](#socketio-implementation)
  - [GraphQL Implementation](#graphql-implementation)
- [Authentication](#authentication)
- [License](#license)

## Features

- **View Posts**: Retrieve a list of all posts.
- **Edit Posts**: Edit existing posts.
- **Delete Posts**: Delete specific posts.
- **Update User Status**: Update the status of a user.
- **User Management**: Register and login users.
- **Authorization**: Secure actions with JSON Web Tokens (JWT).

## Technologies Used

- Node.js
- Express.js
- Socket.io
- GraphQL
- MongoDB
- Mongoose
- Body-parser
- JSON Web Tokens (JWT)
- Nodemon (for development)

## Usage

### HTTP Endpoints

- **GET /feed/posts**
- **POST /feed/post**
- **GET /feed/post/:postId**
- **PUT /feed/post/:postId**
- **DELETE /feed/post/:postId**
- **PATCH /auth/status**
- **POST /auth/signup**: Register a new user.
- **POST /auth/login**: Login an existing user.

### Socket.io Implementation

To use the Socket.io implementation, ensure that the Socket.io server is running and the client is connected.

#### Events

- **postCreated**: Emitted when a new post is created.
- **postUpdated**: Emitted when a post is updated.
- **postDeleted**: Emitted when a post is deleted.
- **statusUpdated**: Emitted when a user status is updated.
- **userSignedUp**: Emitted when a new user signs up.
- **userLoggedIn**: Emitted when a user logs in.

### GraphQL Implementation

The GraphQL API allows for more flexible queries and mutations.

#### Queries

- **getPosts**: Retrieve a list of all posts.
- **getPost(id: ID!)**: Retrieve a specific post by ID.

#### Mutations

- **createPost(input: PostInput!)**: Create a new post.
- **updatePost(id: ID!, input: PostInput!)**: Update an existing post.
- **deletePost(id: ID!)**: Delete a specific post.
- **updateUserStatus(id: ID!, status: String!)**: Update the status of a user.
- **signupUser(input: UserInput!)**: Register a new user.
- **loginUser(input: LoginInput!)**: Login an existing user.

## Authentication

This project uses JSON Web Tokens (JWT) to authorize user actions. Upon successful login, a JWT is issued to the user, which must be included in the Authorization header of subsequent requests to access protected endpoints.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
