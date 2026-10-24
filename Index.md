HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aperture & Co. — Photography Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Outer Master Grid Container (Named Grid Areas) -->
    <div class="portfolio-grid">

        <!-- 1 & 3. Header Section (Named Grid Area) -->
        <header class="header">
            <div class="logo">Aperture & Co.</div>
            <nav class="nav-links">
                <a href="#gallery">Gallery</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </nav>
        </header>

        <!-- Hero Intro Banner (Named Grid Area) -->
        <section class="hero">
            <div class="hero-content">
                <h1>Capturing Moments, Creating Stories</h1>
                <p>An exquisite collection of landscape, architectural, and fine-art photography.</p>
            </div>
        </section>

        <!-- 2, 4 & 5. Main Grid Layout & Multiple Cards (Named Grid Area) -->
        <main id="gallery" class="main-gallery">
            <div class="gallery-container">

                <!-- Card 1 -->
                <article class="gallery-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?auto=format&fit=crop&w=600&q=80" alt="Misty Pine Forest">
                    </div>
                    <div class="card-info">
                        <h3>Misty Pine Forest</h3>
                        <span class="category">Landscape</span>
                    </div>
                </article>

                <!-- Card 2 -->
                <article class="gallery-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=600&q=80" alt="Yosemite Valley Stream">
                    </div>
                    <div class="card-info">
                        <h3>Yosemite Valley Stream</h3>
                        <span class="category">Nature</span>
                    </div>
                </article>

                <!-- Card 3 -->
                <article class="gallery-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=600&q=80" alt="Modern Architecture">
                    </div>
                    <div class="card-info">
                        <h3>Urban Geometry</h3>
                        <span class="category">Architecture</span>
                    </div>
                </article>

                <!-- Card 4 -->
                <article class="gallery-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1426604966848-d7adac902bff?auto=format&fit=crop&w=600&q=80" alt="Snowy Mountain Peaks">
                    </div>
                    <div class="card-info">
                        <h3>Alps Winter Summit</h3>
                        <span class="category">Mountain</span>
                    </div>
                </article>

                <!-- Card 5 -->
                <article class="gallery-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=600&q=80" alt="Sunset Lake Reflection">
                    </div>
                    <div class="card-info">
                        <h3>Mirror Lake Sunset</h3>
                        <span class="category">Waterscape</span>
                    </div>
                </article>

                <!-- Card 6 -->
                <article class="gallery-card">
                    <div class="image-wrapper">
                        <img src="https://images.unsplash.com/photo-1519681393784-d120267933ba?auto=format&fit=crop&w=600&q=80" alt="Starry Night Sky">
                    </div>
                    <div class="card-info">
                        <h3>Galaxy Over Ridge</h3>
                        <span class="category">Astro</span>
                    </div>
                </article>

            </div>
        </main>

        <!-- Footer Section (Named Grid Area) -->
        <footer class="footer">
            <p>&copy; 2026 Aperture & Co. Photography. All rights reserved. Built with CSS Grid.</p>
        </footer>

    </div>

</body>
</html>


CSS
/* ==========================================
   Global Resets & Typography
   ========================================== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #0f172a;
    color: #f8fafc;
    line-height: 1.6;
}

/* ==========================================================
   1 & 3. Master Grid Layout & Named Grid Areas
   ========================================================== */
.portfolio-grid {
    display: grid; /* 1. Primary Layout using CSS Grid */
    
    /* 3. Named grid areas structure */
    grid-template-areas: 
        "header"
        "hero"
        "main"
        "footer";
    
    grid-template-columns: 1fr;
    grid-template-rows: auto auto 1fr auto;
    min-height: 100vh;
}

/* ==========================================================
   Header Styling
   ========================================================== */
.header {
    grid-area: header;
    background-color: rgba(15, 23, 42, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid #1e293b;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 5%;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 1.25rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    color: #ffffff;
}

.nav-links {
    display: flex;
    gap: 2rem;
}

.nav-links a {
    text-decoration: none;
    color: #94a3b8;
    font-weight: 500;
    font-size: 0.95rem;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: #ffffff;
}

/* ==========================================================
   Hero Intro Section
   ========================================================== */
.hero {
    grid-area: hero;
    padding: 5rem 5% 3rem 5%;
    text-align: center;
}

.hero-content {
    max-width: 700px;
    margin: 0 auto;
}

.hero h1 {
    font-size: 2.75rem;
    font-weight: 800;
    color: #ffffff;
    margin-bottom: 1rem;
    letter-spacing: -0.02em;
}

.hero p {
    color: #94a3b8;
    font-size: 1.15rem;
}

/* ==========================================================
   2 & 5. Main Gallery Grid (`repeat`, `minmax`, `fr`, `gap`)
   ========================================================== */
.main-gallery {
    grid-area: main;
    padding: 2rem 5% 5% 5%;
}

.gallery-container {
    display: grid; /* Inner Sub-Grid for Gallery Cards */
    
    /* 
      2. Grid track sizing using repeat(), auto-fit, minmax(), and fr units:
      - Automatically fits columns with a minimum width of 300px and 1fr fraction 
        to stretch evenly across available viewport space.
    */
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    
    /* Consistent gaps between cards */
    gap: 2rem;
    
    max-width: 1400px;
    margin: 0 auto;
}

/* ==========================================================
   Gallery Card & 4. Overflow Prevention
   ========================================================== */
.gallery-card {
    background-color: #1e293b;
    border: 1px solid #334155;
    border-radius: 12px;
    overflow: hidden; /* 4. Prevents text/image overflow outside the card bounds */
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    display: flex;
    flex-direction: column;
}

.gallery-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 12px 20px -5px rgba(0, 0, 0, 0.3);
}

.image-wrapper {
    width: 100%;
    height: 240px;
    overflow: hidden; /* 4. Clips zoomed image hover expansion */
    background-color: #0f172a;
}

.gallery-card img {
    width: 100%;
    height: 100%;
    object-fit: cover; /* 4. Ensures photos scale proportionally without distortion */
    display: block;
    transition: transform 0.4s ease;
}

.gallery-card:hover img {
    transform: scale(1.06);
}

.card-info {
    padding: 1.25rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.card-info h3 {
    font-size: 1.05rem;
    font-weight: 600;
    color: #ffffff;
    /* 4. Text overflow handling */
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.category {
    font-size: 0.75rem;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    background-color: #334155;
    color: #93c5fd;
    padding: 0.25rem 0.6rem;
    border-radius: 20px;
    font-weight: 600;
}

/* ==========================================================
   Footer Section
   ========================================================== */
.footer {
    grid-area: footer;
    background-color: #0b1120;
    border-top: 1px solid #1e293b;
    padding: 2.5rem 5%;
    text-align: center;
    color: #64748b;
    font-size: 0.9rem;
}

/* ==========================================================
   5. Testing & Responsiveness Across Screen Widths
   ========================================================== */
@media (max-width: 768px) {
    .hero h1 {
        font-size: 2rem;
    }

    .header {
        flex-direction: column;
        gap: 1rem;
        padding: 1rem;
    }

    .nav-links {
        gap: 1.25rem;
    }
}