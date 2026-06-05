<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Version B</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:linear-gradient(135deg,#0f172a,#111827,#1e293b);
    color:white;
    overflow-x:hidden;
}

/* NAVBAR */

nav{
    width:100%;
    padding:20px 50px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    position:fixed;
    top:0;
    background:rgba(0,0,0,0.3);
    backdrop-filter:blur(10px);
    z-index:1000;

    transform:translateY(-100%);
    animation:dropNav 1s ease forwards;
}

@keyframes dropNav{
    to{
        transform:translateY(0);
    }
}

.logo{
    font-size:28px;
    font-weight:bold;
    color:#38bdf8;
}

nav ul{
    display:flex;
    list-style:none;
    gap:25px;
}

nav ul li a{
    text-decoration:none;
    color:white;
    transition:0.3s;
}

nav ul li a:hover{
    color:#38bdf8;
}

/* HERO */

.hero{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:20px;
}

.hero h1{
    font-size:65px;
    margin-bottom:20px;
    opacity:0;
    transform:scale(0.5);

    animation:popHeading 1s ease forwards 1s;
}

@keyframes popHeading{
    to{
        opacity:1;
        transform:scale(1);
    }
}

.hero p{
    width:70%;
    font-size:18px;
    color:#cbd5e1;
    line-height:1.7;

    opacity:0;
    animation:fadePara 1.5s ease forwards 2s;
}

@keyframes fadePara{
    to{
        opacity:1;
    }
}

/* BUTTON */

.btn{
    margin-top:30px;
    padding:15px 35px;
    border:none;
    border-radius:50px;
    background:#38bdf8;
    color:white;
    font-size:18px;
    cursor:pointer;
    transition:0.4s;
    box-shadow:0 0 20px rgba(56,189,248,0.4);

    transform:scale(0);
    animation:zoomBtn 1s ease forwards 2.5s;
}

@keyframes zoomBtn{
    to{
        transform:scale(1);
    }
}

.btn:hover{
    transform:scale(1.1);
    box-shadow:0 0 30px #38bdf8;
}

/* CARDS */

.cards{
    width:90%;
    margin:50px auto 100px;
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,255,255,0.1);
    padding:30px;
    border-radius:20px;
    backdrop-filter:blur(10px);

    opacity:0;
    transform:translateY(80px);

    animation:slideUp 1s ease forwards;
    transition:0.4s;
}

.card:nth-child(1){ animation-delay:3s; }
.card:nth-child(2){ animation-delay:3.3s; }
.card:nth-child(3){ animation-delay:3.6s; }
.card:nth-child(4){ animation-delay:3.9s; }
.card:nth-child(5){ animation-delay:4.2s; }
.card:nth-child(6){ animation-delay:4.5s; }

@keyframes slideUp{
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.card:hover{
    transform:translateY(-10px) scale(1.05);
    box-shadow:0 0 30px rgba(56,189,248,0.4);
    border-color:#38bdf8;
}

.card h2{
    margin-bottom:15px;
    color:#38bdf8;
}

.card p{
    color:#cbd5e1;
    line-height:1.6;
}

/* EXTRA GLOW CIRCLES */

.glow1,
.glow2{
    position:absolute;
    border-radius:50%;
    filter:blur(100px);
    z-index:-1;
}

.glow1{
    width:300px;
    height:300px;
    background:#38bdf8;
    top:100px;
    left:-100px;
}

.glow2{
    width:300px;
    height:300px;
    background:#8b5cf6;
    bottom:100px;
    right:-100px;
}

/* POPUP */

.popup{
    position:fixed;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%) scale(0);
    background:#111827;
    padding:30px 50px;
    border-radius:20px;
    box-shadow:0 0 30px rgba(56,189,248,0.5);
    text-align:center;
    transition:0.4s;
    z-index:9999;
}

.popup.active{
    transform:translate(-50%,-50%) scale(1);
}

.popup h2{
    margin-bottom:10px;
    color:#38bdf8;
}

/* FOOTER */

footer{
    text-align:center;
    padding:30px;
    color:#94a3b8;
    border-top:1px solid rgba(255,255,255,0.1);
}

/* RESPONSIVE */

@media(max-width:768px){

    .hero h1{
        font-size:45px;
    }

    .hero p{
        width:100%;
    }

    nav{
        padding:20px;
    }

    nav ul{
        gap:15px;
    }
}

</style>
</head>

<body>

<div class="glow1"></div>
<div class="glow2"></div>

<!-- NAVBAR -->

<nav>

<div class="logo">AI Version B</div>

<ul>
<li><a href="#">Home</a></li>
<li><a href="#">About</a></li>
<li><a href="#">Services</a></li>
<li><a href="#">Features</a></li>
<li><a href="#">Contact</a></li>
</ul>

</nav>

<!-- HERO -->

<section class="hero">

<h1>Future AI Experience</h1>

<p>
Modern AI website with smooth animations, premium glassmorphism design,
interactive cards and beautiful effects that create a real professional feel.
</p>

<button class="btn" onclick="showPopup()">
Launch AI
</button>

</section>

<!-- CARDS -->

<section class="cards">

<div class="card">
<h2>AI Automation</h2>
<p>Automate smart workflows with modern AI technology.</p>
</div>

<div class="card">
<h2>Cloud System</h2>
<p>Fast and secure cloud-based infrastructure solutions.</p>
</div>

<div class="card">
<h2>Cyber Security</h2>
<p>Advanced protection and security for all platforms.</p>
</div>

<div class="card">
<h2>Smart Analytics</h2>
<p>Track performance and insights with AI dashboards.</p>
</div>

<div class="card">
<h2>Responsive UI</h2>
<p>Beautiful layouts that work perfectly on every device.</p>
</div>

<div class="card">
<h2>Future Tech</h2>
<p>Experience futuristic digital systems with premium UI.</p>
</div>

</section>

<!-- POPUP -->

<div class="popup" id="popup">

<h2>🚀 AI Activated</h2>

<p>Welcome to the Future Experience</p>

</div>

<!-- FOOTER -->

<footer>
© 2026 AI Version B | All Rights Reserved
</footer>

<script>

function showPopup(){

    let popup = document.getElementById("popup");

    popup.classList.add("active");

    setTimeout(()=>{
        popup.classList.remove("active");
    },2500);
}

</script>

</body>
</html>
