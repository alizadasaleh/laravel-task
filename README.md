
# Task Management API

## Project Overview

This Laravel project provides a simple yet powerful API for managing tasks. It allows for creating, reading, updating, and deleting tasks, as well as filtering tasks by status or date.

## Installation

### Prerequisites

- PHP >= 7.3
- Composer
- MySQL or any other database supported by Laravel

### Steps

1. Clone the repository:
   ```
   git clone https://github.com/alizadasaleh/laravel-task.git
   ```

2. Change into the project directory:
   ```
   cd example-app
   ```

3. Install dependencies:
   ```
   composer install
   ```

4. Copy `.env.example` to `.env` and configure your environment:
   ```
   cp .env.example .env
   ```

5. Generate an application key:
   ```
   php artisan key:generate
   ```

6. Create a database and update the `.env` file with your database credentials.

7. Run migrations:
   ```
   php artisan migrate
   ```

8. Start the server:
   ```
   php artisan serve
   ```
   The API will be available at `http://localhost:8000/api`.

## API Endpoints

### Create a Task

- **POST** `/api/tasks`
- Body:
  ```json
  {
    "title": "Task Title",
    "description": "Task Description",
    "status": "new"
  }
  ```

### List Tasks

- **GET** `/api/tasks`

### Get a Specific Task

- **GET** `/api/tasks/{taskId}`

### Update a Task

- **PUT** `/api/tasks/{taskId}`
- Body:
  ```json
  {
    "title": "New Task Title",
    "description": "New Task Description",
    "status": "completed"
  }
  ```

### Delete a Task

- **DELETE** `/api/tasks/{taskId}`

### Filter Tasks

- **GET** `/api/tasks?status=new&date=2024-03-11`

## Usage

Here are some examples of how to use the API:

### Creating a Task

```bash
curl -X POST http://localhost:8000/api/tasks      -H "Content-Type: application/json"      -d '{"title": "Write README", "description": "Write README for the project", "status": "new"}'
```

### Listing Tasks

```bash
curl -X GET http://localhost:8000/api/tasks
```

Refer to the API Endpoints section for more examples.

## Contributing

We welcome contributions! Please open an issue or submit a pull request for any changes.

## License

This project is open-sourced software licensed under the [MIT license](LICENSE.md).
