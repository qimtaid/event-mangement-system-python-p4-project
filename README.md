# Event Management System

## Overview
This Event Management System is a full-stack web application that allows users to create, view, edit, and delete events. The backend is built with Flask, while the frontend is developed using React. This project serves as a template for understanding and implementing a full-stack application.

## Features
- Create new events
- View a list of all events
- Edit existing events
- Delete events

## Technologies Used
### Backend
- Flask
- Flask-CORS
- Flask-RESTful
- Flask-SQLAlchemy
- Flask-Migrate

### Frontend
- React
- Axios
- React Router DOM

## Setup Instructions

### Backend Setup

1. **Clone the repository**:
    ```bash
    git clone <repository_url>
    cd <repository_name>/server
    ```

2. **Install dependencies**:
    ```bash
    pipenv install
    ```

3. **Activate the virtual environment**:
    ```bash
    pipenv shell
    ```

4. **Initialize the database**:
    ```bash
    flask db init
    flask db migrate -m "Initial migration"
    flask db upgrade
    ```

5. **Run the Flask server**:
    ```bash
    python app.py
    ```
    The server will run on `http://localhost:5555`.

### Frontend Setup

1. **Navigate to the client directory**:
    ```bash
    cd ../client
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Start the React application**:
    ```bash
    npm start
    ```
    The client will run on `http://localhost:3000`.

## Directory Structure
```
project-root/
├── server/
│   ├── app.py
│   ├── config.py
│   ├── models.py
│   ├── resources/
│   │   ├── __init__.py
│   │   ├── event.py
│   ├── seed.py
│   ├── migrations/
│   └── instance/
│       └── app.db
├── client/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── EventForm.js
│   │   │   ├── EventList.js
│   │   ├── App.js
│   │   ├── index.js
│   └── package.json
```

## API Endpoints

### Event Endpoints
- `GET /events` - Retrieve a list of all events.
- `POST /events` - Create a new event.
- `GET /events/:id` - Retrieve a single event by its ID.
- `PUT /events/:id` - Update an existing event by its ID.
- `DELETE /events/:id` - Delete an event by its ID.

## Components

### Backend
- **app.py**: Initializes the Flask application and sets up the API routes.
- **config.py**: Configuration for the Flask application, including the database setup.
- **models.py**: Defines the Event model.
- **resources/event.py**: Contains the API resources for managing events (CRUD operations).

### Frontend
- **src/App.js**: Defines the main routes of the React application.
- **src/components/EventList.js**: Displays a list of events and links to add/edit events.
- **src/components/EventForm.js**: Form for adding and editing events.

## Usage
1. Start the backend server.
2. Start the frontend client.
3. Navigate to `http://localhost:3000` to use the application.

## Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.