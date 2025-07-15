# Blog_Backend
Nodejs backend Project for Blogs Manager

# 📝 Node.js Blog API

A full-featured REST API for a blog system built with **Node.js**, **Express**, and **MongoDB**, including:

- ✅ User Authentication (JWT)
- ✅ User-based Access Control
- ✅ Blog Post CRUD Operation
- ✅ Forgot/Reset Password

## 🚀 Features

### 👤 Authentication
- User registration & login
- Passwords are securely hashed using `bcryptjs`
- JWT-based token authentication
- Forgot/Reset password using secure token

### 🔐 Role-Based Access
- Users have roles
- Role middleware to restrict access to certain endpoints

### 🧾 Blog Post Management
- Create, read, update, and delete posts
- Only the post author can update/delete

## 🛠 Tech Stack

- **Backend:** Node.js, Express
- **Database:** MongoDB (with Mongoose)
- **Security:** JWT, bcryptjs Dotenv

## 🛠 TestApi 

++ Authentication ++

* register:- POST / http://localhost:5000/api/auth/register
Json Formate
{
  "username": "demo",
  "email": "demo@example.com",
  "password": "123456"
}

* login:- POST / http://localhost:5000/api/auth/login 
Json Formate
{
  "email": "demo@example.com",
  "password": "123456"
}

* forgot-password POST / http://localhost:5000/api/auth/forgot-password
Json Formate (Token Require)
{
  "email": "paras@example.com"
}

* reset-password POST / http://localhost:5000/api/auth/reset-password/<token>
Json Formate (Token Require)
{
  "password": "123456"
}

++ Post ++

Posts POST/ http://localhost:5000/api/posts/
{
  "title": "Demo",
  "content": "Demo post"
}

Get Posts GET/ http://localhost:5000/api/posts/

Update Posts PUT/ http://localhost:5000/api/posts/{ID}
{
  "title": "Update My First Blog Post",
  "content": "Update This is the content of my blog post."
}

Delete Posts DELETE/ http://localhost:5000/api/posts/{ID}
