# Learning Management System using MERN stack

## Features

- `authentication`
  - complete auth including update profile, forgot, reset and change password
- `authoriztion` - protected routes that access by only admin
- `protected courses` - user access only purchase courses
- `lecture notes` - user add notes to each lecture
- `lecture mark` - user can mark viewd lecture
- `dashboard` - details of users and courses
- `languages` - app available in english, hindi and gujarati language
- `realtime-chat` - chat with other people on this app

### Backend setup

- `cd server` in root directory
- `npm install` in server directory to install all dependencies
- Set `environment variables`
  - `PORT` - port number to listen the server
  - `MONGO_URL` - url of your local_database or Atlas
  - secret token and expiry
    - `JWT_SECRET_KEY`
    - `JWT_EXPIRY`
  - gmail credentials
    - `SMTP_USERNAME`
    - `SMTP_PASSWORD`
  - cloudinary credentials
    - `CLOUD_NAME`
    - `CLOUD_API_KEY`
    - `CLOUD_API_SECRET`
  - stripe credentials
    - `STRIPE_SECRET`
- `npm run dev` to start project

# Backend of LMS using express & MongoDB

## Routes

### user authentication - base route `/api/v1/user`

- `/register`
- `/me` - get and update user detail
- `/login`
- `/logout`
- `/reset` - forgot password
- `/reset/:resetToken`
- `/change-password`

### courses and lectures - base route `/api/v1/course`

- `/category`
- `/instructor`
- `/` - CRUD operation on courses by admin
- `/:courseId` - CRUD operation on lectures by admin

### user progress - base route `/api/v1/my-course`

- `/` - get user purchased courses
- `/:courseId` - CRUD operation on user course

### payment gateway - base route `/api/v1/payment`

- `/getkey`
- `/checkout`
- `/verify` - access course to user on payment success

### admin - base route `/api/v1/admin`

- `/courses-sell-by-user`
- `/courses-sell-by-course`

## npm modules

- bcryptjs
- cloudinary
- cookie-parser
- cors
- dotenv
- express
- jsonwebtoken
- mongoose
- multer
- nodemailer
- socket.io
- stripe

## File Structure

- `config` - configuration for connection like mongodb and clouinary
- `controllers`
- `middleware` - middleware for authentication, errors and file uploads
- `models`
- `routes`
- `utils` - functionality for error and mails
- `app.js` - This is renders different routes
- `server.js` - listen to server
- `package.json` -

## Project Setup

To run project locally

- Clone repo
- `npm install` in root directory
- Set for `environment variables`
  - `PORT` - set port number to listen the server
  - `DB_URL` - url of your local_database or Atlas
  - `CLOUD_NAME` -
  - `CLOUD_API_KEY` -
  - `CLOUD_API_SECRET` -
- `npm run dev` & if nodemon not installed then `npm run start`
- use `http://127.0.0.1:3000` to go to the page
