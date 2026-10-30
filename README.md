```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Yogesh | Portfolio</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

:root {
    --cyan: #00eaff;
    --purple: #b34dff;
    --background: #060914;
    --card: #10182b;
    --text: #eaf3ff;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: var(--background);
    color: var(--text);
    line-height: 1.7;
    overflow-x: hidden;
}

a {
    color: inherit;
    text-decoration: none;
}

section {
    scroll-margin-top: 90px;
}

/* NAVIGATION */

header {
    background: #080d1b;
    border-bottom: 1px solid var(--cyan);
    position: sticky;
    top: 0;
    z-index: 10;
}

nav {
    max-width: 1200px;
    margin: auto;
    padding: 18px 25px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.logo {
    font-size: 28px;
    font-weight: bold;
    letter-spacing: 3px;
}

.logo span {
    color: var(--cyan);
}

nav ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    list-style: none;
}

nav ul a {
    transition: 0.3s;
}

nav ul a:hover {
    color: var(--cyan);
}

/* HOME */

.hero {
    min-height: 650px;
    padding: 80px 7%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 40px;
    background:
        radial-gradient(ellipse at 80% 40%,
        #142957 0%, transparent 55%),
        var(--background);
}

.hero-text {
    flex: 1 1 350px;
    animation: appear 1s ease;
}

.tag {
    color: var(--cyan);
    font-size: 13px;
    letter-spacing: 4px;
    margin-bottom: 20px;
}

.hero h1 {
    font-size: clamp(42px, 6vw, 70px);
    line-height: 1.2;
    margin-bottom: 15px;
}

.cyan {
    color: var(--cyan);
}

.purple {
    color: var(--purple);
}

.hero h2 {
    color: var(--purple);
    font-size: 23px;
    margin-bottom: 18px;
}

.hero p {
    color: #c3cde0;
    max-width: 550px;
}

.buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    margin-top: 28px;
}

.btn {
    display: inline-block;
    padding: 11px 23px;
    border: 1px solid var(--cyan);
    border-radius: 30px;
    transition: 0.3s;
}

.btn.primary {
    background: var(--cyan);
    color: #06101b;
    font-weight: bold;
}

.btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 0 20px #00eaff66;
}

.btn.secondary {
    border-color: var(--purple);
}

/* SPORTS CAR ILLUSTRATION */

.hero-car {
    flex: 1 1 400px;
    min-width: 0;
    text-align: center;
}

.car-art {
    width: 100%;
    max-width: 600px;
    height: auto;
    overflow: visible;
    filter: drop-shadow(0 0 20px #008cff66);
    animation: float 4s ease-in-out infinite;
}

/* SECTIONS */

.content-section {
    padding: 80px 7%;
    max-width: 1300px;
    margin: auto;
}

.section-title {
    text-align: center;
    font-size: clamp(30px, 4vw, 42px);
    margin-bottom: 10px;
}

.section-subtitle {
    text-align: center;
    color: var(--cyan);
    font-size: 12px;
    letter-spacing: 4px;
    margin-bottom: 40px;
}

/* ABOUT */

.about-box {
    max-width: 850px;
    margin: auto;
    padding: 30px;
    border: 1px solid #24415d;
    border-radius: 15px;
    background: var(--card);
    transition: 0.3s;
}

.about-box:hover {
    border-color: var(--cyan);
}

.about-box h3 {
    color: var(--cyan);
    margin-bottom: 12px;
}

.about-box p {
    color: #c3cde0;
    margin-bottom: 12px;
}

.education {
    margin-top: 20px;
    color: var(--purple);
}

/* SKILLS AND PROJECTS */

.grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 22px;
}

.card {
    padding: 28px 20px;
    text-align: center;
    background: var(--card);
    border: 1px solid #24324a;
    border-radius: 14px;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-7px);
    border-color: var(--cyan);
    box-shadow: 0 0 20px #00eaff22;
}

.icon {
    font-size: 42px;
    margin-bottom: 12px;
}

.card h3 {
    color: var(--cyan);
    margin-bottom: 10px;
}

.card p {
    color: #c3cde0;
    font-size: 14px;
}

/* ALTERNATE BACKGROUND */

.alternate {
    max-width: none;
    background: #090f1e;
}

.alternate-inner {
    max-width: 1150px;
    margin: auto;
}

/* DREAM SPORTS CAR */

.sports-box {
    padding: 25px;
    border: 1px solid #21445f;
    border-radius: 20px;
    background:
        radial-gradient(ellipse at 50% 50%,
        #102b4b 0%, #0a1020 65%);
}

.sports-box .car-art {
    display: block;
    margin: 0 auto;
}

.car-caption {
    text-align: center;
    margin-top: 20px;
    font-size: 26px;
    letter-spacing: 3px;
    color: var(--cyan);
}

.car-description {
    text-align: center;
    max-width: 700px;
    margin: 15px auto;
    color: #c3cde0;
}

.car-specs {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 15px;
    margin-top: 25px;
}

.spec {
    padding: 12px 20px;
    border: 1px solid #334560;
    border-radius: 10px;
    text-align: center;
}

.spec strong {
    display: block;
    color: var(--purple);
}

/* CONTACT */

.contact-box {
    max-width: 650px;
    margin: auto;
    padding: 35px;
    text-align: center;
    background: var(--card);
    border: 1px solid #24415d;
    border-radius: 15px;
}

.contact-box p {
    color: #c3cde0;
    margin: 15px 0 25px;
}

/* FOOTER */

footer {
    padding: 25px 15px;
    text-align: center;
    background: #03060d;
    border-top: 1px solid #1b3c52;
    color: #aebbd0;
    font-size: 13px;
}

footer span {
    color: var(--cyan);
}

/* ANIMATIONS */

@keyframes float {
    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-10px);
    }
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateX(-25px);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

/* TABLET AND MOBILE */

@media (max-width: 800px) {
    nav {
        flex-direction: column;
    }

    nav ul {
        gap: 12px 18px;
    }

    nav ul a {
        font-size: 13px;
    }

    .hero {
        padding: 55px 6%;
        text-align: center;
    }

    .hero p {
        margin-left: auto;
        margin-right: auto;
    }

    .buttons {
        justify-content: center;
    }

    .hero-car {
        flex-basis: 100%;
    }

    .grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .content-section {
        padding: 60px 6%;
    }
}

@media (max-width: 500px) {
    .grid {
        grid-template-columns: 1fr;
    }

    .hero h2 {
        font-size: 19px;
    }

    .sports-box {
        padding: 12px;
    }

    .car-caption {
        font-size: 20px;
    }

    .about-box,
    .contact-box {
        padding: 22px;
    }
}

@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        animation: none !important;
        transition: none !important;
        scroll-behavior: auto !important;
    }
}
</style>
</head>

<body>

<!-- NAVIGATION -->

<header>
    <nav>
        <a href="#home" class="logo">YOGESH<span>.</span></a>

        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#sports-car">Sports Car</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<!-- HOME -->

<section class="hero" id="home">

    <div class="hero-text">
        <div class="tag">WELCOME TO MY PORTFOLIO</div>

        <h1>
            Hi, I'm <span class="cyan">Yogesh</span>
        </h1>

        <h2>Mechanical Engineering Student</h2>

        <p>
            I am a first-year student at Mount Zion College of Engineering.
            I love cars, gaming, technology, and learning new things.
        </p>

        <div class="buttons">
            <a href="#about" class="btn primary">Explore My World</a>
            <a href="#contact" class="btn secondary">Contact Me</a>
        </div>
    </div>

    <div class="hero-car">

        <!-- Sports car drawn using SVG; no image download required -->

        <svg class="car-art"
             viewBox="0 0 600 350"
             xmlns="http://www.w3.org/2000/svg"
             role="img"
             aria-label="Illustration of a blue neon sports car">

            <defs>
                <linearGradient id="bodyPaint" x1="0" y1="0" x2="0.8" y2="1">
                    <stop offset="0%" stop-color="#d9faff"/>
                    <stop offset="18%" stop-color="#168bff"/>
                    <stop offset="55%" stop-color="#073c91"/>
                    <stop offset="100%" stop-color="#020817"/>
                </linearGradient>

                <linearGradient id="glass" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#50eaff"/>
                    <stop offset="45%" stop-color="#10294b"/>
                    <stop offset="100%" stop-color="#030711"/>
                </linearGradient>

                <linearGradient id="road" x1="0" y1="0" x2="1" y2="0">
                    <stop offset="0%" stop-color="#061126" stop-opacity="0"/>
                    <stop offset="50%" stop-color="#00eaff" stop-opacity="0.8"/>
                    <stop offset="100%" stop-color="#061126" stop-opacity="0"/>
                </linearGradient>

                <filter id="glow">
                    <feGaussianBlur stdDeviation="5"/>
                </filter>
            </defs>

            <!-- Neon floor -->
            <ellipse cx="300" cy="285" rx="255" ry="22"
                     fill="#00bfff" opacity="0.35" filter="url(#glow)"/>

            <path d="M35 285 L565 285"
                  stroke="url(#road)" stroke-width="5"/>

            <!-- Car shadow -->
            <ellipse cx="305" cy="280" rx="225" ry="22"
                     fill="#00040c"/>

            <!-- Rear spoiler -->
            <path d="M90 207 L175 207 L186 218 L85 218 Z"
                  fill="#07101e" stroke="#00eaff" stroke-width="2"/>

            <path d="M115 208 L112 194 L130 194 L135 208"
                  fill="#101b2c" stroke="#178aff" stroke-width="2"/>

            <!-- Main car body -->
            <path d="
                M55 245
                L76 219
                L145 201
                L204 151
                Q222 135 251 132
                L349 132
                Q381 137 412 174
                L473 197
                L530 225
                L551 248
                L540 264
                L493 272
                L112 272
                L68 262 Z"
                fill="url(#bodyPaint)"
                stroke="#00eaff"
                stroke-width="2.5"/>

            <!-- Windows -->
            <path d="
                M170 198
                L222 150
                Q235 140 255 140
                L295 140
                L292 195 Z"
                fill="url(#glass)"
                stroke="#8cefff"
                stroke-width="2"/>

            <path d="
                M303 140
                L348 140
                Q372 145 400 178
                L416 197
                L302 197 Z"
                fill="url(#glass)"
                stroke="#8cefff"
                stroke-width="2"/>

            <!-- Door line -->
            <path d="M300 200 L285 256"
                  stroke="#8bdfff" stroke-width="2" opacity="0.7"/>

            <path d="M328 213 L356 213"
                  stroke="#b3f8ff" stroke-width="3"/>

            <!-- Front bumper -->
            <path d="M440 219 L508 230 L535 248
                     L513 256 L447 251 Z"
                  fill="#07101e" stroke="#137fff" stroke-width="2"/>

            <!-- Headlights -->
            <path d="M449 207 L492 222 L467 227 L439 219 Z"
                  fill="#e9ffff" stroke="#00eaff" stroke-width="2"/>

            <path d="M449 207 L492 222 L467 227 L439 219 Z"
                  fill="#00eaff" opacity="0.7" filter="url(#glow)"/>

            <!-- Front grille -->
            <path d="M466 241 L514 246 L503 255 L460 252 Z"
                  fill="#01050b" stroke="#00eaff" stroke-width="1.5"/>

            <!-- Rear light -->
            <path d="M77 224 L112 215 L107 226 L70 237 Z"
                  fill="#ff315d" stroke="#ff5279" stroke-width="2"/>

            <!-- Wheels -->
            <g>
                <circle cx="173" cy="259" r="43"
                        fill="#02040a" stroke="#111d31" stroke-width="7"/>

                <circle cx="173" cy="259" r="30"
                        fill="#18263a" stroke="#00eaff" stroke-width="3"/>

                <circle cx="173" cy="259" r="10"
                        fill="#09111e" stroke="#d9faff" stroke-width="3"/>

                <g stroke="#7beaff" stroke-width="4">
                    <path d="M173 232 L173 249"/>
                    <path d="M173 269 L173 286"/>
                    <path d="M146 259 L163 259"/>
                    <path d="M183 259 L200 259"/>
                    <path d="M154 240 L166 252"/>
                    <path d="M180 266 L192 278"/>
                    <path d="M192 240 L180 252"/>
                    <path d="M166 266 L154 278"/>
                </g>
            </g>

            <g>
                <circle cx="438" cy="259" r="43"
                        fill="#02040a" stroke="#111d31" stroke-width="7"/>

                <circle cx="438" cy="259" r="30"
                        fill="#18263a" stroke="#00eaff" stroke-width="3"/>

                <circle cx="438" cy="259" r="10"
                        fill="#09111e" stroke="#d9faff" stroke-width="3"/>

                <g stroke="#7beaff" stroke-width="4">
                    <path d="M438 232 L438 249"/>
                    <path d="M438 269 L438 286"/>
                    <path d="M411 259 L428 259"/>
                    <path d="M448 259 L465 259"/>
                    <path d="M419 240 L431 252"/>
                    <path d="M445 266 L457 278"/>
                    <path d="M457 240 L445 252"/>
                    <path d="M431 266 L419 278"/>
                </g>
            </g>

            <!-- Body highlights -->
            <path d="M92 239 L151 219 L205 209"
                  fill="none" stroke="#d8ffff" stroke-width="2"/>

            <path d="M323 207 L420 207"
                  fill="none" stroke="#5deaff" stroke-width="2"/>

            <path d="M117 270 L494 270"
                  fill="none" stroke="#00eaff" stroke-width="2"/>

            <!-- Neon accents -->
            <path d="M50 300 L200 300"
                  stroke="#00eaff" stroke-width="2" opacity="0.6"/>

            <path d="M400 300 L550 300"
                  stroke="#b34dff" stroke-width="2" opacity="0.6"/>

        </svg>

    </div>

</section>

<!-- ABOUT -->

<section class="content-section" id="about">

    <h2 class="section-title">About <span class="cyan">Me</span></h2>
    <p class="section-subtitle">GET TO KNOW ME</p>

    <div class="about-box">

        <h3>I LOVE CARS 🚗</h3>

        <p>
            Hello! My name is Yogesh. I am a first-year Mechanical
            Engineering student at Mount Zion College of Engineering.
            I enjoy cars, gaming, automobile technology, and engineering.
        </p>

        <p>
            My goal is to learn new skills, develop interesting projects,
            and become a successful engineer.
        </p>

        <div class="education">
            <p><strong>Department:</strong> Mechanical Engineering</p>
            <p><strong>Year:</strong> First Year</p>
            <p><strong>College:</strong> Mount Zion College of Engineering</p>
        </div>

    </div>

</section>

<!-- SKILLS -->

<section class="content-section alternate" id="skills">

    <div class="alternate-inner">

        <h2 class="section-title">My <span class="cyan">Skills</span></h2>
        <p class="section-subtitle">WHAT I ENJOY</p>

        <div class="grid">

            <div class="card">
                <div class="icon">🎮</div>
                <h3>Gaming</h3>
                <p>I enjoy playing games and exploring gaming worlds.</p>
            </div>

            <div class="card">
                <div class="icon">🏎️</div>
                <h3>Cars</h3>
                <p>I love sports cars and automobile technology.</p>
            </div>

            <div class="card">
                <div class="icon">⚙️</div>
                <h3>Engineering</h3>
                <p>I am learning mechanical systems and engineering concepts.</p>
            </div>

        </div>

    </div>

</section>

<!-- SPORTS CAR -->

<section class="content-section" id="sports-car">

    <h2 class="section-title">
        My Dream <span class="cyan">Sports Car</span>
    </h2>

    <p class="section-subtitle">SPEED • POWER • PERFORMANCE</p>

    <div class="sports-box">

        <!-- Reuse the same local SVG car illustration -->
        <svg class="car-art"
             viewBox="0 0 600 350"
             xmlns="http://www.w3.org/2000/svg"
             role="img"
             aria-label="Blue neon sports car">

            <defs>
                <linearGradient id="paint2" x1="0" y1="0" x2="0.8" y2="1">
                    <stop offset="0%" stop-color="#d9faff"/>
                    <stop offset="25%" stop-color="#168bff"/>
                    <stop offset="70%" stop-color="#073c91"/>
                    <stop offset="100%" stop-color="#020817"/>
                </linearGradient>

                <linearGradient id="glass2" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#50eaff"/>
                    <stop offset="50%" stop-color="#10294b"/>
                    <stop offset="100%" stop-color="#030711"/>
                </linearGradient>
            </defs>

            <ellipse cx="300" cy="285" rx="250" ry="20"
                     fill="#00eaff" opacity="0.2"/>

            <path d="M55 245 L76 219 L145 201 L204 151
                     Q222 135 251 132 L349 132
                     Q381 137 412 174 L473 197 L530 225
                     L551 248 L540 264 L493 272 L112 272 L68 262 Z"
                  fill="url(#paint2)" stroke="#00eaff" stroke-width="3"/>

            <path d="M170 198 L222 150 Q235 140 255 140
                     L295 140 L292 195 Z"
                  fill="url(#glass2)" stroke="#8cefff" stroke-width="2"/>

            <path d="M303 140 L348 140 Q372 145 400 178
                     L416 197 L302 197 Z"
                  fill="url(#glass2)" stroke="#8cefff" stroke-width="2"/>

            <path d="M300 200 L285 256"
                  stroke="#8bdfff" stroke-width="2"/>

            <path d="M449 207 L492 222 L467 227 L439 219 Z"
                  fill="#e9ffff" stroke="#00eaff" stroke-width="3"/>

            <path d="M466 241 L514 246 L503 255 L460 252 Z"
                  fill="#01050b" stroke="#00eaff" stroke-width="2"/>

            <path d="M77 224 L112 215 L107 226 L70 237 Z"
                  fill="#ff315d"/>

            <g fill="#02040a" stroke="#00eaff" stroke-width="5">
                <circle cx="173" cy="259" r="40"/>
                <circle cx="438" cy="259" r="40"/>
            </g>

            <g fill="#18263a" stroke="#b8f5ff" stroke-width="3">
                <circle cx="173" cy="259" r="23"/>
                <circle cx="438" cy="259" r="23"/>
            </g>

            <g stroke="#00eaff" stroke-width="4">
                <path d="M173 239 V279 M153 259 H193
                         M159 245 L187 273 M187 245 L159 273"/>

                <path d="M438 239 V279 M418 259 H458
                         M424 245 L452 273 M452 245 L424 273"/>
            </g>

            <path d="M92 239 L151 219 L205 209"
                  fill="none" stroke="#d8ffff" stroke-width="2"/>

            <path d="M323 207 L420 207"
                  fill="none" stroke="#5deaff" stroke-width="2"/>

            <path d="M117 270 L494 270"
                  fill="none" stroke="#00eaff" stroke-width="2"/>

        </svg>

        <h3 class="car-caption">NEON SPORTS CAR</h3>

        <p class="car-description">
            My dream sports car represents my passion for automobile
            design, mechanical engineering, speed, and innovation.
            I want to learn how powerful vehicles are designed and built.
        </p>

        <div class="car-specs">

            <div class="spec">
                <strong>DESIGN</strong>
                Aerodynamic
            </div>

            <div class="spec">
                <strong>STYLE</strong>
                Sporty
            </div>

            <div class="spec">
                <strong>PASSION</strong>
                Automobiles
            </div>

        </div>

    </div>

</section>

<!-- PROJECTS -->

<section class="content-section alternate" id="projects">

    <div class="alternate-inner">

        <h2 class="section-title">My <span class="cyan">Projects</span></h2>
        <p class="section-subtitle">MY LEARNING JOURNEY</p>

        <div class="grid">

            <div class="card">
                <div class="icon">💻</div>
                <h3>Portfolio Website</h3>
                <p>A personal website made using HTML and CSS.</p>
            </div>

            <div class="card">
                <div class="icon">🚘</div>
                <h3>Automobile Learning</h3>
                <p>Exploring car components and mechanical systems.</p>
            </div>

            <div class="card">
                <div class="icon">💡</div>
                <h3>Future Projects</h3>
                <p>A place to showcase projects as I develop my skills.</p>
            </div>

        </div>

    </div>

</section>

<!-- CONTACT -->

<section class="content-section" id="contact">

    <h2 class="section-title">Contact <span class="cyan">Me</span></h2>
    <p class="section-subtitle">LET'S CONNECT</p>

    <div class="contact-box">

        <h3>Thanks for visiting my portfolio!</h3>

        <p>
            Feel free to contact me about cars, gaming,
            mechanical engineering, and projects.
        </p>

        <a href="mailto:yourname@example.com" class="btn primary">
            Send Me an Email
        </a>

    </div>

</section>

<!-- FOOTER -->

<footer>
    <p>Designed by <span>Yogesh</span> | © 2026 All Rights Reserved</p>
</footer>

</body>
</html>
```
