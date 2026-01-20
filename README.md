# RESPONSIVE-LANDING-PAGE
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Responsive Landing Page</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Poppins', sans-serif;
}

/* ===== NAVBAR ===== */
header{
    position: fixed;
    top:0;
    width:100%;
    padding:18px 60px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    background: transparent;
    transition: 0.4s;
    z-index:1000;
}

header.scrolled{
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    box-shadow: 0 6px 20px rgba(0,0,0,0.3);
}

.logo{
    font-size:28px;
    font-weight:700;
    color:#fff;
}

nav a{
    text-decoration:none;
    margin-left:30px;
    color:#fff;
    font-weight:500;
    position:relative;
    transition:0.3s;
}

nav a::after{
    content:'';
    position:absolute;
    width:0%;
    height:2px;
    background:#ffd700;
    left:0;
    bottom:-6px;
    transition:0.3s;
}

nav a:hover::after{
    width:100%;
}

nav a:hover{
    color:#ffd700;
}

/* ===== HERO SECTION ===== */
.hero{
    height:100vh;
    background: linear-gradient(120deg,#5f2c82,#49a09d);
    display:flex;
    align-items:center;
    justify-content:center;
    color:#fff;
    text-align:center;
    padding:20px;
}

.hero h1{
    font-size:52px;
    margin-bottom:20px;
}

.hero p{
    font-size:18px;
    max-width:600px;
    margin:auto;
}

.hero button{
    margin-top:30px;
    padding:14px 40px;
    border:none;
    border-radius:30px;
    background: linear-gradient(45deg,#ffd700,#ff9800);
    color:#000;
    font-size:16px;
    font-weight:600;
    cursor:pointer;
    transition:0.3s;
}

.hero button:hover{
    transform:scale(1.08);
    box-shadow:0 10px 25px rgba(0,0,0,0.4);
}

/* ===== CONTENT SECTION ===== */
section{
    padding:100px 60px;
}

.cards{
    display:grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
}

.card{
    background:#fff;
    border-radius:20px;
    padding:30px;
    text-align:center;
    box-shadow:0 12px 25px rgba(0,0,0,0.15);
    transition:0.3s;
}

.card:hover{
    transform:translateY(-12px);
    box-shadow:0 20px 40px rgba(0,0,0,0.25);
}

.card h3{
    margin-bottom:15px;
    color:#333;
}

.card p{
    color:#666;
    font-size:14px;
}

/* ===== FOOTER ===== */
footer{
    background:#111;
    color:#aaa;
    text-align:center;
    padding:30px;
}

/* ===== RESPONSIVE ===== */
@media(max-width:768px){
    header{
        padding:15px 30px;
    }
    nav a{
        margin-left:15px;
    }
    .hero h1{
        font-size:38px;
    }
}
</style>
</head>

<body>

<header id="navbar">
    <div class="logo">Task-01</div>
    <nav>
        <a href="#">Home</a>
        <a href="#">Features</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
    </nav>
</header>

<div class="hero">
    <div>
        <h1>Responsive Landing Page</h1>
        <p>Create an interactive navigation menu that changes color on scroll and hover using HTML, CSS and JavaScript.</p>
        <button>Get Started</button>
    </div>
</div>

<section>
    <h2 style="text-align:center;margin-bottom:50px;">Our Features</h2>
    <div class="cards">
        <div class="card">
            <h3>Fixed Navbar</h3>
            <p>Navigation menu remains visible on all pages.</p>
        </div>
        <div class="card">
            <h3>Hover Effects</h3>
            <p>Interactive hover animations for menu items.</p>
        </div>
        <div class="card">
            <h3>Scroll Animation</h3>
            <p>Navbar style changes smoothly on scroll.</p>
        </div>
    </div>
</section>

<footer>
    © 2026 Responsive Landing Page | Designed Beautifully ✨
</footer>

<script>
window.addEventListener("scroll", function(){
    const navbar = document.getElementById("navbar");
    if(window.scrollY > 80){
        navbar.classList.add("scrolled");
    } else {
        navbar.classList.remove("scrolled");
    }
});
</script>

</body>
</html>
