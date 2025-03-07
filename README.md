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
