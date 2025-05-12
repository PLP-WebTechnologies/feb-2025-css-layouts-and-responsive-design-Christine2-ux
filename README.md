index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Responsive CSS Layout</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">MySite</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">
    <section class="main-content">
      <h1>Welcome to My Responsive Page</h1>
      <p>This is the main content area. Resize your browser to see how it responds!</p>
    </section>
    <aside class="sidebar">
      <h2>Sidebar</h2>
      <p>This is a sidebar section for extra content.</p>
    </aside>
  </main>

  <footer class="footer">
    <p>&copy; 2025 MySite. All rights reserved.</p>
  </footer>
</body>
</html>
style.css
 {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #0077cc;
  color: #fff;
  padding: 1rem;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.nav-links li a {
  color: white;
  text-decoration: none;
}

.container {
  display: grid;
  grid-template-columns: 3fr 1fr;
  gap: 1rem;
  padding: 1rem;
}

.main-content, .sidebar {
  background-color: #f0f0f0;
  padding: 1rem;
  border-radius: 8px;
}

.footer {
  text-align: center;
  padding: 1rem;
  background-color: #0077cc;
  color: white;
  margin-top: 1rem;
}

@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
  }

  .nav-links {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.5rem;
  }
}

@media (max-width: 480px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .logo {
    margin-bottom: 0.5rem;
  }
}

