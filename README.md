# Node-Js
This repo will contain all the  Node Js fundamentals
# Node.js Server Development  

## Table of Contents  
- [Setting up a Node.js Server using Express](#setting-up-a-nodejs-server-using-express)  
- [Middleware, Routing, and Request/Response Cycle](#middleware-routing-and-requestresponse-cycle)  
- [RESTful APIs](#restful-apis)  
- [Middleware Concepts](#middleware-concepts)  
- [Error Handling and Logging](#error-handling-and-logging)  
- [Authentication: JWT](#authentication-jwt)  
- [API Validation](#api-validation)  
- [Rate Limiting and Security Practices](#rate-limiting-and-security-practices)  
- [File Uploads with Multer](#file-uploads-with-multer)  

---

## Setting up a Node.js Server using Express  
Learn how to set up a basic server with Express:  
1. Install Node.js and initialize the project:  
    ```bash  
    npm init -y  
    npm install express  
    ```  
2. Create a basic server:  
    ```javascript  
    const express = require('express');  
    const app = express();  
    const PORT = 3000;  

    app.get('/', (req, res) => {  
        res.send('Hello, World!');  
    });  

    app.listen(PORT, () => {  
        console.log(`Server is running on http://localhost:${PORT}`);  
    });  
    ```  

---

## Middleware, Routing, and Request/Response Cycle  
- **Middleware**: Functions that execute during the request/response cycle.  
    Examples: `body-parser`, `cors`, and custom middleware.  
- **Routing**: Define routes like `app.get()`, `app.post()`, etc.  
- **Request/Response Cycle**: Understand how a client request flows through middleware, routing, and handlers.  

---

## RESTful APIs  
Designing RESTful endpoints for CRUD operations:  
- **GET**: Fetch resources.  
- **POST**: Create resources.  
- **PUT**: Update resources.  
- **DELETE**: Remove resources.  
Example:  
```javascript  
app.get('/api/resource', (req, res) => res.json({ message: 'Resource fetched' }));  
