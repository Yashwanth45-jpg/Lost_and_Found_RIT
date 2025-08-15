# Lost and Found - Backend Server 📂

This is the backend server for the Lost and Found RIT application. It handles user authentication, item reporting, and database management using Node.js, Express, and MongoDB.

---

## Prerequisites

Before you begin, ensure you have the following installed on your system:

-   [Node.js](https://nodejs.org/en/) (which includes npm)
-   [MongoDB Compass](https://www.mongodb.com/products/compass) (Optional, for database management)

---

## Installation and Setup

Follow these steps to get the server up and running on your local machine.

### 1. Clone the Repository

```bash
git clone [https://github.com/Yashwanth45-jpg/Lost_and_Found_RIT.git](https://github.com/Yashwanth45-jpg/Lost_and_Found_RIT.git)
cd Lost_and_Found_RIT/backend
```

### 2. Install Dependencies

This will install all the necessary packages listed in `package.json`, including Express, Mongoose, JWT, and others.

```bash
npm install
```

### 3. Set Up MongoDB Atlas Database ☁️

You need a MongoDB database to store application data. You can get a free one from MongoDB Atlas.

#### Create a Free Cluster:

1.  Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register) and sign in or create an account.
2.  Create a new project.
3.  Build a new cluster, selecting the **free M0 tier**.
4.  Choose a cloud provider and region, then create the cluster.

#### Configure Access:

-   **Database User:** In the "Database Access" section, create a new database user. Give it a username and a strong password. **Save this password securely.**
-   **Network Access:** In the "Network Access" section, add an IP address. For development, you can select **"Allow Access from Anywhere"** which will add `0.0.0.0/0`.

#### Get Your Connection String:

1.  Go back to your cluster's "Overview" and click the **Connect** button.
2.  Select **"Compass"** as the connection method.
3.  Copy the provided connection string. It will look something like this:
    `mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/?retryWrites=true&w=majority`

### 4. Create an Environment File

You must store your secret connection string in an environment file.

1.  In the `backend` folder, create a new file named `.env`.
2.  Add the following line to the `.env` file:
    ```
    MONGODB_URL=your_mongodb_connection_string
    ```
3.  Paste the connection string you copied from Atlas, replacing `<password>` with the actual password you created for your database user.

---

## Running the Server ▶️

To start the server with automatic reloading on file changes (using nodemon), run the following command:

```bash
npx nodemon server.js
```

The server should now be running, and you'll see a confirmation message in your terminal, like "Server running on port 5000" and "MongoDB connected."
