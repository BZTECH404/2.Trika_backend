# Trika Backend

**Trika Backend** is a RESTful API built with **Express.js**, designed to manage users, carousel items, motivational content, services, about sections, testimonials, contacts, blogs, and yoga services. The application integrates with **AWS services** and **Docker** for deployment.

## Table of Contents

1. [**Installation**](#installation)
2. [**API Endpoints**](#api-endpoints)
3. [**Error Handling**](#error-handling)
4. [**Deployment**](#deployment)
5. [**Scripts**](#scripts)
6. [**Dependencies**](#dependencies)
7. [**Development**](#development)

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/BZTECH404/Trika_backend.git
   cd Trika_backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Environment Variables**:
   Create a `.env` file in the root directory with the following variables:
   ```env
   PORT=8000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   AWS_ACCESS_KEY_ID=your_aws_access_key_id
   AWS_SECRET_ACCESS_KEY=your_aws_secret_access_key
   S3_BUCKET_NAME=your_s3_bucket_name
   ```

4. **Run the application**:
   ```bash
   npm start
   ```

---

## API Endpoints

### User Routes
- **Endpoint**: `/api/user`
- **Description**: Manage user operations.
- **Methods**:
  - **GET**: Retrieve user data.
  - **POST**: Create a new user.
  - **PUT**: Update user data.
  - **DELETE**: Delete a user.

### Carousel Routes
- **Endpoint**: `/api/carousel`
- **Description**: Manage carousel items.
- **Methods**:
  - **GET**: Retrieve carousel items.
  - **POST**: Add new carousel item.
  - **PUT**: Update carousel item.
  - **DELETE**: Delete carousel item.

### Motivation Routes
- **Endpoint**: `/api/motivation`
- **Description**: Manage motivational content.
- **Methods**:
  - **GET**: Retrieve motivational content.
  - **POST**: Add new content.
  - **PUT**: Update content.
  - **DELETE**: Delete content.

### Service Routes
- **Endpoint**: `/api/service`
- **Description**: Manage services.
- **Methods**:
  - **GET**: Retrieve services.
  - **POST**: Add new service.
  - **PUT**: Update service.
  - **DELETE**: Delete service.

### About Routes
- **Endpoint**: `/api/about`
- **Description**: Manage about sections and testimonials.
- **Methods**:
  - **GET**: Retrieve about sections.
  - **POST**: Add new section.
  - **PUT**: Update section.
  - **DELETE**: Delete section.

### Contact Routes
- **Endpoint**: `/api/contact`
- **Description**: Manage contact information.
- **Methods**:
  - **GET**: Retrieve contact information.
  - **POST**: Add new contact information.
  - **PUT**: Update contact information.
  - **DELETE**: Delete contact information.

### Blog Routes
- **Endpoint**: `/api/blog`
- **Description**: Manage blog posts.
- **Methods**:
  - **GET**: Retrieve blog posts.
  - **POST**: Add new blog post.
  - **PUT**: Update blog post.
  - **DELETE**: Delete blog post.

### Yoga Service Routes
- **Endpoint**: `/api/yoga`
- **Description**: Manage yoga services.
- **Methods**:
  - **GET**: Retrieve yoga services.
  - **POST**: Add new yoga service.
  - **PUT**: Update yoga service.
  - **DELETE**: Delete yoga service.

---

## Error Handling

- Errors are logged using **Winston**.
- Errors are sent to the client with a `500` status and an appropriate error message.

---

## Deployment

### Docker

1. **Build Docker image**:
   ```bash
   docker build -t trika-backend .
   ```

2. **Run Docker container**:
   ```bash
   docker run -p 8000:8000 -d trika-backend
   ```

### AWS

- The application uses **AWS services** such as **S3** for storage and is configured for deployment with **AWS ECR** and **Serverless** framework.

---

## Scripts

- **Start**:
  ```bash
  npm start
  ```
- **Deploy**:
  ```bash
  npm run deploy
  ```
- **Dev**:
  ```bash
  npm run dev
  ```

---

## Dependencies

- **Express**: Web framework.
- **Cors**: Middleware for enabling CORS.
- **Mongoose**: MongoDB ORM.
- **AWS SDK**: AWS services integration.
- **Nodemailer**: Email handling.
- **JsonWebToken**: Token-based authentication.
- **Winston**: Logging.

---

## Development

- The application is set up for development with **Nodemon** for live-reloading.
- For more detailed information, refer to the code comments and the documentation provided within each module.

