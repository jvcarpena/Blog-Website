# Blog Website with Database

This is a Flask-based blog website featuring user authentication, admin privileges, and a SQLite database. The website allows users to create, edit, and delete blog posts, as well as add and manage comments.

## Features
- **User Authentication**: Register, log in, and log out securely.
- **Admin Privileges**: Admins can create, edit, and delete blog posts.
- **Comment System**: Logged-in users can add comments; commenters can delete their own comments.
- **Database Integration**: Uses SQLite for managing users, posts, and comments.
- **Email Contact Form**: Sends contact messages via Gmail.

## Technologies Used
- **Python**: Flask, SQLAlchemy, Flask-Login, Flask-Bootstrap, Flask-CKEditor
- **HTML/CSS**: Bootstrap for UI styling
- **Database**: SQLite
- **Email**: SMTP for sending messages

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the root folder and add the following:
   ```env
   FLASK_KEY=<your-secret-key>
   DB_URI=sqlite:///posts.db
   EMAIL_KEY=<your-email-address>
   PASSWORD_KEY=<your-email-app-password>
   ```

5. Initialize the database:
   ```bash
   flask shell
   >>> from app import db
   >>> db.create_all()
   >>> exit()
   ```

6. Run the app:
   ```bash
   flask run --port=5002
   ```

7. Access the website at `http://127.0.0.1:5002`.

## Routes Overview
- `/`: View all blog posts.
- `/post/<post_id>`: View a specific post with comments.
- `/register`: Register a new account.
- `/login`: Log in to an account.
- `/logout`: Log out of the current account.
- `/new-post`: Create a new blog post (admin-only).
- `/edit-post/<post_id>`: Edit an existing blog post (admin-only).
- `/delete/<post_id>`: Delete a blog post (admin-only).
- `/delete/comment/<comment_id>/<post_id>`: Delete a comment (commenter-only).
- `/about`: View the About page.
- `/contact`: Contact form.

## Notes
- Admin functionality is limited to the user with `id=1`.
- Ensure the `.env` file is configured correctly for email functionality.

# Blog Website with Database

This is a Flask-based blog website featuring user authentication, admin privileges, and a SQLite database. The website allows users to create, edit, and delete blog posts, as well as add and manage comments.

## Features
- **User Authentication**: Register, log in, and log out securely.
- **Admin Privileges**: Admins can create, edit, and delete blog posts.
- **Comment System**: Logged-in users can add comments; commenters can delete their own comments.
- **Database Integration**: Uses SQLite for managing users, posts, and comments.
- **Email Contact Form**: Sends contact messages via Gmail.

## Technologies Used
- **Python**: Flask, SQLAlchemy, Flask-Login, Flask-Bootstrap, Flask-CKEditor
- **HTML/CSS**: Bootstrap for UI styling
- **Database**: SQLite
- **Email**: SMTP for sending messages

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the root folder and add the following:
   ```env
   FLASK_KEY=<your-secret-key>
   DB_URI=sqlite:///posts.db
   EMAIL_KEY=<your-email-address>
   PASSWORD_KEY=<your-email-app-password>
   ```

5. Initialize the database:
   ```bash
   flask shell
   >>> from app import db
   >>> db.create_all()
   >>> exit()
   ```

6. Run the app:
   ```bash
   flask run --port=5002
   ```

7. Access the website at `http://127.0.0.1:5002`.

## Routes Overview
- `/`: View all blog posts.
- `/post/<post_id>`: View a specific post with comments.
- `/register`: Register a new account.
- `/login`: Log in to an account.
- `/logout`: Log out of the current account.
- `/new-post`: Create a new blog post (admin-only).
- `/edit-post/<post_id>`: Edit an existing blog post (admin-only).
- `/delete/<post_id>`: Delete a blog post (admin-only).
- `/delete/comment/<comment_id>/<post_id>`: Delete a comment (commenter-only).
- `/about`: View the About page.
- `/contact`: Contact form.

## Notes
- Admin functionality is limited to the user with `id=1`.
- Ensure the `.env` file is configured correctly for email functionality.





