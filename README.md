# Django CRUD Project Using Function-Based Views

This project demonstrates how to create a Django CRUD (Create, Retrieve, Update, Delete) application using function-based views. The application manages a list of orders.

## Prerequisites

Before you begin, ensure you have the following installed:

1. **Python**: Make sure Python is installed on your system.
2. **Django**: Install Django using pip:
    ```sh
    pip install django
    ```
3. **Database**: This project uses MySQL. Ensure you have MySQL installed and running.
4. **Text Editor or IDE**: Use your preferred code editor, such as Visual Studio Code, PyCharm, or Sublime Text.

## Project Setup

1. **Clone the repository**:
    ```sh
    git clone <repository-url>
    cd django-crud
    ```

2. **Create a virtual environment**:
    ```sh
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. **Install dependencies**:
    ```sh
    pip install -r crudproject/requirements.txt
    ```

4. **Configure the database**:
    Update the database settings in [settings.py](http://_vscodecontentref_/1) to match your MySQL configuration.

5. **Apply migrations**:
    ```sh
    python manage.py makemigrations
    python manage.py migrate
    ```

6. **Run the development server**:
    ```sh
    python manage.py runserver
    ```

## Application Structure

- **crudproject/**: Main project directory.
  - **crudapp/**: Django app for managing orders.
    - **models.py**: Defines the [Orders](http://_vscodecontentref_/2) model.
    - **forms.py**: Defines the [OrderForm](http://_vscodecontentref_/3) form.
    - **views.py**: Contains function-based views for CRUD operations.
    - **urls.py**: URL configurations for the app.
    - **templates/**: HTML templates for the app.
  - **settings.py**: Project settings.
  - **urls.py**: URL configurations for the project.
  - **wsgi.py**: WSGI configuration.
  - **asgi.py**: ASGI configuration.
- **templates/**: Directory for HTML templates.
- **manage.py**: Django's command-line utility.

## CRUD Operations

### Create Order

The [orderFormView](http://_vscodecontentref_/4) function in [views.py](http://_vscodecontentref_/5) handles the creation of new orders. It renders a form and saves the order if the form is valid.

### Read Orders

The [showView](http://_vscodecontentref_/6) function in [views.py](http://_vscodecontentref_/7) retrieves and displays all orders.

### Update Order

The [updateView](http://_vscodecontentref_/8) function in [views.py](http://_vscodecontentref_/9) handles updating an existing order.

### Delete Order

The [deleteView](http://_vscodecontentref_/10) function in [views.py](http://_vscodecontentref_/11) handles deleting an existing order.

## Templates

- **layout.html**: Base template with a navbar.
- **order.html**: Template for creating and updating orders.
- **show.html**: Template for displaying all orders.
- **confirmation.html**: Template for confirming order deletion.

## Running Tests

To run tests, use the following command:
```sh
python manage.py test