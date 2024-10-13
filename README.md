
# 📦 Warehouse Management System (WMS)

An application designed to display a tree view of godowns and items stored within each. The system is built using a MERN stack with React for the frontend and Node.js, Express, and MongoDB for the backend, and it's deployed on Vercel.

## 📑 Table of Contents
- [🚀 Approach](#-approach)
- [🛠️ How to Run](#%EF%B8%8F-how-to-run)
- [🎥 Video Demonstration](#-video-demonstration)
- [🌐 Deployment Links](#-deployment-links)
- [💻 Technologies Used](#-technologies-used)

---

## 🚀 Approach

The project required displaying a tree view of godowns, which may have parent-child relationships. The approach includes:

### Backend
- **Source Data**: The `godown.json` file contains godown objects, each with a reference to its parent godown.
- **Recursive Conversion**: A recursive function transforms the JSON array into a hierarchical structure where each godown has a `children` array for its sub-godowns. This hierarchical structure is saved to MongoDB.
- **API Endpoints**:
  - `/godown`: Fetches the hierarchical tree structure from MongoDB.
  - `/item`: Fetches the items for a specific godown by `godownid`.

### Frontend
- **Tree View**: A recursive sidebar component displays the hierarchical tree of godowns. When a user clicks on a leaf node (a godown with no children), an Axios request is made to the `/item` endpoint to fetch the items for that godown.
- **Dynamic Fetching**: Upon expanding any godown node, the items stored in that godown are fetched and displayed dynamically.

---

## 🛠️ How to Run

### Prerequisites
Ensure that you have the following installed:
- **Node.js**
- **MongoDB**

### Installation

#### 1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

#### 2. Set up the Frontend (React + Vite):
   Navigate to the `frontend` folder:
   ```bash
   cd frontend
   ```

   Install dependencies:
   ```bash
   npm i
   ```

   Start the development server:
   ```bash
   npm run dev
   ```

   The frontend will be accessible at `http://localhost:3000`.

#### 3. Set up the Backend (Node + Express):
   Navigate to the `backend` folder:
   ```bash
   cd ../backend
   ```

   Install dependencies:
   ```bash
   npm i
   ```

   Start the backend server:
   ```bash
   npm start
   ```

   The backend will run on `http://localhost:5000`.

#### 4. Environment Variables
Create a `.env` file in the `backend` folder and add the following environment variables:

```bash
MONGO_URI=mongodb://localhost:27017/your-database
```

Make sure MongoDB is running and accessible at the specified URI.

---

## 🎥 Video Demonstration

Watch a video demonstration of the application:

[![Watch the demo](https://img.youtube.com/vi/1jAuaMIRVXyUF_mXkTngPYopMUBOV3vkg/maxresdefault.jpg)](https://drive.google.com/file/d/1jAuaMIRVXyUF_mXkTngPYopMUBOV3vkg/view?usp=sharing)

---

## 🌐 Deployment Links

- **Production**: [https://wms-app-xi.vercel.app/](https://wms-app-xi.vercel.app/)

---

## 💻 Technologies Used

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)

### Backend
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)

### Database
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

### Deployment
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

