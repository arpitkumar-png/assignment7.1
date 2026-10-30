HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.1 — Responsive Navigation Bar</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="nav-style.css">
</head>
<body>

    <!-- Header & Navigation Bar -->
    <header class="site-header">
        <nav class="navbar">
            <!-- 1. Logo -->
            <div class="nav-logo">
                <a href="#">TechClub</a>
            </div>

            <!-- 1. Navigation Links & CTA Button -->
            <ul class="nav-links">
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="registration.html">Register</a></li>
                <li><a href="contact.html" class="nav-btn">Join Us</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content Placeholder -->
    <main class="main-content">
        <section class="hero-section">
            <h1>Responsive Flexbox Navigation</h1>
            <p>Resize your browser window to test how the Flexbox container adapts spacing and alignment dynamically.</p>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 TechClub. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: nav-style.css
CSS
/* --- Global Reset --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    line-height: 1.6;
}

/* --- Site Header Styling --- */
.site-header {
    background-color: #0f172a;
    color: #ffffff;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    position: sticky;
    top: 0;
    z-index: 1000;
}

/* --- 2, 3, 4. Flexbox Navbar Layout --- */
.navbar {
    max-width: 1100px;
    margin: 0 auto;
    padding: 1rem 2rem;
    display: flex;                    /* 2. Apply display: flex */
    justify-content: space-between;   /* 3. Space out logo and links */
    align-items: center;              /* 4. Vertically center items */
    flex-wrap: wrap;                  /* Ensures wrapping on smaller screens */
    gap: 1rem;
}

/* --- Logo Styling --- */
.nav-logo a {
    font-size: 1.5rem;
    font-weight: 700;
    color: #38bdf8;
    text-decoration: none;
    letter-spacing: 0.02em;
}

/* --- Navigation Links List --- */
.nav-links {
    list-style: none;
    display: flex;                    /* Flex container for list items */
    align-items: center;              /* Vertically align items */
    gap: 1.5rem;                      /* Spacing between list items */
}

.nav-links a {
    color: #cbd5e1;
    text-decoration: none;
    font-size: 0.95rem;
    font-weight: 500;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: #ffffff;
}

/* --- 5. Styled Navigation Button --- */
.nav-btn {
    background-color: #2563eb;
    color: #ffffff !important;
    padding: 0.5rem 1.25rem;
    border-radius: 6px;
    font-weight: 600;
    transition: background-color 0.2s ease;
}

.nav-btn:hover {
    background-color: #1d4ed8;
}

/* --- Hero Section Styling --- */
.main-content {
    max-width: 900px;
    margin: 4rem auto;
    padding: 0 1.5rem;
    text-align: center;
}

.hero-section h1 {
    font-size: 2.5rem;
    color: #1e293b;
    margin-bottom: 1rem;
}

.hero-section p {
    color: #64748b;
    font-size: 1.1rem;
}

/* --- Footer --- */
footer {
    text-align: center;
    padding: 2rem;
    background-color: #0f172a;
    color: #94a3b8;
    font-size: 0.9rem;
    margin-top: 5rem;
}