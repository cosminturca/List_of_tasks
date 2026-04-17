# List Of Tasks -- Technical Documentation

# Students:

- **Andone Andrei**
- **Țurcă Cosmin-Constantin**

# 1. General Overview

The List Of Tasks application is a web platform dedicated to the efficient management of tasks and activities, aiming to improve user productivity. The project is built using the MERN stack (MongoDB, Express.js, React.js, Node.js), providing a modern, fast, and scalable solution.

The source code is organized into two main directories:

- **Backend:** The server API and database logic.

- **Frontend:** The reactive user interface.

# 2. Technical Objectives

- **Modern Architecture:** Using React together with Vite for optimal frontend performance.

- **Responsive & Modern Design:** Implementing the graphical interface with Tailwind CSS, ensuring a utility-first, consistent, and adaptable design on any device (mobile, tablet, desktop).

- **Interactivity:** Immediate visual feedback for user actions (adding, deleting, completing tasks).

- **RESTful API:** A standardized backend architecture for managing Task resources.

- **Data Persistence:** Secure data storage using the non-relational MongoDB database.

# 3. Features

- **Task Management (CRUD):** Users can create new tasks, view the full list, edit details, and delete tasks that are no longer needed.

- **Mark as Completed:** Toggle functionality to mark a task as completed or in progress.

- **Dynamic Interface:** Real-time updates of the task list without reloading the page.

- **Adaptive Design:** Flexible layout built with Tailwind utility classes.

- **Offline Mode (Offline-First):** The application works even without internet access, saving data locally and automatically syncing it when the connection is restored.

# 4. Technologies Used

**Frontend**

- **React (Vite)** + **TypeScript**.

- **Tailwind CSS** (used for fast styling, grid/flexbox systems, and responsive design).

- **React Router DOM:** For route management and navigation in the application (SPA - Single Page Application).

- **Axios / Fetch API:** For making HTTP requests to the backend.

**Backend**

- **Node.js & Express.js:** Modular server-side architecture.

- **Firebase Admin SDK:** Library used on the server to verify the integrity of JWT tokens received from the client.

- **Mongoose:** Data modeling (Schema) for interaction with MongoDB.

- **Input Validation:** Dedicated layer for validating received data (Request Body) to ensure data integrity before processing.

- **Middleware:** Intermediate functions for handling authentication and errors.

**Storage**

- **MongoDB:** NoSQL database.

- **Mongoose:** ODM (Object Data Modeling) for defining data structure (Schema) and validation.

# 5. Agile Methodology

The project was developed using an iterative approach, structured into Sprints:

**Sprint 1: MVP & Architecture (Core)**

- **Planning & Design:** Defining the data structure (Schema) and UI design in Tailwind CSS.

- **Implementation:** Setting up the environment (Vite + TypeScript), implementing Firebase authentication, and basic task CRUD operations.

- **Evaluation:** Testing the login flow and MongoDB database connectivity.

**Sprint 2: Advanced Features (Offline First)**

- **Planning:** Analyzing requirements for offline data persistence.

- **Implementation:** Integrating IndexedDB for local storage and automatic synchronization with the backend upon reconnection. Adding filters and categories.

- **Testing:** Verifying offline scenarios and data consistency.

**Sprint 3: UI/UX & Export**

- **Design:** Refining the interface.

- **Implementation:** Adding Export (PDF, CSV, Excel) and Import functionalities.

- **Launch & Retrospective:** Optimizing the build for production (Vercel).

## Development Flow

![Development Flow](./development-flow.png)

## Application Architecture

![Application Architecture](./application-architecture.png)

## React Components Architecture

![React Components Architecture](./react-components-architecture.png)

# 8. API Documentation

All routes are protected and require authentication through the Authorization Header.

**GET /api/tasks** Returns the list of tasks associated exclusively with the authenticated user.

**GET /api/tasks/:id** Returns the details of a single task based on its ID (only if it belongs to the user).

**POST /api/tasks** Creates a new validated task. Body: { title, description, priority, deadline, category }.

**PUT /api/tasks/:id** Updates an existing task (status, content, or priority changes).

**DELETE /api/tasks/:id** Permanently deletes a task from the database.

# 9. Frontend Routes

**Public Routes:** /login – The authentication page. If the user is already logged in, they are automatically redirected to the Dashboard.

**Protected (Private) Routes:**/ (Root) loads the <TaskBoard /> component.

# 10. Conclusions

List Of Tasks demonstrates the ability to build a functional and aesthetically pleasing Full Stack application. The use of Tailwind CSS enabled rapid interface development, while the MERN architecture ensures performance and scalability. The project is ready for future extensions.