# Django App Builder Prompt for tf-smart-prompt API Frontend

## Overview
You are an AI developer tasked with building a Django web application that serves as the front end for the tf-smart-prompt API. The goal is to create a user-friendly interface that fetches and displays data from the API. This project should include proper error handling, clear code documentation, and instructions for deployment.

## Requirements
1. **Project Initialization:**
   - Create a new Django project named `SmartPromptFrontend`.
   - Within this project, create a Django app called `api_front`.

2. **Configuration:**
   - Add `api_front` to the `INSTALLED_APPS` in the project’s settings.
   - Configure any environment variables or settings needed to connect to the tf-smart-prompt API.

3. **OpenAPI Documentation:**
   - The smartprompt-api repository already contains an `OpenAPI.json` file that documents the API endpoints, request/response formats, and data structures.
   - Make sure to review and refer to this documentation as you implement the API calls to ensure proper integration and handling of the data.

4. **URL Routing:**
   - In the main `urls.py`, include the URL routing for the `api_front` app.
   - In `api_front/urls.py`, create routes for:
     - An index view (e.g., `/`) that displays a summary of data from the API.
     - A detail view (e.g., `/detail/<id>/`) to show individual record details, if applicable.

5. **Views:**
   - Create an index view in `api_front/views.py` that:
     - Makes an HTTP GET request to the tf-smart-prompt API endpoint.
     - Parses the JSON response.
     - Renders an HTML template with the fetched data.
   - Create a detail view (if needed) that:
     - Fetches additional data for a given item from the API using its identifier.
     - Renders a detail template.
   - Use Python’s `requests` library (or Django’s built-in tools) to interact with the API.
   - Implement error handling to manage API request failures.

6. **Templates:**
   - In `api_front/templates/api_front/`, create:
     - An `index.html` template to display a list or summary of data.
     - A `detail.html` template (if applicable) to display detailed information.
   - Use Django’s templating language to loop through and render API data.

7. **Static Files & Front-End:**
   - Set up static file handling to include CSS and JavaScript to enhance the UI.
   - Ensure the front end is clean, responsive, and user-friendly.

8. **Testing & Documentation:**
   - Write tests in `api_front/tests.py` to verify that the views correctly fetch and display data from the API.
   - Include inline comments and a `README.md` that explains:
     - How to install dependencies.
     - How to perform database migrations.
     - How to run the development server.
     - Any additional deployment considerations.

## Example Code Snippets

### Project Initialization
