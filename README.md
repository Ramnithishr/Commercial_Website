# Ex02 Commercial Website
## Date: 24/2/2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM

# Index.Html
```
<!DOCTYPE html>
<html>
<head>
    <title>CarZone Premium</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<!-- Navbar -->
<nav>
    <div class="logo">CarZone</div>
    <div>
        <a href="#home">Home</a>
        <a href="#buy">Buy</a>
        <a href="#sell">Sell</a>
    </div>
</nav>

<!-- HOME -->
<section id="home" class="section hero">
    <h1>Premium Cars Marketplace</h1>
    <a href="#buy" class="btn">Explore Cars</a>
</section>

<!-- BUY SECTION -->
<section id="buy" class="section">
    <h2>Available Cars</h2>

    <div class="card-container">

        <div class="card">
            <h3>BMW 3 Series</h3>
            <p>₹45,00,000</p>
            <a href="#bmw" class="btn">View Details</a>
        </div>

        <div class="card">
            <h3>Audi A6</h3>
            <p>₹55,00,000</p>
            <a href="#audi" class="btn">View Details</a>
        </div>

        <div class="card">
            <h3>Mercedes Benz C-Class</h3>
            <p>₹60,00,000</p>
            <a href="#benz" class="btn">View Details</a>
        </div>

    </div>
</section>

<!-- BMW DETAILS -->
<section id="bmw" class="section">
    <h2>BMW 3 Series</h2>
    <div class="details-box">
        <p><strong>Price:</strong> ₹45,00,000</p>
        <p><strong>Year:</strong> 2023</p>
        <p><strong>Engine:</strong> 2.0L Turbo</p>
        <p><strong>Fuel:</strong> Petrol</p>
        <a href="#home" class="btn">Buy Now</a>
        <img src="images (3).jpg";>
    </div>
</section>

<!-- AUDI DETAILS -->
<section id="audi" class="section">
    <h2>Audi A6</h2>
    <div class="details-box">
        <p><strong>Price:</strong> ₹55,00,000</p>
        <p><strong>Year:</strong> 2023</p>
        <p><strong>Engine:</strong> 2.0L TFSI</p>
        <p><strong>Fuel:</strong> Petrol</p>
        <a href="#home" class="btn">Buy Now</a>
        <img src="images.jpg";>
    </div>
</section>

<!-- BENZ DETAILS -->
<section id="benz" class="section">
    <h2>Mercedes Benz C-Class</h2>
    <div class="details-box">
        <p><strong>Price:</strong> ₹60,00,000</p>
        <p><strong>Year:</strong> 2023</p>
        <p><strong>Engine:</strong> 2.0L Turbo</p>
        <p><strong>Fuel:</strong> Diesel</p>
        <a href="#home" class="btn">Buy Now</a>
        <img src="download.jpg";>
    </div>
</section>

<!-- SELL SECTION -->
<section id="sell" class="section">
    <h2>Sell Your Car</h2>

    <div class="sell-box">
        <input type="text" placeholder="Car Brand">
        <input type="number" placeholder="Year">
        <input type="number" placeholder="Expected Price">

        <div class="price-display">
            Estimated Price: ₹25,00,000
        </div>

        <a href="#home" class="btn">Submit</a>
    </div>
</section>

</body>
</html>
```

# Style.Css
```
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial;
    scroll-behavior:smooth;
}

nav{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px 40px;
    background:rgba(0,0,0,0.9);
    color:white;
    position:fixed;
    width:100%;
    z-index:1000;
}

nav a{
    color:white;
    text-decoration:none;
    margin-left:20px;
}

.section{
    min-height:100vh;
    padding:120px 50px;
    text-align:center;
    color:white;
}

/* 🔥 HERO WITH CAR BACKGROUND */
.hero{
    background: 
    linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
    url("https://images.unsplash.com/photo-1503376780353-7e6692767b70");
    
    background-size:cover;
    background-position:center;
    background-repeat:no-repeat;

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
}

/* BUY SECTION BACKGROUND */
#buy{
    background:
    linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
    url("https://images.unsplash.com/photo-1493238792000-8113da705763");
    background-size:cover;
    background-position:center;
}

/* CAR CARDS */
.card-container{
    display:flex;
    justify-content:center;
    gap:20px;
    margin-top:30px;
    flex-wrap:wrap;
}

.card{
    background:rgba(255,255,255,0.9);
    color:black;
    padding:20px;
    width:250px;
    border-radius:10px;
    transition:0.3s;
}

.card:hover{
    transform:scale(1.05);
}

/* DETAILS SECTION */
.details-box{
    background:rgba(255,255,255,0.9);
    color:black;
    padding:30px;
    max-width:400px;
    margin:auto;
    border-radius:10px;
}

/* SELL SECTION BACKGROUND */
#sell{
    background:
    linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
    url("https://images.unsplash.com/photo-1549924231-f129b911e442");
    background-size:cover;
    background-position:center;
}

.sell-box{
    display:flex;
    flex-direction:column;
    gap:15px;
    max-width:300px;
    margin:auto;
}

.sell-box input{
    padding:10px;
}

.price-display{
    background:black;
    color:white;
    padding:10px;
    border-radius:5px;
}

/* BUTTON */
.btn{
    display:inline-block;
    margin-top:10px;
    padding:8px 15px;
    background:black;
    color:white;
    text-decoration:none;
    border-radius:5px;
}
```


## OUTPUT

<img width="1882" height="1026" alt="image" src="https://github.com/user-attachments/assets/f565cb70-4dfa-4c09-a481-067151cd6aa9" />

<img width="1885" height="1029" alt="image" src="https://github.com/user-attachments/assets/7f37edac-cf8f-4940-85b1-a63500144899" />

<img width="1885" height="1024" alt="image" src="https://github.com/user-attachments/assets/02d610c1-0fdb-4152-9697-f99ccba089fd" />

<img width="1880" height="1030" alt="image" src="https://github.com/user-attachments/assets/89e88f16-b20d-4259-ade0-cfd03a8f1c7a" />



## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
