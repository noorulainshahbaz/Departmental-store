csd-department-store/
   ├── public/
   │   ├── css/
   │   │   └── styles.css
   │   ├── js/
   │   │   └── script.js
   │   ├── images/
   │   └── index.html
   ├── server.js
   ├── package.json
   └── README.md
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>CSD Department Store</title>
       <link rel="stylesheet" href="css/styles.css">
   </head>
   <body>
       <header>
           <h1>Welcome to CSD Department Store</h1>
           <nav>
               <ul>
                   <li><a href="/">Home</a></li>
                   <li><a href="/about">About Us</a></li>
                   <li><a href="/products">Products</a></li>
                   <li><a href="/contact">Contact</a></li>
               </ul>
           </nav>
       </header>
       <main>
           <section class="hero">
               <h2>Your One-Stop Shop for Everything!</h2>
               <p>Explore our wide range of products at unbeatable prices.</p>
               <a href="/products" class="btn">Shop Now</a>
           </section>
       </main>
       <footer>
           <p>&copy; 2023 CSD Department Store. All rights reserved.</p>
       </footer>
       <script src="js/script.js"></script>
   </body>
   </html>
console.log("CSD Department Store - Frontend Loaded!");npm init -y
     npm install express mongoose body-parser cors

     const express = require("express");
   const mongoose = require("mongoose");
   const bodyParser = require("body-parser");
   const cors = require("cors");

   const app = express();
   const PORT = 5000;

   // Middleware
   app.use(cors());
   app.use(bodyParser.json());
   app.use(express.static("public"));

   // MongoDB Connection
   mongoose.connect("mongodb://localhost:27017/csd-store", {
       useNewUrlParser: true,
       useUnifiedTopology: true,
   });

   // Routes
   app.get("/", (req, res) => {
       res.sendFile(__dirname + "/public/index.html");
   });

   app.get("/about", (req, res) => {
       res.sendFile(__dirname + "/public/about.html");
   });

   app.get("/products", (req, res) => {
       res.sendFile(__dirname + "/public/products.html");
   });

   app.get("/contact", (req, res) => {
       res.sendFile(__dirname + "/public/contact.html");
   });

   // Start Server
   app.listen(PORT, () => {
       console.log(`Server is running on http://localhost:${PORT}`);
   });
