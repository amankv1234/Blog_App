<h1 align="center">📝 Blog App</h1>

🚀 Overview

Blogify is a full-stack blogging platform where users can sign up, log in, write blogs, upload cover images, comment on posts, and read blogs.
It includes JWT authentication, cookie-based sessions, Multer uploads, and a structured MVC-like architecture.

---

## 🚀 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Mongoose-880000?style=for-the-badge&logo=mongoose&logoColor=white" />
  <img src="https://img.shields.io/badge/EJS-64C7FF?style=for-the-badge&logo=ejs&logoColor=black" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Cookie%20Parser-000000?style=for-the-badge&logo=cookiecutter&logoColor=white" />
</p>

---

⭐ Features

🔐 User Authentication (JWT + Cookies)

📝 Create, Read, Update & Delete Blogs

💬 Comment System (Add comments on blogs)

🖼 Cover Image Upload using Multer

🗂 Clean Folder Structure (MVC-inspired)

🧩 Reusable EJS Partials

🚀 Fast & Lightweight Node.js backend

🗂 Folder Structure
```
BLOG_APP
├─ middlewares/
│   └─ authentication.js
├─ models/
│   ├─ blog.js
│   ├─ comment.js
│   └─ user.js
├─ node_modules/
├─ public/
│   ├─ images/
│   └─ uploads/
├─ routes/
│   ├─ blog.js
│   └─ user.js
├─ service/
│   └─ authentication.js
├─ views/
│   ├─ partials/
│   │   ├─ head.ejs
│   │   ├─ nav.ejs
│   │   └─ script.ejs
│   ├─ addBlog.ejs
│   ├─ blog.ejs
│   ├─ home.ejs
│   ├─ signin.ejs
│   └─ signup.ejs
├─ .env
├─ app.js
├─ package.json
└─ package-lock.json
```
⚙️ Tech Stack (with logos)
|  Tool Used  | Category|
|--------|--------|
|**Node.js** | Server runtime.|
|**Express.js**| Web framework.|
|**MongoDB**|  Database (via Mongoose).|
|**EJS**| Templating engine.|
|**JWT**|  Authentication tokens.|
|**Multer**| File upload middleware.|
|**bcrypt**  |Password hashing.|
|**dotenv** |Environment variables.|
|**cookie-parser** | Cookie handling.|
|**nodemon** | Dev auto-restart.|

🚀 Quick Setup — (COPY & PASTE)
Option A — If you're cloning this repo (recommended)

# clone the repo
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

# install dependencies (reads package.json)
```bash
npm install
```
# create .env file (see example below)
# then start in dev
```bash
npm run dev
```
# or start normally
```bash
npm start
```
Option B — If you're starting from scratch (new project)

mkdir blog-app && cd blog-app
```bash
npm init -y
```
# install runtime dependencies
```bash
npm install express ejs mongoose dotenv jsonwebtoken cookie-parser multer bcrypt
```
# optional (dev)
```bash
npm install -D nodemon
```
# create project files/folders (use the structure above)
📦 Full list of recommended npm packages
express
ejs
mongoose
dotenv
jsonwebtoken
cookie-parser
multer
bcrypt
cookie-signature (optional)
Dev:
nodemon
You can install them all at once:
```bash
npm install express ejs mongoose dotenv jsonwebtoken cookie-parser multer bcrypt
```
```bash
npm install -D nodemon
```
🔧 Environment Variables (.env example)

Create a .env file in project root and populate values:
PORT=3000
MONGODB_URI=mongodb://localhost:27017/blogify
How to run (commands)

Development (auto restart):
```bash
npm run dev
```
  # assumes package.json has "dev": "nodemon app.js"
Production:
```bash
npm start
```
 # "start": "node app.js"
🔐 Authentication flow (high level)

User signs up → password hashed with bcrypt → saved to users collection.

On login → server validates credentials → signs a JWT (jsonwebtoken) → stores token in an HTTP-only cookie (cookie-parser).

Protected routes check cookie + verify JWT in middlewares/authentication.js.

📁 Views & Partials

views/partials/head.ejs — head tags, CSS links, meta.

views/partials/nav.ejs — navigation bar, user name, logout.

views/partials/script.ejs — JS imports.

Main pages: home.ejs, addBlog.ejs, blog.ejs, signin.ejs, signup.ejs.

🖼️ Image Uploads

Using multer to accept cover images and store them in public/uploads/.

Optionally configure Cloudinary and store the URL in the DB (recommended for production).

🤝 Contributing

Fork the repo → create a feature branch → open a PR with description.

Please follow consistent coding style and add meaningful commit messages.


📝 License

MIT License — see LICENSE file.

✉️ Author

Aman Kumar Vishwakarma
Email: amankumarvishwakarma
