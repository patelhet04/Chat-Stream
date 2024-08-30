# Chat-Stream: Scalable Chat App

**Technologies Used:**

- **Socket.io:** Implemented real-time, bidirectional communication between the server and clients, enabling instantaneous messaging and presence features.
- **Kafka:** Designed and utilized a distributed messaging system for high-throughput, fault-tolerant data streaming, ensuring reliable communication between microservices.
- **Redis:** Employed as an in-memory data structure store for caching frequently accessed data and managing session information, resulting in improved application performance and reduced latency.
- **Postgres:** Leveraged as the primary relational database for storing user data and chat histories, ensuring data consistency and supporting complex queries.
- **React.js:** Developed the front-end user interface, creating a responsive and dynamic web experience that supports real-time updates and interactions.
- **Prisma:** Used as an ORM (Object-Relational Mapping) tool to interact with the Postgres database, simplifying data modeling and query generation with TypeScript support.
- **TypeScript:** Utilized throughout the codebase to enforce strict type-checking and improve code reliability, making the development process more robust and maintainable.

**Project Highlights:**

- Developed a scalable architecture that handles thousands of concurrent users with minimal latency.
- Ensured data integrity and consistent performance across the application using a combination of state-of-the-art technologies.
- Created an intuitive user interface that provides a seamless chat experience, with real-time updates and high reliability.

## Backend Setup (Node.js, Prisma, Kafka, Redis, Postgres)

### 1. Prerequisites
Ensure you have the following installed on your machine:
- **Node.js** (v14 or higher)
- **PostgreSQL** (v12 or higher)
- **Redis** (v6 or higher)
- **Kafka** (v2.7 or higher)
- **Docker** (Optional, for containerized services)

### 2. Clone the Repository
```bash
git clone https://github.com/patelhet04/Chat-Stream.git
cd Chat-Stream/backend
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Set Up Environment Variables
Create a `.env` file in the `backend` directory and configure it with your environment settings:

```bash
DATABASE_URL="postgresql://username:password@localhost:5432/Chat-Stream"
REDIS_URL="redis://localhost:6379"
KAFKA_BROKER="localhost:9092"
PRISMA_LOG_LEVEL="info"
PORT=4000
```

### 5. Set Up Prisma

Prisma is used as the ORM for interacting with the Postgres database.

* Generate Prisma client:

```bash
npx prisma generate
```

* Run database migrations:

```bash
npx prisma migrate dev
```

### 6. Run Kafka, Redis, and Postgres
Ensure Kafka, Redis, and Postgres services are running. You can run them using Docker for easy setup:
```bash
docker-compose up -d
```

### 7. Start the Backend Server
```bash
npm run dev
```
The backend server should now be running at `http://localhost:4000`.

## Frontend Setup (React.js and TypeScript)

### 1. Navigate to Frontend Directory

```bash
cd ../frontend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env` file in the `frontend` directory and configure it with your environment settings:

```bash
REACT_APP_API_URL="http://localhost:4000"
```

### 4. Start the Frontend Server

```bash
npm start
```

The frontend should now be running at `http://localhost:3000`.
