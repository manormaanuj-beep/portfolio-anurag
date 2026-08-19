<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Anurag | Class Monitor Portfolio</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

:root{
    --bg:#050816;
    --card:rgba(255,255,255,0.07);
    --border:rgba(255,255,255,0.15);
    --text:#f5f7ff;
    --muted:#b8bfd8;
    --accent:#8b5cf6;
    --accent2:#06b6d4;
}

body{
    font-family:"Segoe UI",Arial,sans-serif;
    background:
        radial-gradient(circle at 20% 20%,rgba(139,92,246,.20),transparent 30%),
        radial-gradient(circle at 80% 70%,rgba(6,182,212,.15),transparent 30%),
        var(--bg);
    color:var(--text);
    overflow-x:hidden;
}

#particles{
    position:fixed;
    inset:0;
    z-index:-2;
}

.particle{
    position:absolute;
    width:3px;
    height:3px;
    background:white;
    border-radius:50%;
    opacity:.5;
    animation:float 8s infinite ease-in-out;
}

@keyframes float{
    0%,100%{
        transform:translateY(0);
    }
    50%{
        transform:translateY(-40px);
    }
}

nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;

    display:flex;
    justify-content:space-between;
    align-items:center;

    padding:18px 5%;

    background:rgba(5,8,22,.65);
    backdrop-filter:blur(15px);

    border-bottom:1px solid var(--border);
}

.logo{
    font-size:22px;
    font-weight:800;
    letter-spacing:2px;
}

.logo span{
    color:var(--accent2);
}

nav ul{
    display:flex;
    list-style:none;
    gap:25px;
}

nav a{
    color:white;
    text-decoration:none;
    font-size:14px;
    transition:.3s;
}

nav a:hover{
    color:var(--accent2);
}

section{
    min-height:100vh;
    padding:120px 8% 80px;
    display:flex;
    flex-direction:column;
    justify-content:center;
}

.container{
    max-width:1200px;
    width:100%;
    margin:auto;
}

.section-title{
    text-align:center;
    font-size:42px;
    margin-bottom:50px;
}

.section-title span{
    color:var(--accent2);
}

/* HERO */

#home{
    text-align:center;
    position:relative;
}

.hero-small{
    color:var(--accent2);
    letter-spacing:4px;
    text-transform:uppercase;
    font-size:14px;
    margin-bottom:20px;
}

.hero h1{
    font-size:clamp(50px,8vw,100px);
    line-height:1;
    margin-bottom:20px;

    background:linear-gradient(
        90deg,
        #fff,
        #a78bfa,
        #22d3ee,
        #fff
    );

    background-size:300%;
    -webkit-background-clip:text;
    color:transparent;

    animation:gradient 6s infinite;
}

@keyframes gradient{
    0%{background-position:0%}
    50%{background-position:100%}
    100%{background-position:0%}
}

.hero h2{
    font-size:25px;
    font-weight:400;
    color:var(--muted);
}

.hero p{
    max-width:700px;
    margin:25px auto;
    color:var(--muted);
    line-height:1.8;
}

.btn{
    display:inline-block;
    padding:14px 28px;
    margin-top:20px;

    border:1px solid var(--accent2);
    border-radius:50px;

    color:white;
    text-decoration:none;

    transition:.4s;
}

.btn:hover{
    transform:translateY(-5px) scale(1.04);
    background:var(--accent2);
    box-shadow:0 10px 30px rgba(6,182,212,.3);
}

/* CARDS */

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:25px;
}

.card{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:25px;
    padding:30px;

    backdrop-filter:blur(12px);

    transform-style:preserve-3d;
    transition:.4s;

    box-shadow:
        0 20px 50px rgba(0,0,0,.25);
}

.card:hover{
    transform:
        perspective(1000px)
        rotateX(5deg)
        rotateY(-5deg)
        translateY(-10px);

    border-color:rgba(6,182,212,.6);
}

.card h3{
    color:#fff;
    margin-bottom:15px;
    font-size:22px;
}

.card p,
.card li{
    color:var(--muted);
    line-height:1.8;
}

.card ul{
    padding-left:20px;
}

/* PHOTO PLACEHOLDER */

.photo-placeholder{
    width:100%;
    height:330px;

    border-radius:25px;

    border:2px dashed rgba(255,255,255,.25);

    display:flex;
    justify-content:center;
    align-items:center;

    background:
        linear-gradient(
            135deg,
            rgba(139,92,246,.12),
            rgba(6,182,212,.08)
        );

    color:#9ca3af;
    text-align:center;

    margin-bottom:25px;

    overflow:hidden;
}

.photo-placeholder img{
    width:100%;
    height:100%;
    object-fit:cover;
}

/* INTRO */

.intro-layout{
    display:grid;
    grid-template-columns:380px 1fr;
    gap:50px;
    align-items:center;
}

.intro-text{
    font-size:18px;
    line-height:2;
    color:var(--muted);
}

.motto{
    margin-top:25px;
    padding:20px;
    border-left:4px solid var(--accent2);
    background:rgba(255,255,255,.04);
    font-style:italic;
}

/* VISION */

.vision-card{
    min-height:230px;
}

.icon{
    font-size:40px;
    margin-bottom:15px;
}

/* TIMELINE */

.timeline{
    position:relative;
    max-width:900px;
    margin:auto;
}

.timeline::before{
    content:"";
    position:absolute;
    left:50%;
    transform:translateX(-50%);
    width:3px;
    height:100%;
    background:linear-gradient(
        var(--accent),
        var(--accent2)
    );
}

.timeline-item{
    width:50%;
    padding:25px;
    position:relative;
}

.timeline-item:nth-child(odd){
    left:0;
    text-align:right;
}

.timeline-item:nth-child(even){
    left:50%;
}

.timeline-content{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:20px;
    padding:25px;
    transition:.4s;
}

.timeline-content:hover{
    transform:scale(1.04);
}

.timeline-content h3{
    color:var(--accent2);
    margin-bottom:10px;
}

/* LEADERSHIP */

.leadership-box{
    max-width:1000px;
    margin:auto;
}

.leadership-box li{
    margin:15px 0;
}

/* ACHIEVEMENTS */

.achievement-photo{
    height:250px;
}

.achievement-card{
    text-align:center;
}

.trophy{
    font-size:45px;
    margin-bottom:15px;
}

/* EXTRA CURRICULAR */

.activity{
    text-align:center;
}

.activity .photo-placeholder{
    height:260px;
}

/* STRENGTH */

.progress{
    height:8px;
    background:rgba(255,255,255,.1);
    border-radius:20px;
    margin-top:10px;
    overflow:hidden;
}

.progress span{
    display:block;
    height:100%;
    width:90%;
    background:linear-gradient(
        90deg,
        var(--accent),
        var(--accent2)
    );
    animation:grow 2s ease;
}

@keyframes grow{
    from{width:0}
}

/* CONTACT */

.contact{
    text-align:center;
}

.contact-number{
    font-size:35px;
    color:var(--accent2);
    margin:30px 0;
    letter-spacing:2px;
}

.thankyou{
    font-size:70px;
    font-weight:800;

    background:linear-gradient(
        90deg,
        #fff,
        #a78bfa,
        #22d3ee
    );

    -webkit-background-clip:text;
    color:transparent;
}

/* FOOTER */

footer{
    text-align:center;
    padding:30px;
    border-top:1px solid var(--border);
    color:#8f96ae;
}

/* SCROLL */

.reveal{
    opacity:0;
    transform:translateY(60px);
    transition:1s;
}

.reveal.active{
    opacity:1;
    transform:translateY(0);
}

/* MOBILE */

@media(max-width:850px){

    nav ul{
        display:none;
    }

    section{
        padding-left:5%;
        padding-right:5%;
    }

    .intro-layout{
        grid-template-columns:1fr;
    }

    .timeline::before{
        left:10px;
    }

    .timeline-item,
    .timeline-item:nth-child(even),
    .timeline-item:nth-child(odd){
        width:100%;
        left:0;
        text-align:left;
        padding-left:35px;
    }

    .section-title{
        font-size:34px;
    }

    .thankyou{
        font-size:45px;
    }
}

</style>
</head>

<body>

<div id="particles"></div>

<!-- NAVIGATION -->

<nav>

    <div class="logo">
        ANURAG<span>.</span>
    </div>

    <ul>
        <li><a href="#home">Index</a></li>
        <li><a href="#introduction">Introduction</a></li>
        <li><a href="#vision">Vision</a></li>
        <li><a href="#academic">Academic</a></li>
        <li><a href="#leadership">Leadership</a></li>
        <li><a href="#achievements">Awards</a></li>
        <li><a href="#activities">Activities</a></li>
        <li><a href="#growth">Growth</a></li>
        <li><a href="#contact">Connect</a></li>
    </ul>

</nav>


<!-- INDEX -->

<section id="home">

    <div class="container hero">

        <div class="hero-small">
            Student • Leader • Speaker
        </div>

        <h1>Anurag</h1>

        <h2>Class 7 | Class Monitor</h2>

        <p>
            A journey of leadership, learning, public speaking,
            creativity and continuous growth.
        </p>

        <a href="#introduction" class="btn">
            Explore My Journey ↓
        </a>

    </div>

</section>


<!-- INTRODUCTION -->

<section id="introduction">

<div class="container reveal">

<h2 class="section-title">
    <span>01.</span> Introduction
</h2>

<div class="intro-layout">

    <div class="photo-placeholder">

        <span>
            📸<br><br>
            INTRODUCTION PHOTO<br>
            <small>Photo will be added here</small>
        </span>

    </div>

    <div class="intro-text">

        <p>
        I am <strong>Anurag</strong>, a Class 7 student and the
        <strong>Class Monitor</strong>. I believe that leadership
        is not just about holding a position, but about taking
        responsibility, inspiring others, and creating a positive impact.
        </p>

        <br>

        <p>
        My school journey has shaped me through academics,
        leadership, public speaking, competitions, and various
        creative and co-curricular activities.
        </p>

        <br>

        <p>
        As Class Monitor, I strive to lead with
        <strong>dedication, discipline, empathy, and integrity</strong>,
        while encouraging those around me to discover their own potential.
        </p>

        <div class="motto">
            <strong>My Motto:</strong><br>
            “Lead with purpose, serve with humility,
            and inspire through action.”
        </div>

    </div>

</div>

</div>

</section>


<!-- VISION -->

<section id="vision">

<div class="container reveal">

<h2 class="section-title">
    <span>02.</span> My Vision & Goals
</h2>

<div class="grid">

<div class="card vision-card">

<div class="icon">👑</div>

<h3>As a Class Monitor</h3>

<ul>
<li>Lead with integrity, empathy, and responsibility.</li>
<li>Be a voice for classmates.</li>
<li>Help create a positive classroom environment.</li>
<li>Encourage classmates to participate and discover their potential.</li>
<li>Lead by example through discipline and teamwork.</li>
</ul>

</div>


<div class="card vision-card">

<div class="icon">📚</div>

<h3>As an Intelligent & Dedicated Student</h3>

<ul>
<li>Maintain academic excellence.</li>
<li>Develop practical knowledge and critical thinking.</li>
<li>Remain curious and consistent.</li>
<li>Learn beyond textbooks.</li>
<li>Balance academics with responsibilities.</li>
</ul>

</div>


<div class="card vision-card">

<div class="icon">🎤</div>

<h3>As an Anchor & Debater</h3>

<ul>
<li>Become a confident and impactful speaker.</li>
<li>Sharpen communication and reasoning.</li>
<li>Improve quick-thinking skills.</li>
<li>Use my voice to inform and inspire.</li>
</ul>

</div>


<div class="card vision-card">

<div class="icon">🎯</div>

<h3>My Goal</h3>

<p>
To make my school journey meaningful by
<strong>learning continuously, leading responsibly,
speaking fearlessly, and leaving behind a positive legacy.</strong>
</p>

</div>

</div>

</div>

</section>


<!-- ACADEMIC -->

<section id="academic">

<div class="container reveal">

<h2 class="section-title">
    <span>03.</span> Academic Journey
</h2>

<div class="photo-placeholder">

<span>
📸<br><br>
ACADEMIC JOURNEY PHOTOS<br>
<small>Your academic photos will be added here</small>
</span>

</div>


<div class="timeline">

    <div class="timeline-item">

        <div class="timeline-content">

            <h3>School Journey</h3>

            <p>
                My academic journey has been a continuous process
                of learning, curiosity, discipline and improvement.
            </p>

        </div>

    </div>


    <div class="timeline-item">

        <div class="timeline-content">

            <h3>Class 7</h3>

            <p>
                Currently studying in Class 7 and balancing academics
                with leadership, competitions and co-curricular
                responsibilities.
            </p>

        </div>

    </div>


    <div class="timeline-item">

        <div class="timeline-content">

            <h3>Learning Beyond Books</h3>

            <p>
                Along with academics, I have developed my skills in
                public speaking, debating, anchoring, creativity,
                teamwork and leadership.
            </p>

        </div>

    </div>


    <div class="timeline-item">

        <div class="timeline-content">

            <h3>Looking Ahead</h3>

            <p>
                I aim to continue learning, challenging myself and
                transforming every experience into an opportunity
                for growth.
            </p>

        </div>

    </div>

</div>

</div>

</section>


<!-- LEADERSHIP -->

<section id="leadership">

<div class="container reveal">

<h2 class="section-title">
    <span>04.</span> Leadership & Responsibility
</h2>

<div class="card leadership-box">

<p>
As the <strong>Class Monitor</strong>, I have the responsibility
of representing my classmates and contributing to a positive
and disciplined classroom environment.
</p>

<br>

<ul>

<li>
<strong>Student Leadership:</strong>
Representing classmates, listening to their concerns,
and communicating them responsibly.
</li>

<li>
<strong>Class Coordination:</strong>
Helping coordinate classroom activities and ensuring
that tasks are completed properly.
</li>

<li>
<strong>Team Management:</strong>
Working with classmates, sharing responsibilities,
and encouraging effective teamwork.
</li>

<li>
<strong>Discipline & Responsibility:</strong>
Encouraging discipline, punctuality and respect
for classroom values.
</li>

<li>
<strong>Public Speaking:</strong>
Speaking confidently during classroom activities
and school programmes.
</li>

<li>
<strong>Student Engagement:</strong>
Motivating classmates to participate actively
in academics, competitions and activities.
</li>

<li>
<strong>Leading by Example:</strong>
Upholding dedication, discipline, integrity and empathy.
</li>

</ul>

<div class="motto">

For me, leadership is not about being above others—
it is about standing with them, guiding them,
and growing together.

</div>

</div>

</div>

</section>


<!-- ACHIEVEMENTS -->

<section id="achievements">

<div class="container reveal">

<h2 class="section-title">
    <span>05.</span> Achievements & Awards
</h2>

<div class="grid">

    <div class="card achievement-card">

        <div class="photo-placeholder achievement-photo">

            <span>
            🏆<br><br>
            ACHIEVEMENT PHOTO 1
            </span>

        </div>

        <div class="trophy">🏆</div>

        <h3>Achievement</h3>

        <p>
        Your achievement details will be written here
        after your photographs are added.
        </p>

    </div>


    <div class="card achievement-card">

        <div class="photo-placeholder achievement-photo">

            <span>
            🏆<br><br>
            ACHIEVEMENT PHOTO 2
            </span>

        </div>

        <div class="trophy">🥇</div>

        <h3>Award</h3>

        <p>
        Your award details will be added here.
        </p>

    </div>


    <div class="card achievement-card">

        <div class="photo-placeholder achievement-photo">

            <span>
            🏅<br><br>
            ACHIEVEMENT PHOTO 3
            </span>

        </div>

        <div class="trophy">🏅</div>

        <h3>Recognition</h3>

        <p>
        Your recognition details will be added here.
        </p>

    </div>

</div>

</div>

</section>


<!-- EXTRA CURRICULAR -->

<section id="activities">

<div class="container reveal">

<h2 class="section-title">
    <span>06.</span> Extra-Curricular
</h2>

<div class="grid">

<div class="card activity">

<div class="photo-placeholder">

<span>
🎤<br><br>
DEBATE PHOTO<br>
<small>Photo will be added here</small>
</span>

</div>

<h3>Debating</h3>

<p>
Public speaking and debating have helped me develop
reasoning, confidence, quick thinking and the ability
to express ideas effectively.
</p>

</div>


<div class="card activity">

<div class="photo-placeholder">

<span>
🎙️<br><br>
ANCHORING PHOTO<br>
<small>Photo will be added here</small>
</span>

</div>

<h3>Anchoring</h3>

<p>
Anchoring has given me opportunities to connect with
audiences, manage stages and communicate with confidence.
</p>

</div>


<div class="card activity">

<div class="photo-placeholder">

<span>
🎭<br><br>
EVENT PHOTO<br>
<small>Photo will be added here</small>
</span>

</div>

<h3>Creative & Co-Curricular Activities</h3>

<p>
My school journey has also included creative,
cultural and collaborative activities that have helped
me become more expressive and adaptable.
</p>

</div>

</div>

</div>

</section>


<!-- STRENGTH & GROWTH -->

<section id="growth">

<div class="container reveal">

<h2 class="section-title">
    <span>07.</span> Strengths & Growth
</h2>

<div class="grid">

<div class="card">

<h3>Leadership</h3>

<p>
I take responsibility seriously and strive to lead
by example.
</p>

<div class="progress">
<span></span>
</div>

</div>


<div class="card">

<h3>Communication</h3>

<p>
My experience as an anchor and debater has helped me
express my thoughts with confidence and clarity.
</p>

<div class="progress">
<span></span>
</div>

</div>


<div class="card">

<h3>Academic Dedication</h3>

<p>
I am committed to my studies and constantly aim to
improve my understanding and performance.
</p>

<div class="progress">
<span></span>
</div>

</div>


<div class="card">

<h3>Confidence</h3>

<p>
I am comfortable taking the stage, addressing an
audience and handling responsibilities.
</p>

<div class="progress">
<span></span>
</div>

</div>


<div class="card">

<h3>Teamwork</h3>

<p>
I believe in listening to others, valuing different
perspectives and working together.
</p>

<div class="progress">
<span></span>
</div>

</div>


<div class="card">

<h3>Adaptability</h3>

<p>
I am willing to learn from challenges and adjust
myself when situations demand it.
</p>

<div class="progress">
<span></span>
</div>

</div>

</div>

<br><br>

<div class="card">

<h3>My Growth</h3>

<p>
My journey has taught me that growth is not about being
perfect—it is about becoming <strong>better than I was yesterday.</strong>
</p>

<br>

<p>
From academics and public speaking to taking on the
responsibilities of Class Monitor, I have learned to
manage pressure, communicate effectively, make responsible
decisions and work with different people.
</p>

<br>

<p>
I continue to work on becoming more
<strong>patient, organised, confident and resilient</strong>,
while turning every challenge into an opportunity to learn.
</p>

<br>

<div class="motto">

My greatest strength is my willingness to learn,
and my greatest goal is to never stop growing.

</div>

</div>

</div>

</section>


<!-- CONTACT -->

<section id="contact">

<div class="container reveal contact">

<h2 class="section-title">
    <span>08.</span> Contact & Connect
</h2>

<p>
Thank you for taking the time to explore my journey.
</p>

<div class="contact-number">
    ✨ Let's Connect ✨
</div>

<p>
Leadership is a journey, learning is continuous,
and every experience is an opportunity to grow.
</p>

<br><br>

<div class="thankyou">
    THANK YOU
</div>

</div>

</section>


<!-- FOOTER -->

<footer>

© 2026 Anurag • Class 7 • Class Monitor

</footer>


<!-- JAVASCRIPT -->

<script>

/* CREATE PARTICLES */

const particleContainer =
document.getElementById("particles");

for(let i=0;i<80;i++){

    const particle =
    document.createElement("div");

    particle.classList.add("particle");

    particle.style.left =
    Math.random()*100+"%";

    particle.style.top =
    Math.random()*100+"%";

    particle.style.animationDelay =
    Math.random()*8+"s";

    particle.style.animationDuration =
    (5+Math.random()*8)+"s";

    particleContainer.appendChild(particle);
}


/* SCROLL REVEAL */

const reveals =
document.querySelectorAll(".reveal");

function revealOnScroll(){

    reveals.forEach(element=>{

        const windowHeight =
        window.innerHeight;

        const elementTop =
        element.getBoundingClientRect().top;

        if(elementTop < windowHeight-100){

            element.classList.add("active");

        }

    });

}

window.addEventListener(
    "scroll",
    revealOnScroll
);

revealOnScroll();


/* 3D CARD TILT */

const cards =
document.querySelectorAll(".card");

cards.forEach(card=>{

    card.addEventListener("mousemove",(e)=>{

        const rect =
        card.getBoundingClientRect();

        const x =
        e.clientX - rect.left;

        const y =
        e.clientY - rect.top;

        const centerX =
        rect.width/2;

        const centerY =
        rect.height/2;

        const rotateX =
        ((y-centerY)/centerY)*5;

        const rotateY =
        ((x-centerX)/centerX)*-5;

        card.style.transform =
        `perspective(1000px)
         rotateX(${rotateX}deg)
         rotateY(${rotateY}deg)
         translateY(-8px)`;

    });

    card.addEventListener("mouseleave",()=>{

        card.style.transform="";

    });

});

</script>

</body>
</html>
