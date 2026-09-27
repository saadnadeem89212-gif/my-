```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lahore Restaurant | Kharian</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

body{
    font-family:Arial, sans-serif;
    background:#0b0b0b;
    color:white;
    overflow-x:hidden;
}

/* NAVBAR */
nav{
    position:fixed;
    top:0;
    width:100%;
    z-index:1000;
    padding:18px 7%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    background:rgba(0,0,0,.75);
    backdrop-filter:blur(12px);
    border-bottom:1px solid rgba(255,255,255,.08);
}

.logo{
    font-size:25px;
    font-weight:bold;
    color:#ffb300;
}

.logo span{
    color:white;
}

nav ul{
    display:flex;
    list-style:none;
    gap:28px;
}

nav a{
    color:white;
    text-decoration:none;
    transition:.3s;
}

nav a:hover{
    color:#ffb300;
}

.menu-btn{
    display:none;
    font-size:28px;
    cursor:pointer;
}

/* HERO */
.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    position:relative;
    overflow:hidden;
    background:
      radial-gradient(circle at 20% 30%,#5b2700 0%,transparent 30%),
      radial-gradient(circle at 80% 70%,#3d1800 0%,transparent 30%),
      #080808;
}

.hero-content{
    position:relative;
    z-index:2;
    animation:heroIn 1.5s ease;
}

.badge{
    display:inline-block;
    padding:9px 18px;
    border:1px solid #ffb300;
    border-radius:30px;
    color:#ffb300;
    margin-bottom:20px;
    animation:pulse 2s infinite;
}

.hero h1{
    font-size:clamp(45px,8vw,90px);
    line-height:1;
    margin-bottom:20px;
}

.hero h1 span{
    color:#ffb300;
}

.hero p{
    max-width:650px;
    margin:auto;
    color:#ccc;
    font-size:18px;
    line-height:1.7;
}

.buttons{
    margin-top:30px;
    display:flex;
    justify-content:center;
    gap:15px;
    flex-wrap:wrap;
}

.btn{
    padding:14px 27px;
    border-radius:30px;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

.primary{
    background:#ffb300;
    color:#111;
}

.secondary{
    border:1px solid #555;
    color:white;
}

.btn:hover{
    transform:translateY(-5px) scale(1.03);
    box-shadow:0 10px 30px rgba(255,179,0,.25);
}

/* FLOATING FOOD */
.food{
    position:absolute;
    font-size:55px;
    opacity:.18;
    animation:float 6s ease-in-out infinite;
}

.food1{left:8%;top:25%;}
.food2{right:10%;top:20%;animation-delay:1s;}
.food3{left:15%;bottom:15%;animation-delay:2s;}
.food4{right:15%;bottom:12%;animation-delay:3s;}

@keyframes float{
    0%,100%{transform:translateY(0) rotate(0deg);}
    50%{transform:translateY(-35px) rotate(10deg);}
}

@keyframes heroIn{
    from{opacity:0;transform:translateY(40px);}
    to{opacity:1;transform:translateY(0);}
}

@keyframes pulse{
    50%{box-shadow:0 0 25px rgba(255,179,0,.3);}
}

/* SECTIONS */
section{
    padding:90px 7%;
}

.title{
    text-align:center;
    margin-bottom:50px;
}

.title h2{
    font-size:42px;
}

.title span{
    color:#ffb300;
}

.title p{
    color:#aaa;
    margin-top:10px;
}

/* ABOUT */
.about{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:50px;
    align-items:center;
}

.about-box{
    background:linear-gradient(145deg,#191919,#101010);
    border:1px solid #292929;
    padding:40px;
    border-radius:25px;
    box-shadow:0 20px 50px rgba(0,0,0,.3);
}

.about-box h3{
    font-size:30px;
    margin-bottom:15px;
    color:#ffb300;
}

.about-box p{
    color:#bbb;
    line-height:1.8;
}

.stats{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:15px;
}

.stat{
    padding:30px;
    text-align:center;
    border-radius:20px;
    background:#151515;
    border:1px solid #292929;
    transition:.3s;
}

.stat:hover{
    transform:translateY(-8px);
    border-color:#ffb300;
}

.stat h3{
    font-size:35px;
    color:#ffb300;
}

/* MENU */
.menu-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:25px;
}

.card{
    background:#151515;
    border:1px solid #292929;
    border-radius:22px;
    padding:30px;
    text-align:center;
    transition:.4s;
    position:relative;
    overflow:hidden;
}

.card:hover{
    transform:translateY(-12px);
    border-color:#ffb300;
    box-shadow:0 20px 50px rgba(255,179,0,.12);
}

.card .icon{
    font-size:65px;
    margin-bottom:15px;
    transition:.4s;
}

.card:hover .icon{
    transform:scale(1.2) rotate(5deg);
}

.card h3{
    font-size:23px;
    margin-bottom:10px;
}

.card p{
    color:#aaa;
    font-size:14px;
    line-height:1.6;
}

.price{
    display:block;
    margin-top:18px;
    color:#ffb300;
    font-size:22px;
    font-weight:bold;
}

/* OFFER */
.offer{
    background:
      linear-gradient(90deg,rgba(0,0,0,.9),rgba(30,15,0,.75)),
      radial-gradient(circle,#8b4500,#080808);
    border-radius:30px;
    padding:70px 30px;
    text-align:center;
    border:1px solid #4a3000;
}

.offer h2{
    font-size:45px;
}

.offer h2 span{
    color:#ffb300;
}

.offer p{
    margin:15px auto 25px;
    color:#ddd;
}

/* LOCATION */
.location{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:30px;
}

.info{
    background:#151515;
    padding:35px;
    border-radius:25px;
    border:1px solid #292929;
}

.info h3{
    color:#ffb300;
    margin-bottom:20px;
}

.info p{
    color:#bbb;
    margin:14px 0;
}

.map{
    min-height:300px;
    border-radius:25px;
    background:
      linear-gradient(rgba(255,179,0,.08),rgba(255,179,0,.03)),
      #151515;
    border:1px solid #292929;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:70px;
}

/* FOOTER */
footer{
    text-align:center;
    padding:35px;
    background:#050505;
    border-top:1px solid #222;
    color:#888;
}

footer strong{
    color:#ffb300;
}

/* REVEAL */
.reveal{
    opacity:0;
    transform:translateY(50px);
    transition:1s;
}

.reveal.active{
    opacity:1;
    transform:translateY(0);
}

/* RESPONSIVE */
@media(max-width:800px){
    nav ul{
        display:none;
        position:absolute;
        top:70px;
        left:0;
        width:100%;
        background:#101010;
        flex-direction:column;
        text-align:center;
        padding:25px;
    }

    nav ul.show{
        display:flex;
    }

    .menu-btn{
        display:block;
    }

    .about,
    .location{
        grid-template-columns:1fr;
    }

    .menu-grid{
        grid-template-columns:1fr;
    }

    .hero h1{
        font-size:50px;
    }
}
</style>
</head>

<body>

<nav>
    <div class="logo">Lahore <span>Restaurant</span></div>

    <ul id="navLinks">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#offers">Offers</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>

    <div class="menu-btn" onclick="toggleMenu()">☰</div>
</nav>

<!-- HERO -->
<section class="hero" id="home">

    <div class="food food1">🍕</div>
    <div class="food food2">🍔</div>
    <div class="food food3">🍗</div>
    <div class="food food4">🍟</div>

    <div class="hero-content">
        <div class="badge">📍 Kharian</div>

        <h1>
            Taste of <span>Lahore</span>
        </h1>

        <p>
            Authentic Pakistani flavors, delicious BBQ,
            juicy burgers and traditional desi food —
            all served with a modern restaurant experience.
        </p>

        <div class="buttons">
            <a href="#menu" class="btn primary">🍽️ Explore Menu</a>
            <a href="#contact" class="btn secondary">📍 Visit Us</a>
        </div>
    </div>
</section>

<!-- ABOUT -->
<section id="about" class="reveal">

    <div class="title">
        <h2>About <span>Us</span></h2>
        <p>A taste you will remember.</p>
    </div>

    <div class="about">

        <div class="about-box">
            <h3>Welcome to Lahore Restaurant</h3>
            <p>
                Experience the rich taste of Pakistani cuisine
                in Kharian. From traditional desi dishes to
                delicious BBQ and fast food, we prepare every
                meal with care and passion.
            </p>
        </div>

        <div class="stats">
            <div class="stat">
                <h3>50+</h3>
                <p>Food Items</p>
            </div>

            <div class="stat">
                <h3>4.8★</h3>
                <p>Customer Rating</p>
            </div>

            <div class="stat">
                <h3>100%</h3>
                <p>Fresh Food</p>
            </div>

            <div class="stat">
                <h3>24/7</h3>
                <p>Love for Food</p>
            </div>
        </div>

    </div>
</section>

<!-- MENU -->
<section id="menu" class="reveal">

    <div class="title">
        <h2>Our <span>Menu</span></h2>
        <p>Some customer favorites</p>
    </div>

    <div class="menu-grid">

        <div class="card">
            <div class="icon">🍗</div>
            <h3>Chicken Karahi</h3>
            <p>Traditional spicy chicken karahi with fresh ingredients.</p>
            <span class="price">Rs. 1,299</span>
        </div>

        <div class="card">
            <div class="icon">🍖</div>
            <h3>BBQ Platter</h3>
            <p>Juicy seekh kebab, tikka and delicious BBQ selection.</p>
            <span class="price">Rs. 1,599</span>
        </div>

        <div class="card">
            <div class="icon">🍔</div>
            <h3>Special Burger</h3>
            <p>Loaded burger with crispy chicken and special sauce.</p>
            <span class="price">Rs. 599</span>
        </div>

        <div class="card">
            <div class="icon">🍕</div>
            <h3>Special Pizza</h3>
            <p>Cheesy pizza loaded with fresh toppings.</p>
            <span class="price">Rs. 999</span>
        </div>

        <div class="card">
            <div class="icon">🍚</div>
            <h3>Chicken Biryani</h3>
            <p>Fragrant basmati rice with spicy chicken and masala.</p>
            <span class="price">Rs. 450</span>
        </div>

        <div class="card">
            <div class="icon">🥤</div>
            <h3>Cold Drinks</h3>
            <p>Chilled drinks to complete your delicious meal.</p>
            <span class="price">Rs. 150</span>
        </div>

    </div>
</section>

<!-- OFFER -->
<section id="offers" class="reveal">

    <div class="offer">
        <h2>🔥 Special <span>Deal</span></h2>

        <p>
            Get a complete family meal with BBQ,
            karahi, naan and drinks.
        </p>

        <a href="#contact" class="btn primary">
            Order / Contact
        </a>
    </div>

</section>

<!-- LOCATION -->
<section id="contact" class="reveal">

    <div class="title">
        <h2>Visit <span>Us</span></h2>
        <p>Come and enjoy the taste of Lahore in Kharian.</p>
    </div>

    <div class="location">

        <div class="info">
            <h3>📍 Restaurant Information</h3>

            <p>📌 <strong>Location:</strong> Kharian, Punjab, Pakistan</p>
            <p>🍽️ <strong>Restaurant:</strong> Lahore Restaurant</p>
            <p>🕐 <strong>Opening:</strong> 11:00 AM – 11:00 PM</p>
            <p>📞 <strong>Phone:</strong> 0300-0000000</p>

            <a class="btn primary"
               href="tel:03000000000">
               📞 Call Now
            </a>
        </div>

        <div class="map">
            📍
        </div>

    </div>
</section>

<footer>
    © 2026 <strong>Lahore Restaurant Kharian</strong> — All Rights Reserved.
</footer>

<script>

/* MOBILE MENU */
function toggleMenu(){
    document.getElementById("navLinks").classList.toggle("show");
}

/* SCROLL ANIMATION */
const reveals = document.querySelectorAll(".reveal");

function revealOnScroll(){

    reveals.forEach(element => {

        const windowHeight = window.innerHeight;
        const elementTop = element.getBoundingClientRect().top;

        if(elementTop < windowHeight - 100){
            element.classList.add("active");
        }

    });
}

window.addEventListener("scroll", revealOnScroll);
revealOnScroll();

/* CLOSE MOBILE MENU */
document.querySelectorAll("nav a").forEach(link => {
    link.addEventListener("click", () => {
        document.getElementById("navLinks").classList.remove("show");
    });
});

</script>

</body>
</html>
```
