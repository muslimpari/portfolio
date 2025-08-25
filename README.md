<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manahil Aamir - Full Stack Developer</title>
    <link rel="stylesheet" href="style.css">
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.12/typed.min.js"></script>
</head>
<body>

    <!-- Header -->
    <header class="header">
        <div class="profile-header">
            <img src="muslim-woman.png" alt="Profile Picture" class="small-profile-pic">
            <h1 color="#ef49e1">Portfolio</h1>
        </div>
        <nav>
            <ul class="nav-links">
                <li><a href="#" onclick="showSection('home')" >Home</a></li>
                <li><a href="#" onclick="showSection('about')">About</a></li>
                <li><a href="#" onclick="showSection('services')">Services</a></li>
                <li><a href="#" onclick="showSection('contact')">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="section">
        <div class="home-container">
            <div class="home-left">
                <span id="typing"></span>
            </div>
            <div class="home-center">
                <img src="Mypic.jpg" alt="Profile Image" class="home-profile-pic">
            </div>
            <div class="home-right">
                <div class="content-box" onclick="showText('home-content')">
                    <div class="social-icons">
                    <a href="https://www.twitter.com"><i class='bx bxl-twitter'></i></a>
                    <a href="https://www.facebook.com"><i class='bx bxl-facebook-circle' ></i></a>
                    <a href="https://www.youtube.com"><i class='bx bxl-instagram-alt' ></i></a>
                    <a href="https://www.twitter.com"><i class='bx bxl-youtube' ></i></a>
                    <a href="https://github.com"><i class='bx bxl-github' ></i></a> 
                </div>
                    <h2>Hi, I'm Manahil Aamir</h2>
                    <p class="home-content">I am a Web Developer and Full Stack Developer.</p>
                    <button class="hire-btn">Hire Me</button>
                    
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section" style="display: none;">
        <div class="about-container">
            <div class="about-left">
                <div class="about-box" onclick="showText('about-content')">
                    <h1>About Me! </h1>
                    <h2>I'm<span class="name-highlight"> Manahil</span></h2>
                    <p class="about-content">A passionate Full Stack Developer with expertise in building interactive and user-friendly web applications.</p>
                    <p class="about-content">I love solving problems, creating innovative digital solutions, and bringing ideas to life.</p>
                    <p> I'm drive for innovation. I specialize in both front-end and back-end development</p>
                </div>
            </div>
            <div class="about-right">
                <img src="Mypic.jpg" alt="Manahil Aamir" class="glowing-pic">
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section" style="display: none;">
      
        <div class="services-container">
            <h2>My Services</h2>
            <div class="service-box">
                
                <img src="web developer.jpg" alt="Web-dev">
                <h3>Web Developer</h3>
                <p>Building interactive and user-friendly websites.</p>
            </div>
            <div class="service-box">
                <img src="web dev-icon.jpg" alt="Web-dev">
                <h3>Backend Developer</h3>
                <p>Creating powerful server-side applications.</p>
            </div>
            <div class="service-box">
                <img src="UI UX Design .jpg" alt="Web-dev">
                <h3>UI/UX Designer</h3>
                <p>Designing seamless user experiences.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact-container" style="display:none">
        <h2>Contact Me</h2>
        <p>Email:minahilamir2012@gmail.com</p>
        <p>Phoneno:03440052796</p>
        <p>Pls fill out the form</p>
        
        <form id="contact-form">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
        
        <div id="success-message" style="display: none;">
            <p>Message sent successfully! I'll get back to you soon.</p>
        </div>
    </section>

    <script>
        var typed = new Typed("#typing", {
            strings: ["I am a Creative Coder", "Web Developer", "Full Stack Developer"],
            typeSpeed: 50,
            backSpeed: 50,
            loop: true
        });
        function showText(contentId) {
    var content = document.getElementById(contentId);
    
    if (content.classList.contains('show-content')) {
        content.classList.remove('show-content'); 
        setTimeout(() => { content.style.display = 'none'; }, 500); // Thoda delay rakho
    } else {
        content.style.display = 'block';  
        setTimeout(() => { content.classList.add('show-content'); }, 10); // Smooth transition ke liye delay
    }
}


     function showSection(section) {
    // Hide all sections
    document.querySelectorAll('.section').forEach(sec => sec.style.display = 'none');

    // Show the clicked section
    document.getElementById(section).style.display = 'block';

    // Remove active class from all links
    document.querySelectorAll('.nav-links a').forEach(link => link.classList.remove('active'));

    // Add active class to the clicked link
    var activeLink = document.querySelector(`.nav-links a[href="#${section}"]`);
    activeLink.classList.add('active');
}
   
    </script>
   #style.css
   /* Global Styles */
body {
    font-family: 'Poppins', sans-serif;
    margin: 0;
    padding: 0;
    background: linear-gradient(to right, #068D9D, #53599A, #6D9DC5);
    color: rgb(248, 254, 254);
}

/* Header */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 40px;
    padding-left: 5px;
    background: rgba(0, 0, 0, 0.3);
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 100;
}


/* Profile Heading */
.profile-header {
    display: flex;
    align-items: center;
    gap: 10px;
}

.profile-header h1 {
    margin: 0;
    padding-left: 10px;
}

/* Small Profile Pic in Header */
.small-profile-pic {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    border: 2px solid white;
    box-shadow: 0 0 10px #ef49e1;
    text-decoration: none;
    transition: 0.3s ease-in-out;
}
.small-profile-pic :hover{
    color:#FFDD57
}

/* Navigation */
.nav-links {
    list-style: none;
    display: flex;
    gap: 70px;
    padding-left: 5px;
    nav-left: 30px;
}

.nav-links a {
    text-decoration: none;
    color: rgb(255, 255, 255);
    font-size: 1.2rem;
    padding: 10px 20px;
    border-radius: 5px;
   
}
.nav-links a:hover {
    color: #f388f7; /* Purple color on hover */
}
.nav-links a:active, 
.nav-links a.active {
    color: #f388f7; /* Purple color */
    font-weight: bold;
    background: none; /* Removes yellow highlight */
}
.nav-links a.active {
    color: #FF6347;  /* Aap chahein toh koi bhi color set kar sakte hain */
    font-weight: bold;
}



/* Home Page */
.home-container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    gap: 50px;
}

/* Animated Text */
#typing {
    font-size: 1.8rem;
    font-weight: bold;
    animation: fadeIn 2s infinite alternate;
}

/* Center Profile Image */
.home-center .home-profile-pic {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 3px solid white;
    box-shadow: 0 0 15px #FFDD57;
    animation: glowingCircle 2s infinite alternate;
}

/* Right Content Box */
.home-right .content-box {
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: 10px;
    box-shadow: 0 0 10px #068D9D;
    animation: glowing 1.5s infinite alternate;
    max-width: 400px;
    cursor: pointer;
}

/* Button */
.hire-btn {
    margin-top: 20px;
    padding: 12px 25px;
    align-items: center;
    background-color: #068D9D;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1.2rem;
    transition: 0.3s ease-in-out;
    box-shadow: 0 0 10px #84c3f0e9;
    animation: glowing 1.5s infinite alternate;
}

.hire-btn:hover {
    background-color: #53599A;
    box-shadow: 0 0 20px #ebba0c;
}
.social-icons  {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-top: 20px;
}
i.bx {
    color: #FFDD57;
    border-radius: 50%;
    border:2px solid #ef49e1;
    background:transparent;
    font-size: 30px;
    box-shadow: 0 0 10px #ef49e1;
    text-decoration: none;
    transition: 0.3s ease-in-out;

}
i.bx:hover{
    box-shadow: 0 0 20px #FFDD57;
}


.social-icon a svg {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background:transparent;
    border:2px solid #ef49e1;
    border-radius: 50%;
    font-size: 20px;
    color:#ef49e1;
    background-size: cover;
    box-shadow: 0 0 10px #ef49e1;
    text-decoration: none;
    transition: 0.3s ease-in-out;
}

.social-icon:hover svg {
    transform: scale(1.1);
    box-shadow: 0 0 20px #FFDD57;
}


/* About Page */
.about-container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    gap: 50px;
}
.about-container h1{
    margin-top:50px;
    display:flex;
    justify-content: center;
    align-items:center;
    color:#ef49e1;

}
.about-container h2{
    
    color:#ffffff;

}
.name-highlight {
    color: #ef49e1; /* Manahil ka color change kar diya (Customize as needed) */
}

.about-left .about-box {
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: 10px;
    box-shadow: 0 0 10px #068D9D;
    animation: glowing 1.5s infinite alternate;
    max-width: 400px;
    cursor: pointer;
}
.about-container h1{
    color:#ef49e1;
}
/* Content Animation (Text inside box) */

/* About Page Image */
.about-right .glowing-pic {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 3px solid white;
    box-shadow: 0 0 15px #FFDD57;
    animation: glowingCircle 2s infinite alternate;
}

/* Content Animation (Text inside box) */
.show-content {
    animation: fadeInContent 1.5s ease-in-out;
    color:#ef49e1
}
.services-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-top: 150px;
    margin-bottom: 200px;
    gap: 80px; /* Add 10px spacing between the boxes */
    flex-wrap: wrap; /* Allow boxes to wrap to the next line if needed */
    padding: 10px;
}
.services-container h2{
  display:flex;
  flex-direction: column; /* Ensures elements stack vertically */
  align-items: center;
  margin-bottom: 20px;
  text-align: center;
  margin-inline-start: 20px;
  font-size: 50px;


}
.service-box {
    display: flex;
    justify-content: center;
    padding-top: 8px; /* Centers boxes horizontally */
    gap: 80px; /* Space between boxes */
    flex-wrap: wrap; /* Allows wrapping if needed */
    width: 100%;
    background-color: rgba(30, 215, 202, 0.5);
    border-radius: 30px;
    box-shadow: 0 0 15px #FFDD57;
    text-align: center;
    cursor: pointer;
    transition: 0.3s ease-in-out;
    animation: glowing 1.5s infinite alternate;
}
.service-box img {
    width: 100px; /* Adjust size as needed */
    height: 100px;
    border-radius: 50%; /* Makes image circular */
    box-shadow: 0 0 15px #ef49e1;
    cursor: pointer;
    transition: 0.3s ease-in-out;
    animation: glowing 1.5s infinite alternate;
    object-fit: cover;
}


.service-box h3 {
    font-size: 1.8rem;
    margin-bottom: 15px;
    color:#fff7fe
}

.service-box p {
    font-size: 1.2rem;
    color: rgb(150, 20, 120);
}

/* Hover effect for service boxes */
.service-box:hover {
    transform: scale(1.05);
    box-shadow: 0 0 25px #FFDD57;
}

.contact-container {
        text-align: center;
        padding: 50px;
        max-width: 500px;
        margin: 100px auto;
        background: rgba(0, 0, 0, 0.5);
        border-radius: 10px;
        box-shadow: 0 0 10px #FFDD57;
    }
    
    .contact-container h2 {
        font-size: 2rem;
        margin-top: 40px;
        color:#ef49e1
    }
    
    .contact-container p {
        font-size: 1.2rem;
        margin-bottom: 20px;
    }
    
    form {
        display: flex;
        flex-direction: column;
    }
    
    form input, form textarea {
        width: 50%;
        padding: 10px;
        margin: 5px 0;
        margin-left: 100px;
        border: 1px solid #067d28;
        border-radius: 5px;
        font-size: 1rem;
        
    }
    
    form textarea {
        height: 150px;
    }
    
    button {
    margin-top: 20px;
    padding: 12px;
    align-items: center;
    background-color: #068D9D;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1.2rem;
    transition: 0.3s ease-in-out;
    box-shadow: 0 0 10px #FFDD57;
    animation: glowing 1.5s infinite alternate;
    }
    
    button:hover {
        background-color: #53599A;
    }
    
/* Animations */
@keyframes glowingCircle {
    0% {
        box-shadow: 0 0 15px #FFDD57, 0 0 40px #FFDD57, 0 0 60px #FFDD57, 0 0 80px #068D9D;
    }
    25% {
        box-shadow: 0 0 15px #FFDD57, 0 0 40px #FFDD57, 0 0 60px #FFDD57, 0 0 80px #53599A;
    }
    50% {
        box-shadow: 0 0 15px #FFDD57, 0 0 40px #FFDD57, 0 0 60px #FFDD57, 0 0 80px #FFDD57;
    }
    75% {
        box-shadow: 0 0 15px #FFDD57, 0 0 40px #FFDD57, 0 0 60px #FFDD57, 0 0 80px #068D9D;
    }
    100% {
        box-shadow: 0 0 15px #FFDD57, 0 0 40px #FFDD57, 0 0 60px #FFDD57, 0 0 80px #6D9DC5;
    }
}

@keyframes fadeIn {
    0% { opacity: 0.3; }
    100% { opacity: 1; }
}

@keyframes fadeInContent {
    0% { opacity: 0; transform: scale(0.8); }
    100% { opacity: 1; transform: scale(1); }
}

@keyframes slideIn {
    0% {
        transform: translateY(50px);
        opacity: 0;
    }
    100% {
        transform: translateY(0);
        opacity: 1;
    }

}

</body>
</html>
