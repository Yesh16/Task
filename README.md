# Task Management API

This is a RESTful API for managing tasks in a Task Management Application built with Node.js, Express, and MongoDB.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/task-manager.git
    cd task-manager
    ```

2. **Install dependencies:**
    ```sh
    npm install
    ```

3. **Set up environment variables:**
    Create a `.env` file in the root of your project and add the following:
    ```env
    MONGODB_URI=mongodb://localhost:27017/taskmanager
    PORT=3000
    ```

4. **Start the server:**
    ```sh
    node server.js
    ```

The server should now be running at `http://localhost:3000`.

## Usage

You can use tools like Postman to test the API endpoints. Below are the available endpoints.

## API Endpoints

### Create a new task

- **URL:** `/tasks`
- **Method:** `POST`
- **Body:**
    ```json
    {
        "title": "Task title",
        "description": "Task description",
        "status": "pending"
    }
    ```
- **Success Response:**
    - **Code:** `201 CREATED`
    - **Content:**
        ```json
        {
            "_id": "task_id",
            "title": "Task title",
            "description": "Task description",
            "status": "pending",
            "createdAt": "2023-12-09T05:30:00.000Z"
        }
        ```

### Get all tasks

- **URL:** `/tasks`
- **Method:** `GET`
- **Success Response:**
    - **Code:** `200 OK`
    - **Content:**
        ```json
        [
            {
                "_id": "task_id",
                "title": "Task title",
                "description": "Task description",
                "status": "pending",
                "createdAt": "2023-12-09T05:30:00.000Z"
            }
        ]
        ```

### Get a single task by ID

- **URL:** `/tasks/:id`
- **Method:** `GET`
- **Success Response:**
    - **Code:** `200 OK`
    - **Content:**
        ```json
        {
            "_id": "task_id",
            "title": "Task title",
            "description": "Task description",
            "status": "pending",
            "createdAt": "2023-12-09T05:30:00.000Z"
        }
        ```

### Update a task by ID

- **URL:** `/tasks/:id`
- **Method:** `PATCH`
- **Body:**
    ```json
    {
        "title": "Updated title",
        "description": "Updated description",
        "status": "completed"
    }
    ```
- **Success Response:**
    - **Code:** `200 OK`
    - **Content:**
        ```json
        {
            "_id": "task_id",
            "title": "Updated title",
            "description": "Updated description",
            "status": "completed",
            "createdAt": "2023-12-09T05:30:00.000Z"
        }
        ```

### Delete a task by ID

- **URL:** `/tasks/:id`
- **Method:** `DELETE`
- **Success Response:**
    - **Code:** `200 OK`
    - **Content:**
        ```json
        {
            "_id": "task_id",
            "title": "Task title",
            "description": "Task description",
            "status": "pending",
            "createdAt": "2023-12-09T05:30:00.000Z"
        }
        ```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
