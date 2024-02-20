# Flask Blog App

This is a blog web app built with Flask and SQLite. 

## Features

- Create, edit, and delete blog posts (admin only)
- Register new users 
- Login/logout 
- Comment on posts (requires login)
- Delete own comments (comment author only)
- Responsive design

## Code Overview

The main code files:

### forms.py

Contains WTForm classes for handling form data:

- `CreatePostForm` for creating/editing posts 
- `RegisterForm` for registering new users
- `LoginForm` for logging in 
- `CommentForm` for commenting on posts

### models.py 

Sets up the SQLite database with Flask-SQLAlchemy:

- `User`, `BlogPost`, and `Comment` models
- Relationships between models 

### routes.py

Handles the app routes and view functions:

- `/` - Main blog page
- `/register` - Register new user  
- `/login` - Login 
- `/logout` - Logout
- `/post/<id>` - View post and comments
- `/new-post` - Create new post (admin only)
- `/edit-post/<id>` - Edit post (admin only) 
- `/delete-post/<id>` - Delete post (admin only)
- `/delete-comment/<id>` - Delete comment (comment author only)

Uses decorators to check user permissions before deleting/editing posts and comments.

### templates/

HTML templates for viewing the app pages.

### static/ 

CSS and images for styling the templates.

## Setup

1. Clone the repo
2. Create and activate a virtualenv
3. Install requirements: `pip install -r requirements.txt`
4. Run the app: `flask run`
5. Access the app at http://localhost:5002

## Usage

- Browse blog posts on the home page
- Register an account to comment and login 
- Admin users can create/edit/delete posts from the admin dashboard
- Commenters can delete their own comments

This simple app demonstrates core Flask functionality like routing, templates, forms, logins, and databases. Some features that could be added:

- Tags on posts
- Search posts
- Pagination 
- Email subscriptions
- Rich text editing

## License

This project is open source under the MIT license.
