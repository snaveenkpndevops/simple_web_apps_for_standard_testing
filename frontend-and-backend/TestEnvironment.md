# Test Environment - Customer App

The Customer App is a web application built with ReactJS (frontend) and Node.js (backend).

## Pre-requisites

Make sure the following are installed on your machine:

- Node.js  
- npm  

To install Node.js and npm, visit: https://nodejs.org/en/

## How to Run the Application

After cloning the repository, follow the steps below.

### 1) Start the Backend

Open a terminal, navigate to the root of the repository, and run:

```
cd backend
npm install
npm start
```

The backend server will run on port 3001 by default.

If you want to change the port, update the value in:

/backend/server.js

const port = 3001;

---

### 2) Start the Frontend

Open a new terminal, navigate to the root of the repository, and run:

```
cd frontend
npm install
```

#### Environment Configuration

Update the .env file located at:

/frontend/.env

##### Case 1: Connecting to Local Backend

```
REACT_APP_API_URL=http://localhost:3001/
```

Make sure the port matches your backend configuration.

##### Case 2: Connecting to Azure Web App Backend

```
REACT_APP_API_URL=http://customer-backend-app-ckgya4dedudehkcr.centralindia-01.azurewebsites.net/
```
- Azure App Service automatically runs the backend on port 8080
- So, you only need to provide the DNS URL
- No changes are required in /frontend/src/App.js

### 3) Run the Frontend

```
npm run build
npm start
```
## Access the Application

Open your browser and navigate to:

http://localhost:3000/