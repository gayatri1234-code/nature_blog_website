# nature_blog_website

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Blog</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar">
        <div class="container">
            <h1 class="logo">My Blog</h1>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#blog">Blog</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="hero">
        <div class="hero-content">
            <h2>Welcome to My Blog</h2>
            <p>Sharing insights, stories, and tutorials.</p>
        </div>
    </header>

    <!-- Blog Posts -->
    <section id="blog" class="blog-section">
        <div class="container">
            <h2>Latest Posts</h2>
            <div class="blog-posts">
                <!-- Blog Post Example -->
                <article class="post">
                    <img src="https://files.worldwildlife.org/wwfcmsprod/images/Capture_Wildlife_Images_tavel_blog/blog_show/7ib2pykbzi_10_ways_to_capture.JPG" alt="Post Image">
                    <h3>Post Title</h3>
                    <p class="date">Published on July 23, 2023</p>
                    <p class="summary">Capturing beautiful wildlife images on your travels requires both patience and preparation. This photo, from the World Wildlife Fund, highlights the importance of respecting wildlife, understanding natural lighting, and blending into the environment to capture animals in their natural behavior. Techniques like using a telephoto lens, practicing with moving subjects, and researching the habitat are key for beginners and pros alike. Whether you're in a forest, savannah, or coral reef, these tips can help bring your photos to life and deepen your connection to nature.</p>
                    <a href="#" class="read-more">Read More</a>
                </article>
                <!-- Repeat <article> for more posts -->
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2024 My Blog. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

# style.css

/* Reset basic styling */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

/* Navbar Styling */
.navbar {
    background-color: #333;
    padding: 1em;
}

.navbar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.navbar .logo {
    color: #fff;
    font-size: 1.5em;
}

.navbar .nav-links {
    list-style: none;
    display: flex;
}

.navbar .nav-links li {
    margin-left: 20px;
}

.navbar .nav-links a {
    color: #fff;
    text-decoration: none;
}

.hero {
    background: url('https://avatars.mds.yandex.net/get-pdb/1088712/8b19d278-0b9b-46f8-89e4-66f5541efc55/s1200?webp=false') no-repeat center center/cover;
    height: 50vh;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.hero-content h2 {
    font-size: 2.5em;
}

.hero-content p {
    font-size: 1.2em;
}

.blog-section {
    padding: 2em 0;
    background-color: #f4f4f4;
}

.blog-section .container {
    max-width: 1200px;
    margin: 0 auto;
}

.blog-section h2 {
    text-align: center;
    margin-bottom: 1.5em;
}

.blog-posts {
    display: flex;
    flex-wrap: wrap;
    gap: 2em;
    justify-content: center;
}

.post {
    background-color: #fff;
    padding: 1em;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    text-align: center;
    transition: transform 0.3s ease;
}

.post img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
}

.post h3 {
    margin: 1em 0 0.5em;
}

.post .date {
    font-size: 0.9em;
    color: #555;
}

.post .summary {
    margin: 0.5em 0;
}

.post .read-more {
    color: #333;
    font-weight: bold;
    text-decoration: none;
    border: 1px solid #333;
    padding: 0.5em 1em;
    border-radius: 5px;
    transition: background-color 0.3s ease, color 0.3s ease;
}

.post:hover {
    transform: translateY(-5px);
}

.post .read-more:hover {
    background-color: #333;
    color: #fff;
}

/* Footer Styling */
.footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1em;
}

/* Responsive Styling */
@media (max-width: 768px) {
    .nav-links {
        flex-direction: column;
    }

    .hero {
        height: 30vh;
    }

    .blog-posts {
        flex-direction: column;
        align-items: center;
    }
}



# script.js
// Smooth scrolling for navigation links
document.querySelectorAll('.nav-links a').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});

