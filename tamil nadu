<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tamil Nadu — Where Tradition Meets Tomorrow</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:#090909;
    color:white;
    overflow-x:hidden;
}

/* NAVIGATION */
nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    padding:18px 5%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:1000;
    background:rgba(0,0,0,.65);
    backdrop-filter:blur(12px);
    border-bottom:1px solid rgba(255,255,255,.1);
}

.logo{
    font-size:24px;
    font-weight:900;
    letter-spacing:2px;
}

.logo span{
    color:#ffb300;
}

nav a{
    color:white;
    text-decoration:none;
    margin-left:25px;
    font-size:14px;
    transition:.3s;
}

nav a:hover{
    color:#ffb300;
}

/* HERO */
.hero{
    height:100vh;
    min-height:650px;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    position:relative;
    overflow:hidden;
    background:
    linear-gradient(rgba(0,0,0,.45),rgba(0,0,0,.8)),
    url("https://images.unsplash.com/photo-1600100397608-f010cb0d0c5b?auto=format&fit=crop&w=2000&q=85")
    center/cover;
}

.hero::after{
    content:"";
    position:absolute;
    inset:0;
    background:linear-gradient(
        180deg,
        transparent 60%,
        #090909 100%
    );
}

.hero-content{
    position:relative;
    z-index:2;
    max-width:1000px;
    padding:30px;
    animation:fadeUp 1.5s ease;
}

.small-title{
    color:#ffb300;
    letter-spacing:6px;
    font-size:15px;
    margin-bottom:20px;
    text-transform:uppercase;
}

.hero h1{
    font-size:clamp(55px,10vw,130px);
    line-height:.9;
    font-weight:900;
    letter-spacing:-5px;
}

.hero h1 span{
    color:#ffb300;
}

.hero p{
    margin:30px auto;
    max-width:650px;
    font-size:19px;
    line-height:1.7;
    color:#ddd;
}

.btn{
    display:inline-block;
    padding:15px 28px;
    border-radius:40px;
    background:#ffb300;
    color:#111;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

.btn:hover{
    transform:translateY(-4px) scale(1.03);
    box-shadow:0 10px 30px rgba(255,179,0,.3);
}

/* SECTIONS */
section{
    padding:110px 7%;
}

.section-title{
    text-align:center;
    margin-bottom:60px;
}

.section-title small{
    color:#ffb300;
    letter-spacing:4px;
}

.section-title h2{
    font-size:clamp(38px,5vw,70px);
    margin-top:12px;
}

/* INTRO */
.intro{
    text-align:center;
    max-width:950px;
    margin:auto;
}

.intro p{
    color:#bbb;
    font-size:21px;
    line-height:1.9;
}

/* CARDS */
.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
    gap:25px;
    max-width:1200px;
    margin:auto;
}

.card{
    min-height:330px;
    border-radius:22px;
    padding:30px;
    position:relative;
    overflow:hidden;
    display:flex;
    flex-direction:column;
    justify-content:flex-end;
    background-size:cover;
    background-position:center;
    transition:.5s;
    cursor:pointer;
}

.card:hover{
    transform:translateY(-10px) scale(1.02);
}

.card::before{
    content:"";
    position:absolute;
    inset:0;
    background:linear-gradient(
        transparent 25%,
        rgba(0,0,0,.9)
    );
}

.card-content{
    position:relative;
    z-index:2;
}

.card h3{
    font-size:30px;
    margin-bottom:8px;
}

.card p{
    color:#ddd;
    line-height:1.5;
}

/* HERITAGE */
.temple{
    background-image:url("https://images.unsplash.com/photo-1582510003544-4d00b7f74220?auto=format&fit=crop&w=1200&q=85");
}

.nature{
    background-image:url("https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=1200&q=85");
}

.food{
    background-image:url("https://images.unsplash.com/photo-1601050690597-df0568f70950?auto=format&fit=crop&w=1200&q=85");
}

.city{
    background-image:url("https://images.unsplash.com/photo-1595658658481-d53d3f999875?auto=format&fit=crop&w=1200&q=85");
}

/* TIMELINE */
.timeline{
    max-width:900px;
    margin:auto;
    position:relative;
}

.timeline::before{
    content:"";
    position:absolute;
    left:50%;
    transform:translateX(-50%);
    width:3px;
    height:100%;
    background:#ffb300;
}

.timeline-item{
    width:50%;
    padding:25px 45px;
    position:relative;
}

.timeline-item:nth-child(odd){
    left:0;
    text-align:right;
}

.timeline-item:nth-child(even){
    left:50%;
}

.timeline-item::after{
    content:"";
    position:absolute;
    top:30px;
    width:15px;
    height:15px;
    background:#ffb300;
    border-radius:50%;
    border:4px solid #090909;
}

.timeline-item:nth-child(odd)::after{
    right:-9px;
}

.timeline-item:nth-child(even)::after{
    left:-9px;
}

.timeline-item h3{
    color:#ffb300;
    font-size:25px;
}

.timeline-item p{
    margin-top:8px;
    color:#bbb;
    line-height:1.6;
}

/* STATS */
.stats{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    max-width:1100px;
    margin:auto;
    gap:20px;
}

.stat{
    text-align:center;
    padding:30px;
    border:1px solid #292929;
    border-radius:20px;
    background:#111;
}

.stat strong{
    display:block;
    font-size:45px;
    color:#ffb300;
}

.stat span{
    color:#aaa;
}

/* FINAL */
.final{
    min-height:80vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    background:
    radial-gradient(circle at center,#493000 0%,#090909 55%);
}

.final h2{
    font-size:clamp(45px,8vw,100px);
    line-height:1;
}

.final h2 span{
    color:#ffb300;
}

.final p{
    color:#aaa;
    font-size:20px;
    margin:25px auto;
    max-width:650px;
}

/* FOOTER */
footer{
    padding:30px;
    text-align:center;
    background:#050505;
    color:#777;
}

/* ANIMATION */
@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(40px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.reveal{
    opacity:0;
    transform:translateY(50px);
    transition:1s;
}

.reveal.active{
    opacity:1;
    transform:translateY(0);
}

/* MOBILE */
@media(max-width:700px){

    nav .links{
        display:none;
    }

    .stats{
        grid-template-columns:repeat(2,1fr);
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
        padding-left:45px;
        padding-right:10px;
    }

    .timeline-item::after,
    .timeline-item:nth-child(odd)::after,
    .timeline-item:nth-child(even)::after{
        left:3px;
        right:auto;
    }
}
</style>
</head>

<body>

<nav>
    <div class="logo">TAMIL<span>NADU</span></div>

    <div class="links">
        <a href="#heritage">Heritage</a>
        <a href="#culture">Culture</a>
        <a href="#nature">Nature</a>
        <a href="#future">Future</a>
    </div>
</nav>

<!-- HERO -->
<section class="hero">

    <div class="hero-content">

        <div class="small-title">
            Incredible India • Tamil Nadu
        </div>

        <h1>
            TAMIL<br>
            <span>NADU</span>
        </h1>

        <p>
            Where ancient civilization, magnificent temples,
            living traditions and modern innovation come together.
        </p>

        <a class="btn" href="#heritage">
            EXPLORE ↓
        </a>

    </div>

</section>

<!-- INTRO -->
<section>

    <div class="section-title reveal">
        <small>THE SOUL OF SOUTH INDIA</small>
        <h2>A Land of Stories</h2>
    </div>

    <div class="intro reveal">

        <p>
            Tamil Nadu is a state where history is not locked inside
            museums — it lives in its temples, languages, festivals,
            music, food, architecture and everyday traditions.
        </p>

    </div>

</section>

<!-- HERITAGE -->
<section id="heritage">

    <div class="section-title reveal">
        <small>01 • HERITAGE</small>
        <h2>Built to Last</h2>
    </div>

    <div class="grid">

        <div class="card temple reveal">
            <div class="card-content">
                <h3>Great Temples</h3>
                <p>
                    Architectural masterpieces such as the
                    Brihadisvara Temple tell stories carved in stone.
                </p>
            </div>
        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1606298855672-3efb63017be8?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>Mahabalipuram</h3>
                <p>
                    Ancient monuments and rock-cut architecture
                    overlooking the Bay of Bengal.
                </p>
            </div>

        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1587135941948-670b381f08ce?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>Madurai</h3>
                <p>
                    A historic cultural centre famous for the
                    magnificent Meenakshi Amman Temple.
                </p>
            </div>

        </div>

    </div>

</section>

<!-- CULTURE -->
<section id="culture">

    <div class="section-title reveal">
        <small>02 • CULTURE</small>
        <h2>A Culture That Dances</h2>
    </div>

    <div class="grid">

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1600605731444-5c2c3e2e2f44?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>💃 Bharatanatyam</h3>
                <p>
                    One of India's most celebrated classical dance
                    traditions.
                </p>
            </div>

        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1548013146-72479768bada?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>🎵 Music</h3>
                <p>
                    Carnatic music forms an important part of
                    Tamil Nadu's artistic heritage.
                </p>
            </div>

        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1590050752117-23a9d0b0b4b4?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>🌾 Pongal</h3>
                <p>
                    A harvest festival celebrating gratitude,
                    nature and community.
                </p>
            </div>

        </div>

    </div>

</section>

<!-- FOOD -->
<section>

    <div class="section-title reveal">
        <small>03 • FLAVOURS</small>
        <h2>Taste of Tamil Nadu</h2>
    </div>

    <div class="grid">

        <div class="card food reveal">
            <div class="card-content">
                <h3>South Indian Cuisine</h3>
                <p>
                    From dosa and idli to sambar and Chettinad
                    specialties, food is deeply connected to culture.
                </p>
            </div>
        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1589302168068-964664d93dc0?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>Banana Leaf</h3>
                <p>
                    Traditional meals served on banana leaves turn
                    eating into a cultural experience.
                </p>
            </div>

        </div>

    </div>

</section>

<!-- NATURE -->
<section id="nature">

    <div class="section-title reveal">
        <small>04 • NATURE</small>
        <h2>From Hills to the Sea</h2>
    </div>

    <div class="grid">

        <div class="card nature reveal">

            <div class="card-content">
                <h3>Nilgiris</h3>
                <p>
                    Misty mountains, tea gardens and the famous
                    Nilgiri Mountain Railway.
                </p>
            </div>

        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>Coastline</h3>
                <p>
                    Tamil Nadu's eastern coastline stretches along
                    the Bay of Bengal.
                </p>
            </div>

        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>Western Ghats</h3>
                <p>
                    Biodiversity-rich landscapes, forests and
                    spectacular hill regions.
                </p>
            </div>

        </div>

    </div>

</section>

<!-- TIMELINE -->
<section>

    <div class="section-title reveal">
        <small>05 • HISTORY</small>
        <h2>A Journey Through Time</h2>
    </div>

    <div class="timeline">

        <div class="timeline-item reveal">
            <h3>Sangam Age</h3>
            <p>
                Tamil literature flourished during the ancient
                Sangam tradition.
            </p>
        </div>

        <div class="timeline-item reveal">
            <h3>Chola Era</h3>
            <p>
                The Cholas became renowned for administration,
                maritime influence and temple architecture.
            </p>
        </div>

        <div class="timeline-item reveal">
            <h3>Temple Civilization</h3>
            <p>
                Major temple cities became centres of art,
                education and community life.
            </p>
        </div>

        <div class="timeline-item reveal">
            <h3>Modern Tamil Nadu</h3>
            <p>
                Today the state combines its cultural heritage
                with education, manufacturing and technology.
            </p>
        </div>

    </div>

</section>

<!-- CHENNAI -->
<section id="future">

    <div class="section-title reveal">
        <small>06 • TOMORROW</small>
        <h2>Tradition Meets Innovation</h2>
    </div>

    <div class="grid">

        <div class="card city reveal">

            <div class="card-content">
                <h3>Chennai</h3>
                <p>
                    A major centre for education, technology,
                    automobiles, healthcare and culture.
                </p>
            </div>

        </div>

        <div class="card reveal"
        style="background-image:url('https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=1200&q=85')">

            <div class="card-content">
                <h3>Innovation</h3>
                <p>
                    Tamil Nadu's modern economy is powered by
                    industry, research, technology and entrepreneurship.
                </p>
            </div>

        </div>

    </div>

</section>

<!-- STATS -->
<section>

    <div class="section-title reveal">
        <small>07 • AT A GLANCE</small>
        <h2>Tamil Nadu in Numbers</h2>
    </div>

    <div class="stats">

        <div class="stat reveal">
            <strong>38</strong>
            <span>Districts</span>
        </div>

        <div class="stat reveal">
            <strong>₹</strong>
            <span>Major economic powerhouse</span>
        </div>

        <div class="stat reveal">
            <strong>4</strong>
            <span>UNESCO World Heritage Sites* </span>
        </div>

        <div class="stat reveal">
            <strong>∞</strong>
            <span>Stories to discover</span>
        </div>

    </div>

    <p style="text-align:center;color:#666;margin-top:20px;font-size:12px;">
        *UNESCO listing/count should be checked against the latest official information before competition use.
    </p>

</section>

<!-- FINAL -->
<section class="final">

    <div class="reveal">

        <div class="small-title">
            THE FINAL CHAPTER
        </div>

        <h2>
            NOT JUST A PLACE.<br>
            <span>A STORY.</span>
        </h2>

        <p>
            Tamil Nadu carries its past forward —
            preserving tradition while building the future.
        </p>

        <a class="btn" href="#top">
            ↑ BACK TO TOP
        </a>

    </div>

</section>

<footer>
    Made for Canva Fest • Tamil Nadu — Where Tradition Meets Tomorrow
</footer>

<script>

const revealElements =
document.querySelectorAll(".reveal");

const observer =
new IntersectionObserver((entries)=>{

    entries.forEach(entry=>{

        if(entry.isIntersecting){
            entry.target.classList.add("active");
        }

    });

},{
    threshold:.15
});

revealElements.forEach(el=>{
    observer.observe(el);
});

</script>

</body>
</html>
