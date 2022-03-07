# parthri.github.io
My Portfolio Website
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- favicon -->
  <link rel="shortcut icon" href="images/favicosn-1.ico" type="image/x-icon" />
  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
  <!-- AOS -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css" />
  <!-- Glidejs -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Glide.js/3.4.1/css/glide.core.css" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Glide.js/3.4.1/css/glide.theme.css" />
  <!-- Custom Stylesheet -->
  <link rel="stylesheet" href="styles.css" />
  <title>Portfolio Website</title>

  <style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;600&display=swap');

:root {
  --customColor: #18eaf1;
  --purple: #c71ee9;
  --blue: #17d5db;
  --orange: #e6372b;
  --cyan: #0314ff;
  --light: #46c4bd;
}


*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  scroll-behavior: smooth;
  box-sizing: border-box;
  font-size: 62.5%;
}

body {
  font-family: 'Poppins', sans-serif;
  font-size: 1.6rem;
  font-weight: 400;
  background-color: #fff;
  color: #222;
  position: relative;
  z-index: 1;
}

h1,
h2,
h3,
h4 {
  font-weight: 500;
}

a {
  text-decoration: none;
}

img {
  max-width: 100%;
}

li {
  list-style-type: none;
}

.container {
  max-width: 114rem;
  margin: 0 auto;
}

@media only screen and (max-width: 1200px) {
  .container {
    padding: 0 3rem;
  }
}

/* Header */
.header {
  position: relative;
  width: 100%;
  min-height: 100vh;
  background-color: rgb(0, 0, 19);
  z-index: 1;
  overflow: hidden;
}

.header img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: -1
}

.nav {
  padding: 1.6rem 0
}

.nav.fix-nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: var(--customColor);
  box-shadow: 0 5px 15px rgba(0, 0, 0, .1);
  z-index: 999;
}

.nav.fix-nav .logo h1 span {
  color: #fff
}

.navigation {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo h1 {
  font-size: 2.5rem;
  color: #fff;
}

.logo h1 span {
  font-weight: bold;
  color: var(--customColor);
}

.nav-list {
  display: flex;
  align-items: center;
}

.nav-item:not(:last-child) {
  margin-right: .5rem;
}

.nav-link:link,
.nav-link:visited {
  color: #fff;
  padding: .8rem 1rem;
  transition: all 300ms ease-in-out;
}

.nav-link:hover {
  border-radius: .3rem;
  background-color: var(--customColor);
}

.hamburger,
.top-nav {
  display: none;
}

@media only screen and (max-width: 768px) {
  .menu {
    position: fixed;
    top: 0;
    left: -100%;
    width: 0%;
    max-width: 35rem;
    height: 100%;
    background-color: #fff;
    transition: all 500ms ease-in-out;
    z-index: 100;
  }

  .menu.show {
    left: 0;
    width: 100%;
  }

  .top-nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: var(--customColor);
    padding: 1rem 1.6rem;
  }

  .logo h1 span,
  .top-nav .close {
    color: #fff;
  }


  .hamburger,
  .top-nav .close {
    display: block;
    color: #fff;
    font-size: 2.3rem;
    padding: .5rem;
    cursor: pointer;
  }

  .nav-link:link,
  .nav-link:visited {
    display: block;
    font-size: 1.7rem;
    color: #222;
    padding: 1rem 0;
  }

  .nav-list {
    flex-direction: column;
    align-items: flex-start;
    padding: 1rem 1.6rem;
  }

  body.show::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, .8);
    z-index: 1;
  }

  .nav.show {
    background-color: rgba(0, 0, 0, .8);
  }
}

/* Hero */
.hero {
  position: absolute;
  top: 50%;
  right: 5%;
  transform: translate(0, -50%);
  color: #fff;
}

.hero h3 {
  font-weight: 400;
  font-size: 2rem;
}

.hero h1 {
  font-size: 9rem;
  margin: 0;
}

.hero h4 {
  font-size: 2rem;
}

.hero h4 span {
  color: var(--customColor);
  text-decoration: underline;
}

.hero a:link,
.hero a:visited {
  display: inline-block;
  padding: .8rem 2.5rem;
  border: 1px solid var(--customColor);
  background-color: var(--customColor);
  color: #fff;
  margin-top: 2rem;
}

.hero a:hover {
  background-color: transparent;
}

@media only screen and (max-width: 1200px) {
  .hero {
    transform: translate(-5%, 50%);
  }

  .hero h1 {
    font-size: 7rem;
  }
}

@media only screen and (max-width: 996px) {
  .hero {
    transform: translate(5%, 50%);
  }

  .hero h1 {
    font-size: 6rem;
  }
}

@media only screen and (max-width: 768px) {

  .hero h1 {
    font-size: 5rem;
  }
}


@media only screen and (max-width: 768px) {

  .hero h1 {
    font-size: 5rem;
  }

}

@media only screen and (max-width: 567px) {

  .hero {
    top: 65%;
    transform: translate(0, -50%);
  }

  .hero h1 {
    font-size: 4rem;
  }

  .hero h3 {
    font-size: 1.6rem;
  }

  .hero h4 {
    font-size: 1.6rem;
  }

}

.icons {
  position: absolute;
  bottom: 5%;
  right: 10%;
  color: #fff
}

.icons span:not(:last-child) {

  margin-right: 1rem;
}

.icons span {
  font-size: 2rem;
  cursor: pointer;
  transition: all 300ms ease-in-out;
}

.icons span:hover i {
  color: var(--customColor);
}

@media only screen and (max-width: 967px) {
  .icons {
    display: none;
  }
}

.control {
  position: fixed;
  right: -3.5rem;
  top: 15%;
  transition: all 300ms ease-in-out;
  z-index: 1000;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

.control.open {
  right: 0;
}

.control .widget {
  position: absolute;
  left: -3.4rem;
  border-radius: 1rem 0 0 1rem;
  padding: .5rem .7rem;
  margin-right: .1rem;
  box-shadow: 0 2px 5px rgba(0, 0, 0, .4);
  cursor: pointer;
  background-color: #fff;
  text-align: center;
}

.control .widget i {
  font-size: 2rem;
  animation: spin 2s linear infinite;
}

.control .colors {
  background-color: #fff;
  padding: 1rem .8rem;
  box-shadow: 0 2px 5px rgba(0, 0, 0, .2);
}

.control .colors span {
  display: block;
  width: 1.9rem;
  height: 1.9rem;
  padding: .7rem;
  border-radius: 50%;
  box-shadow: 0 2px 5px rgba(0, 0, 0, .2);
  cursor: pointer;
}

.control .colors span:not(:last-child) {
  margin-bottom: .7rem;
}

.control .colors span:nth-child(1) {
  background-color: var(--cyan);
}

.control .colors span:nth-child(2) {
  background-color: var(--orange);
}

.control .colors span:nth-child(3) {
  background-color: var(--purple);
}

.control .colors span:nth-child(4) {
  background-color: var(--blue);
}


/* About */

.section {
  padding: 5rem 0 7rem 0;
  overflow-x: hidden;
}

.about {
  margin-top: 5rem;
}

.about-center {
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 3rem 5rem;
}

.title {
  margin: 4rem 0 7rem 0;
  text-align: center;
}

.title h1 {
  font-size: 3rem;
  display: inline-block;
  position: relative;
  z-index: 0;
}

.title h1::after {
  content: '';
  position: absolute;
  left: 50%;
  bottom: -20%;
  transform: translate(-50%, -50%);
  background-color: var(--customColor);
  width: 50%;
  height: .4rem;
  z-index: 1;
}

.left img {
  height: 40rem;
  width: 100%;
  object-fit: cover;
}

.right h1 {
  margin-bottom: 2rem;
}

.right p {
  line-height: 2;
  margin-bottom: 2rem;
  color: #333;
}

.right h1 span {
  color: var(--customColor);
}

a.btn,
.btn-form {
  display: inline-block;
  padding: 1rem 2rem;
  background-color: var(--customColor);
  color: #fff;
  border-radius: .5rem;
  border: 2px solid var(--customColor);
  box-shadow: 0 10px 10px rgba(0, 0, 0, .1);
  transition: all 300ms ease-in-out;
}

a.btn:hover,
.btn-form:hover {
  transform: translateY(-3px);
  background-color: transparent;
  color: inherit
}

a.btn:active,
.btn-form:active {
  transform: translateY(0);
}

@media only screen and (max-width: 996px) {
  .right h1 {
    font-size: 2rem;
  }

  .right p {
    font-size: 1.5rem;
  }

  a.btn {
    padding: .7rem 1.8rem;
  }

  .left img {
    height: 40rem;
    max-width: 25rem;
  }
}


@media only screen and (max-width: 996px) {
  .about-center {
    grid-template-columns: 1fr;
    gap: 3rem 0;
  }

  .left {
    text-align: center;
  }

  .left img {
    height: 40rem;
    max-width: 90%;
  }
}




/* Skills */

.skills{
    background-color: #0e1538;
    color:   rgb(136, 142, 148);

}

.skills-box:not(:last-child) {
  margin-bottom: 2rem;
  
}

.skills-box h4 {
  font-size: 1.8rem;
  color:  rgb(136, 142, 148);
  font-weight: 500;
}

.skills-box .skills-ilt {
  width: 100%;
  position: relative;
  height: .4rem;
  background-color:  rgb(136, 142, 148);
  border-radius: .5rem;
}

.skills-box .skills-bar {
  background-color: var(--customColor);
  height: .4rem;
  color:  rgb(136, 142, 148);
}

.skills-box .html {
  width: 95%;
}

.skills-box .nodejs {
  width: 60%;
}

.skills-box .css {
  width: 60%;
}

.skills-box .javascript {
  width: 70%;
}

.skills-box .mongodb {
  width: 50%;
}

.skills-box span {
  position: absolute;
  bottom: 10%;
  right: 0;
  font-size: 1.4rem;
}

.skills-center {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6rem;
  color: rgb(136, 142, 148);
}

.right h3 {
  margin-bottom: 5rem;
  color:  rgb(136, 142, 148);
}


.right p {
  margin-bottom: 2rem;
  color:  rgb(136, 142, 148);
}

@media only screen and (max-width: 768px) {
  .skill-center {
    grid-template-columns: 1fr;
    
  }
}

/* Contact */


.contact-center{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
}

.left h2{
  font-size: 2.5rem;
}


.left p{
  font-size: 1.6rem;
  margin-bottom: 2rem;
}

.left div{
  display: flex;
  align-items: center;
  margin-bottom: 1.5rem;
}

.left div .content{
  text-align: left;
}

.left .icon{
  margin-right: 2rem;
  font-size: 2.3rem;
  color: var(--customColor);
}

form h2{
  font-size: 2rem;
  margin-bottom: 1rem;
}

.form input,.form textarea{
font-family: 'Poppins', sans-serif;
font-size: 1.6rem;
padding: 1rem 0;
text-indent: 1rem;
border-radius: .5rem;
margin-bottom: 1rem;
width: 100%;
outline: none;
border: none;
border: 1px solid rgb(175, 165, 165);

}

.form .right div{
  display: flex;
}

.form .right div input{
  flex: 1 1 50%;
}

.form textarea{
  width: 100%;
  resize: vertical;
  margin-bottom: 3rem;
}

@media only screen and (max-width: 768px){
  .contact-center{
    grid-template-columns: 1fr;
  }

  .contact-center .left{
    text-align: left;
  }

  .left div .content h3{
    font-size: 1.6rem;
  }

  .left div .content span{
    font-size: 1.5rem;
  }
}


footer{
  background-color: #000;
  padding: 1.6rem 1rem;
  text-align: center; 
}

footer p{
  color: white;
}

footer p span{
  color: var(--customColor);
}

  </style>



</head>

<body>
  <!-- Header -->
  <header class="header" id="home">
    <!-- Navigation -->
    <nav class="nav">
      <div class="navigation container">
        <div class="logo">
          <h1>Parth <span>B</span>rahmbhatt</h1>
        </div>

        <div class="menu">
          <div class="top-nav">
            <div class="logo">
              <h1>Parth <span>B</span>rahmbhatt</h1>
            </div>

            <div class="close">
              <i class="fas fa-times"></i>
            </div>
        </div>

        <ul class="nav-list">
          <li class="nav-item">
            <a href="#home" class="nav-link scroll-link">Home</a>
            <a href="#about" class="nav-link scroll-link">About</a>
            <a href="#skills" class="nav-link scroll-link">Skills</a>
            <a href="#contact" class="nav-link scroll-link">Contact</a>
          </li>
        </ul>
      </div>
      <div class="hamburger">
        <i class="fas fa-bars"></i>
      </div>
    </div>
  </nav>

  

  <!-- Hero -->
  <div class="hero">
    <h3>Hello, my name is</h3>
    <h1>Parth Brahmbhatt</h1>
    <h4>And I'm a <span id="type1" class="typeit"></span></h4>
    <a href="#">Hire me</a>
  </div>

  <div class="icons">
    <span><i class="fab fa-facebook-f"></i></span>
    <span><i class="fab fa-instagram"></i></span>
    <span><i class="fab fa-twitter"></i></span>
  </div>

  <!-- Color -->
  <div class="control">
    <div class="widget">
      <i class="fas fa-cog"></i>
    </div>
    <div class="colors">
        <span data-id="#0044ff"></span>
        <span data-id="#ff4600"></span>
        <span data-id="#ce00ff"></span>
        <span data-id="#03ffc7"></span>
      </div>
    </div>
  </header>

  <!-- Main -->
  <section class="section about" id="about">
    <div class="title">
      <h1>About me</h1>
    </div>

    <div class="about-center container">
      <div class="left" data-aos="fade-right" data-aos-duration="1500">
       
      </div>
      <div class="right" data-aos="fade-left" data-aos-duration="1500">
        <h1>I'm Parth a <span id="type2"></span></h1>
        <p>
         Learning  a Web Desgining , app Developing and Node Js
        </p>
        <a href="#" class="btn">Download</a>
      </div>
    </div>
  </section>

  

  <!-- Skills -->
  <section class="section skills" id="skills">
    <div class="title">
      <h1>My Skills</h1>
    </div>

    <div class="skills-center container">
      <div class="skills-left">
        <div class="skills-box">
          <h1>MY SKILLS</h1>
          <h4>HTML</h4>
          <div class="skills-ilt">
            <div class="skills-bar html"></div>
            <span>95%</span>
          </div>
        </div>
        <div class="skills-box">
          <h4>CSS</h4>
          <div class="skills-ilt">
            <div class="skills-bar css"></div>
            <span>60%</span>
          </div>
        </div>
        <div class="skills-box">
          <h4>DART</h4>
          <div class="skills-ilt">
            <div class="skills-bar javascript"></div>
            <span>75%</span>
        </div>
      </div>
      <div class="skills-box">
        <h4>NODEJS</h4>
        <div class="skills-ilt">
          <div class="skills-bar nodejs"></div>
          <span>66%</span>
        </div>
      </div>
      <div class="skills-box">
        <h4>C</h4>
        <div class="skills-ilt">
          <div class="skills-bar mongodb"></div>
          <span>75%</span>
        </div>
      </div>
    </div>

    <div class="right">
      <h3>My Creative skills and experience</h3>
      <p>
        I'm Learning App developing , Web Degining , Flutter , React and Node js 
      </p>
      <a href="" class="btn">Read more</a>
    </div>
  </div>
</section>



<section class="section contact" id="contact">
<div class="title">
  <h1>Contact me</h1>
</div>

<div class="contact-center container">
    <div class="left" data-aos="fade-dowm" data-aos-duration="1500">
        <h2>Get In Touch</h2>
        <p>
            </p>
        <div>
          <span class="icon"><i class="fas fa-user"></i></span>
          <span class="content">
            <h3>Name</h3>
            <span>Parth Brahmbhatt</span>
          </span>
        </div>

        <div>
          <span class="icon"><i class="fas fa-map-marker-alt"></i></span>
          <span class="content">
            <h3>Address</h3>
            <span>Surat,Piplod</span>
          </span>
        </div>

        <div>
          <span class="icon"><i class="fas fa-envelope"></i></span>
          <span class="content">
            <h3>Email</h3>
            <span>brahmbhattp974@gmail.com</span>
          </span>
        </div>
      </div>

      <div class="right" data-aos="fade-up" data-aos-duration="1500">
        <form action="https://formsubmit.co/amarjeetkumar802212@gmail.com" method="POST" class="form">
          <h2>Message Me</h2>
          <div>
            <input type="text" placeholder="Name" required />
            <input type="email" name="email" placeholder="Email Address" required />
          </div>

          <textarea name="message" id="" cols="30" rows="10" placeholder="Your message">
            </textarea>
          <button type="submit" class="btn btn-form">Send message</button>
        </form>
    </div>
</div>
</section>



<!-- Scripts -->
<!-- AOS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
<!-- TypeIt -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/typeit/7.0.4/typeit.min.js"></script>
<!-- Glidejs -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/Glide.js/3.4.1/glide.min.js"></script>
<!-- GSAP -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.6.1/gsap.min.js"></script>
<!-- Custom Script -->
<script src="index.js"></script>
<script>
    const navBar = document.querySelector(".nav");
const navHeight = navBar.getBoundingClientRect().height;
window.addEventListener("scroll", () => {
  const scrollHeight = window.pageYOffset;
  if (scrollHeight > navHeight) {
    navBar.classList.add("fix-nav");
  } else {
    navBar.classList.remove("fix-nav");
  }
});

// Scroll To
const links = [...document.querySelectorAll(".scroll-link")];
links.map((link) => {
  link.addEventListener("click", (e) => {
    e.preventDefault();

    const id = e.target.getAttribute("href").slice(1);
    const el = document.getElementById(id);
    const fixNav = navBar.classList.contains("fix-nav");
    let position = el.offsetTop - navHeight;

    window.scrollTo({
      top: position,
      left: 0,
    });

    navBar.classList.remove("show");
    menu.classList.remove("show");
    document.body.classList.remove("show");
  });
});

// Toggle Menu
const menu = document.querySelector(".menu");
const navOpen = document.querySelector(".hamburger");
const navClose = document.querySelector(".close");

const navLeft = menu.getBoundingClientRect().left;
navOpen.addEventListener("click", () => {
  if (navLeft < 0) {
    menu.classList.add("show");
    document.body.classList.add("show");
    navBar.classList.add("show");
  }
});

navClose.addEventListener("click", () => {
  if (navLeft < 0) {
    menu.classList.remove("show");
    document.body.classList.remove("show");
    navBar.classList.remove("show");
  }
});

// Colors

const widget = document.querySelector(".widget");
const control = document.querySelector(".control");

widget.addEventListener("click", () => {
  control.classList.toggle("open");
});

const colors = [...document.querySelectorAll(".colors span")];
document.querySelector(":root").style.setProperty("--customColor", "#0044ff");

colors.forEach((color) => {
  color.addEventListener("click", () => {
    const currentColor = color.dataset.id;
    document
      .querySelector(":root")
      .style.setProperty("--customColor", currentColor);
  });
});

window.addEventListener("scroll", () => {
  control.classList.remove("open");
});

// Glidejs

const glide = document.querySelector(".glide");

if (glide)
  new Glide(glide, {
    type: "carousel",
    startAt: 0,
    perView: 3,
    gap: 30,
    hoverpause: true,
    autoplay: 2000,
    animationDuration: 800,
    animationTimingFunc: "linear",
    breakpoints: {
      996: {
        perView: 2,
      },
      768: {
        perView: 1,
      },
    },
  }).mount();

AOS.init();

new TypeIt("#type1", {
  speed: 120,
  loop: true,
  waitUntilVisible: true,
})
  .type("Designer", { delay: 400 })
  .pause(500)
  .delete(9)
  .type("Developer", { delay: 400 })
  .pause(500)
  .delete(9)
  .go();

new TypeIt("#type2", {
  speed: 120,
  loop: true,
  waitUntilVisible: true,
})
  .type("Designer", { delay: 400 })
  .pause(500)
  .delete(9)
  .type("Developer", { delay: 400 })
  .pause(500)
  .delete(9)
  .go();

gsap.from(".logo", { opacity: 0, duration: 1, delay: 0.5, y: -10 });
gsap.from(".hamburger", { opacity: 0, duration: 1, delay: 0.8, x: 20 });
gsap.from(".banner", { opacity: 0, duration: 1, delay: 1.1, x: -200 });
gsap.from(".hero h3", { opacity: 0, duration: 1, delay: 1.4, y: -50 });
gsap.from(".hero h1", { opacity: 0, duration: 1, delay: 1.7, y: -45 });
gsap.from(".hero h4", { opacity: 0, duration: 1, delay: 2.1, y: -30 });
gsap.from(".hero a", { opacity: 0, duration: 1, delay: 2.4, y: -10 });

gsap.from(".nav-item", {
  opacity: 0,
  duration: 1,
  delay: 1,
  y: 30,
  stagger: 0.2,
});

gsap.from(".icons span", {
  opacity: 0,
  duration: 1,
  delay: 2.5,
  x: -30,
  stagger: 0.2,
});


</script>
</body>

</html>
