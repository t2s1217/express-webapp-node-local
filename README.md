# Case Study: Getting Started with express-t2s-app-v1 (Cloud & DevOps Foundations)

## Situation
As part of a cloud-native learning initiative, the goal was to help beginners understand the fundamentals of building a Node.js and Express web application—the first step toward mastering DevOps-ready, cloud-deployable systems. Many learners struggled with local setup, code structure, and debugging when starting with backend frameworks.

To address this, we created **express-t2s-app-v1**, a minimal Node.js application designed to teach core concepts like HTTP routing, static file serving, and basic server configuration—laying the groundwork for future containerization and deployment.

## Task
The objective was to build and document a simple, educational Express.js project that would allow learners to:
- Run a local web server successfully
- Understand the structure of an Express app
- View and modify HTML pages served from the backend
- Practice debugging and managing server ports

## Action
To achieve this, we:

1. **Set Up the Project Environment**
   - Installed Node.js (LTS version), Git, and VS Code for consistent development setup.
   - Initialized the project with `package.json` and added Express as a dependency.

2. **Structured the Application**
   ```
   express-t2s-app-v1/
   ├── public/              # Static assets (HTML/CSS)
   │   └── index.html       # Home page
   ├── index.js             # Main server file
   ├── package.json         # Dependencies & metadata
   └── README.md            # Documentation
   ```

3. **Implemented a Basic Express Server**
   - Used `express.static()` to serve files from the `/public` directory.
   - Configured the app to listen on port 3000 by default.
   - Added routes such as `/about` to demonstrate dynamic responses.

   ```js
   const express = require('express');
   const app = express();
   app.use(express.static('public'));
   app.get('/about', (req, res) => res.send('About this app'));
   app.listen(3000, () => console.log('Server is running at http://localhost:3000'));
   ```

4. **Provided Hands-On Guidance**
   - Step-by-step instructions to install dependencies (`npm install`) and run the app (`node index.js`).
   - Troubleshooting tips for common issues (port conflicts, Node not found).
   - Exercises encouraging modification of `index.html` and creation of new routes.

## Result
By the end of the project, learners were able to:
- Successfully run a Node.js + Express web server locally
- Understand the core structure of an Express application
- Experiment with HTML and basic routes
- Build confidence using the terminal and debugging startup issues

This foundation now prepares them to advance to **express-t2s-app-v2**, where they will Dockerize the app and begin exploring containerized deployments—key steps toward a full DevOps and cloud engineering workflow.

## Next Step
Move to **express-t2s-app-v2** to learn how to containerize and prepare your app for modern cloud infrastructure.
