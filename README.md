# Django REST Framework JWT UUID Authentication

## Overview
This project implements JWT (JSON Web Tokens) authentication in a Django REST Framework application using UUIDs (Universally Unique Identifiers) for user identifiers instead of the traditional integer IDs. This approach enhances security by making user IDs less predictable.

## Features
- User registration with UUIDs
- JWT authentication for secure API access
- JSON responses for authentication success and failure
- Middleware to handle JWT in requests

## Getting Started

### Prerequisites
- Python 3.x
- Django 3.x or higher
- Django REST Framework
- PyJWT

### Installation Steps
1. **Clone the repository:**
   ```bash
   git clone https://github.com/abdumannon-rabbimqulov/drf_jwt_uuid2.git
   cd drf_jwt_uuid2
   ```  
2. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```  
3. **Run database migrations:**
   ```bash
   python manage.py migrate
   ```  
4. **Create a superuser (optional):**
   ```bash
   python manage.py createsuperuser
   ```  
5. **Run the server:**
   ```bash
   python manage.py runserver
   ```

### Usage
- Register a new user:
  - Endpoint: `/api/register/`
  - Method: `POST`
  - Payload Example:
    ```json
    {
      "username": "myusername",
      "password": "mypassword"
    }
    ```

- Obtain JWT token:
  - Endpoint: `/api/token/`
  - Method: `POST`
  - Payload Example:
    ```json
    {
      "username": "myusername",
      "password": "mypassword"
    }
    ```

- Protected endpoint example:
  - Use the token received above in the `Authorization` header as `Bearer <token>`.

## Contributing
Contributions are welcome. Please open an issue for any feature requests or bugs.

## License
This project is licensed under the MIT License.