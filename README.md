# Backend-service
Simple Express.js Server
Installation
Make sure you have Node.js installed, then run the following command to install Express: npm i express
Also make sure you have nodemon installed: npm i -g nodemon


The following JavaScript code creates a web server using Express:
import express from "express"; // Import Express framework
const app = express(); // Initialize an Express application
const port = 3000; // Define the port number

// Define routes for different pages
app.get("/", (req, res) => {
  res.send("<h1>Hello</h1>"); // Home route
});

app.get("/about", (req, res) => {
  res.send("<h1>About Me</h1><p>My name is Fortune</p>"); // About page
});

app.get("/contact", (req, res) => {
  res.send("<h1>Contact Me</h1><p>Phone: 08064960219</p>"); // Contact page
});

// Start the server and listen on the defined port
app.listen(port, () => {
  console.log(`Server started on port ${port}.`);
});
How It Works
Imports Express → The script imports the Express framework.
Creates an Express App → Initializes an instance of Express.
Defines a Port → The server runs on port 3000.
Handles GET Requests:
/ → Responds with "Hello" as an HTML heading.
/about → Displays information about the developer.
/contact → Provides contact details.
Starts the Server → The server listens on port 3000 and logs a message when running.
How to Run the Server
Save the script as index.js.
Open a terminal and navigate to the project folder.
Run the command:
nodemon index.js

Open your browser and visit:
http://localhost:3000/ → Home Page
http://localhost:3000/about → About Page
http://localhost:3000/contact → Contact Page

Notes
This script uses ES Modules (import express from "express"). If you get an error, add "type": "module" in package.json or use CommonJS (const express = require("express")).
