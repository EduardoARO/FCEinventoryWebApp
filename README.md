# **FCEinventoryWebApp**

**FCEinventoryWebApp** is a fullstack application built with **React (Vite)** for the frontend, **Node.js + Express + TypeScript** for the backend, and **MongoDB** as the database.
This project demonstrates a complete setup for a MERN-based application with basic CRUD operations to manage users.

---

## **Project Structure**

```
FCEinventoryWebApp/
│
├── backend/            # API built with Node.js, Express, TypeScript
│   ├── src/
│   │   ├── config/     # Database connection
│   │   │   └── db.ts
│   │   ├── models/     # MongoDB models
│   │   │   └── User.ts
│   │   ├── controllers/# Controllers for handling business logic
│   │   │   └── userController.ts
│   │   ├── routes/     # API routes
│   │   │   └── userRoutes.ts
│   │   ├── app.ts      # Express app configuration
│   │   └── server.ts   # App entry point
│   │
│   └── tsconfig.json   # TypeScript configuration
│
└── frontend/           # React app (Vite + TypeScript)
    ├── src/
    │   ├── api/        # Axios instance for API calls
    │   │   └── api.ts
    │   ├── pages/      # Application pages
    │   │   └── Home.tsx
    │   ├── App.tsx
    │   └── main.tsx
    │
    └── vite.config.ts  # Vite configuration
```

---

## **Features**

* Add new users with **name** and **email**.
* View a list of all registered users.
* REST API endpoints to manage data.
* Fully typed backend with TypeScript.
* MongoDB for persistence.

---

## **Tech Stack**

### **Frontend**

* [React](https://react.dev/)
* [Vite](https://vitejs.dev/)
* [Axios](https://axios-http.com/)

### **Backend**

* [Node.js](https://nodejs.org/)
* [Express](https://expressjs.com/)
* [TypeScript](https://www.typescriptlang.org/)
* [Mongoose](https://mongoosejs.com/)

### **Database**

* [MongoDB](https://www.mongodb.com/)

---

## **Getting Started**

Follow these steps to run **FCEinventoryWebApp** locally.

### **Prerequisites**

* [Node.js](https://nodejs.org/) (v16+ recommended)
* [MongoDB](https://www.mongodb.com/try/download/community) running locally or a MongoDB Atlas connection.

---

### **1. Clone the repository**

```bash
git clone https://github.com/your-username/FCEinventoryWebApp.git
cd FCEinventoryWebApp
```

---

### **2. Backend Setup**

1. Navigate to the backend folder:

   ```bash
   cd backend
   ```
2. Install dependencies:

   ```bash
   npm install
   ```
3. Create a `.env` file:

   ```
   MONGO_URI=mongodb://127.0.0.1:27017/FCEinventoryDB
   PORT=5000
   ```
4. Run the backend server:

   ```bash
   npm run dev
   ```

   The backend will run at: `http://localhost:5000`

---

### **3. Frontend Setup**

1. Navigate to the frontend folder:

   ```bash
   cd ../frontend
   ```
2. Install dependencies:

   ```bash
   npm install
   ```
3. Start the development server:

   ```bash
   npm run dev
   ```

   The frontend will run at: `http://localhost:5173`

---

## **API Endpoints**

| Method | Endpoint     | Description       |
| ------ | ------------ | ----------------- |
| GET    | `/api/users` | Get all users     |
| POST   | `/api/users` | Create a new user |

**Example Request (POST /api/users):**

```json
{
  "name": "John Doe",
  "email": "john.doe@example.com"
}
```

**Example Response:**

```json
{
  "_id": "6513ae8a9f1234567890abcd",
  "name": "John Doe",
  "email": "john.doe@example.com",
  "__v": 0
}
```

---

## **Scripts**

### **Backend**

| Command         | Description                                       |
| --------------- | ------------------------------------------------- |
| `npm run dev`   | Run backend in development mode using ts-node-dev |
| `npm run build` | Compile TypeScript to JavaScript                  |
| `npm start`     | Run compiled backend (`dist/`)                    |

### **Frontend**

| Command         | Description                         |
| --------------- | ----------------------------------- |
| `npm run dev`   | Run frontend in development mode    |
| `npm run build` | Build the production-ready frontend |

---

## **Folder Overview**

### **Backend**

* **`config/db.ts`** → MongoDB connection logic.
* **`models/User.ts`** → User model schema.
* **`controllers/userController.ts`** → Handles user-related requests.
* **`routes/userRoutes.ts`** → Routes for user endpoints.

### **Frontend**

* **`pages/Home.tsx`** → Main page to view and add users.
* **`api/api.ts`** → Axios instance configured for API requests.

---

## **Demo**

* **Frontend URL:** `http://localhost:5173`
* **Backend URL:** `http://localhost:5000/api/users`

---

## **Future Improvements**

* Add user authentication (JWT).
* Edit and delete users.
* Implement pagination on the user list.
* Deploy to production using services like Vercel (Frontend) and Render (Backend).

---

## **License**

This project is licensed under the MIT License.
See the [LICENSE](LICENSE) file for more details.
