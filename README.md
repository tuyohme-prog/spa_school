<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Spabafet School</title>
  <style>
    * {margin: 0; padding: 0; box-sizing: border-box;}

    body {
      font-family: Arial, sans-serif;
      background-color: black;
      color: white;
    }

    /* Header */
    #school_header{
      color: yellowgreen;
      border: 6px solid green;
      border-bottom-left-radius: 30px;
      border-top-right-radius: 30px;
      padding: 10px 20px;
      width: fit-content;
      margin: 20px auto;
      text-align: center;
    }

    /* Navigation */
    nav {
      background: #111;
      padding: 10px 0;
    }

    .nav-bar {
      display: flex;
      justify-content: center;
      list-style: none;
      gap: 30px;
      flex-wrap: wrap;
    }

    .nav-bar li {
      position: relative;
      cursor: pointer;
      text-transform: uppercase;
    }

    .nav-bar a {
      text-decoration: none;
      color: white;
      padding: 8px 12px;
      display: block;
      transition: background 0.3s;
    }

    .nav-bar a:hover {
      background: green;
      border-radius: 5px;
    }

    /* Dropdown */
    .dropdown {
      display: none;
      position: absolute;
      top: 100%;
      left: 0;
      background: #222;
      min-width: 220px;
      list-style: none;
      border-radius: 5px;
      z-index: 1000;
    }

    .dropdown li a {
      padding: 10px;
      color: white;
    }

    .dropdown li a:hover {
      background: yellowgreen;
      color: black;
    }

    /* Active dropdown */
    li.active > .dropdown {
      display: block;
    }

    /* Nested dropdowns should open to the right */
    .dropdown .dropdown {
      top: 0;
      left: 100%;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .nav-bar {
        flex-direction: column;
        align-items: center;
        gap: 15px;
      }

      .dropdown {
        position: static;
        min-width: 100%;
      }

      .dropdown .dropdown {
        position: static;
      }
      background: #111;
      padding: 15px;
      text-align: center;
    }

    #welcome_header{
      color: yellowgreen;
      width: fit-content;
      margin: auto;
      padding: 10px 20px;
    }

    nav {
      background: green;
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 12px;
      flex-wrap: wrap;
      position:sticky;
      top:0px;
    }

    nav a {
      color: white;
      text-decoration: none;
      text-transform: uppercase;
      font-weight: bold;
      padding: 6px 12px;
      transition: 0.3s;
    }

    nav a:hover {
      background: yellowgreen;
      color: black;
      border-radius: 6px;
    }

    .hero {
      text-align: center;
      padding: 50px 20px;
      background: url("images/school_bg.jpg") center/cover no-repeat;
      background-attachment: fixed;
      color: white;
    }

    .hero h2 {
      font-size: 2rem;
      margin-bottom: 15px;
      color: yellowgreen;
      text-shadow: 2px 2px 8px black;
    }

    .content {
      max-width: 1000px;
      margin: auto;
      padding: 30px 20px;
    }

    h2 {
      color: yellowgreen;
      border-bottom: 2px solid green;
      padding-bottom: 5px;
      margin-top: 30px;
    }

    ul {
      margin: 10px 0 20px 20px;
    }

    footer {
      background: #111;
      text-align: center;
      padding: 15px;
      margin-top: 40px;
      font-size: 14px;
      color: #aaa;
    }

    .cta {
      text-align: center;
      margin: 30px 0;
    }

    .cta a {
      background: yellowgreen;
      color: black;
      text-decoration: none;
      padding: 12px 25px;
      border-radius: 8px;
      font-weight: bold;
      transition: 0.3s;
    }

    .cta a:hover {
      background: green;
      color: white;
    }
  </style>
</head>
<body>
  <h1 id="school_header">Spabafet School</h1>

  <nav>
    <ul class="nav-bar">
      <li><a href="spabafet_school.html">Home</a></li>

      <!-- Administration -->
      <li>
        <a href="administration_page.html">Administration</a>
      </li>

      <!-- Academics -->
      <li>
        <a href="#">Academics ▾</a>
        <ul class="dropdown">
          <li>
            <a href="#">College ▸</a>
            <ul class="dropdown">
              <li><a href="#">School of Science (Medicine)</a></li>
              <li><a href="#">School of Science (Environmental Studies)</a></li>
              <li><a href="#">School of Technology (Computer Science)</a></li>
              <li><a href="#">School of Science (Applied Science)</a></li>
              <li><a href="#">School of Engineering (Electrical & Electronics)</a></li>
            </ul>
          </li>
          <li>
            <a href="#">High School ▸</a>
            <ul class="dropdown">
              <li>
                <a href="#">Junior Secondary School (JSS)</a>
                <ul class="dropdown">
                  <li><a href="#">JSS1</a></li>
                  <li><a href="#">JSS2</a></li>
                  <li><a href="#">JSS3</a></li>
                </ul>
              </li>
              <li>
                <a href="#">Senior Secondary School (SSS)</a>
                <ul class="dropdown">
                  <li><a href="#">SS1</a></li>
                  <li><a href="#">SS2</a></li>
                  <li><a href="#">SS3</a></li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </li>

      <!-- Portals -->
      <li>
        <a href="login.html">Portals ▾</a>
        <ul class="dropdown">
          <li><a href="portal_log_in.html" target="blank">Students Portal</a></li>
          <li><a href="portal_log_in.html" target="blank">Staff Portal</a></li>
        </ul>
      </li>

      <!-- Services -->
      <li>
        <a href="#">Services ▾</a>
        <ul class="dropdown">
          <li><a href="school_helpdesk.html">ICT Team (Help Desk)</a></li>
          <li><a href="school_court_portal.html">Students Court</a></li>
        </ul>
      </li>

      <!-- Resources -->
      <li>
        <a href="#">Resources ▾</a>
        <ul class="dropdown">
          <li><a href="combined.html">Results & Transcripts</a></li>
          <li><a href="combined.html">Fee Structures</a></li>
          <li><a href="combined.html">Students Organizations</a></li>
          <li><a href="combined.html">pay school fees</a></li>
        </ul>
      </li>



      <!-- Gallery -->
      <li><a href="school_gallary.html">School Gallery</a></li>

      <!-- About -->
      <li><a href="about_page.html">About</a></li>
    </ul>
      </nav>
      <br>
    
    <h1 id="welcome_header">Welcome to Spabafet School</h1>
  <div class="hero">
    <h2>Shaping Bright Futures Together</h2>
    <p>Where curiosity, creativity, and leadership are nurtured.</p>
  </div>

  <div class="content">
    <h2>Why Choose Us?</h2>
    <ul>
      <li><strong>Quality Education</strong> – A well-rounded curriculum balancing academics, skills, and character development.</li>
      <li><strong>Dedicated Teachers</strong> – Passionate educators committed to guiding students every step of the way.</li>
      <li><strong>Modern Learning</strong> – Blending technology with innovative teaching methods.</li>
      <li><strong>Holistic Growth</strong> – Opportunities in sports, arts, leadership, and community service.</li>
    </ul>

    <h2>Our Vision</h2>
    <p>To create lifelong learners who are responsible, innovative, and compassionate leaders of tomorrow.</p>

    <h2>Our Mission</h2>
    <p>To provide a safe, inclusive, and supportive learning environment where every student can thrive.</p>

    <div class="cta">
      <a href="portal_log_in.html">Explore Student Portals</a>
    </div>
  </div>

  <footer>
    &copy; 2025 Spabafet School. All rights reserved.
  </footer>

  <script>
    // Toggle dropdowns on click (including nested ones)
    document.querySelectorAll('.nav-bar li > a').forEach(link => {
      link.addEventListener('click', function(e) {
        const parentLi = this.parentElement;
        const dropdown = parentLi.querySelector('.dropdown');

        if (dropdown) {
          e.preventDefault(); // stop navigation if it has submenu
          parentLi.classList.toggle('active');

          // Close siblings
          const siblings = parentLi.parentElement.querySelectorAll('li');
          siblings.forEach(sib => {
            if (sib !== parentLi) sib.classList.remove('active');
          });
        }
      });
    });
  </script>
</body>
</html>
