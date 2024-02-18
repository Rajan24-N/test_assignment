# test_assignment
Read the README file for event management using FLASK

# Event Management Application

This is a simple Python backend application that allows users to manage events. It provides REST APIs for creating, viewing, updating, and deleting events.

## Setup Instructions

1. **Install Python**: Make sure you have Python installed on your system. You can download and install Python from the [official Python website](https://www.python.org/downloads/).

2. **Install Visual Studio Code (VSCode)**: If you haven't already, download and install Visual Studio Code from the [official website](https://code.visualstudio.com/).

3. **Open VSCode**: Launch Visual Studio Code.

4. **Create a New Folder**: Create a new folder for your project where you'll store your Python files.

5. **Open Terminal**: In VSCode, open the integrated terminal. You can do this by selecting `Terminal` > `New Terminal` from the menu.

6. **Create a Virtual Environment**: It's a good practice to create a virtual environment for your Python projects to isolate dependencies. In the terminal, run the following command to create a virtual environment named `venv`:

    ```
    python -m venv venv
    ```

7. **Activate the Virtual Environment**: Activate the virtual environment. In the terminal, run the appropriate command based on your operating system:

    For Windows:
    ```
    venv\Scripts\activate
    ```

    For macOS/Linux:
    ```
    source venv/bin/activate
    ```

8. **Install Flask**: With the virtual environment activated, you can now install Flask using pip, Python's package installer. In the terminal, run:

    ```
    pip install Flask
    pip install pymysql
    pip install pytest
    pip install flask2postman


    ```

9. **Create Python Files**: In your VSCode project folder, create a new Python file named `app.py`.

10. **Copy the Flask Code**: Copy the Flask code provided in the `app.py` file from this repository.

11. **Create `events.json` File**: Create a new file named `events.json` in the same folder as `app.py` and paste the following content into it:

    ```json
    []
    ```

12. **Create a README.md File**: Create a new file named `README.md` in the project folder. Paste the README content provided below into this file.

13. **Adjust README Content**: Adjust the README content as needed, replacing placeholders like `<repository_url>` and `link/to/postman/collection` with appropriate values.

14. **Save Changes**: Save all the files you've created or modified in VSCode.

## Running the Application

1. **Run the Flask Application**: In the terminal, navigate to your project folder if you're not already there. Then, run the following command to start the Flask application:

    ```
    python app.py
    ```

## Endpoints

Here are the endpoints provided by the application:

### Create Event

- **URL:** `/events`
- **Method:** `POST`
- **Request Body:**
    ```json
    {
        "title": "Event Title",
        "description": "Event Description",
        "start_time": "2024-02-17 09:00:00",
        "end_time": "2024-02-17 10:00:00"
    }
    ```
- **Response:**
    ```json
    {
        "title": "Event Title",
        "description": "Event Description",
        "start_time": "2024-02-17 09:00:00",
        "end_time": "2024-02-17 10:00:00"
    }
    ```

### View All Events

- **URL:** `/event`
- **Method:** `GET`
- **Response:**
    ```json
    [
        {
            "title": "Event Title",
            "description": "Event Description",
            "start_time": "2024-02-17 09:00:00",
            "end_time": "2024-02-17 10:00:00"
        }
    ]
    ```

### Update Event

- **URL:** `/events/<event_id>`
- **Method:** `PUT`
- **Request Body:**
    ```json
    {
        "title": "Updated Event Title",
        "description": "Updated Event Description"
    }
    ```
- **Response:**
    ```json
    {
        "title": "Updated Event Title",
        "description": "Updated Event Description",
        "start_time": "2024-02-17 09:00:00",
        "end_time": "2024-02-17 10:00:00"
    }
    ```

### Delete Event

- **URL:** `/events/<event_id>`
- **Method:** `DELETE`
- **Response:**
    ```json
    {
        "message": "Event deleted"
    }
    ```

## Postman Collection

You can import the Postman collection file provided with this repository to test the endpoints.
flask2postman your_flask_app.app --name "Your Collection Name" > postman_collection.json

For CURL commands encoded for credentials use this:
import base64
username = 'demo'
password = 'demo'
auth_string = base64.b64encode(f'{username}:{password}'.encode()).decode()
ZGVtbzpkZW1v


## CURL DEMO COMMANDS
curl -X POST -H "Content-Type: application/json" -H "Authorization: Basic ZGVtbzpkZW1v" -d "{\"title\":\"Meeting\", \"description\":\"Discuss project updates\", \"start_time\":\"2024-02-17 09:00:00\", \"end_time\":\"2024-02-17 10:00:00\"}" http://localhost:5000/event

