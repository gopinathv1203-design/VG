<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MR__ GOPINATH - Portfolio</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
    body { line-height: 1.6; background: #f9f9f9; color: #333; }
    header { background: #333; color: #fff; padding: 1rem; position: sticky; top: 0; z-index: 1000; }
    .navbar { display: flex; justify-content: space-between; align-items: center; }
    .nav-links { list-style: none; display: flex; }
    .nav-links li { margin: 0 10px; }
    .nav-links a { color: white; text-decoration: none; padding: 8px; }
    .nav-links a:hover { background: #555; border-radius: 5px; }
    section { padding: 50px 20px; max-width: 1000px; margin: auto; }
    h2 { margin-bottom: 20px; }
    .hero { background: #eee; text-align: center; padding: 100px 20px; }
    .hero h1 span { color: #e63946; }
    .btn { display: inline-block; padding: 10px 20px; background: #333; color: white; text-decoration: none; border-radius: 5px; }
    .btn:hover { background: #555; }
    .about-content { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
    .about-content img { width: 150px; border-radius: 10px; }
    .project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; }
    .project-card { background: white; padding: 15px; border-radius: 10px; box-shadow: 0 0 5px rgba(0,0,0,0.1); }
    form input, form textarea { width: 100%; padding: 10px; margin: 10px 0; border: 1px solid #ccc; border-radius: 5px; }
    form button { background: #333; color: white; padding: 10px 15px; border: none; border-radius: 5px; cursor: pointer; }
    form button:hover { background: #555; }
    footer { text-align: center; background: #333; color: white; padding: 1rem; margin-top: 2rem; }

    /* Quiz Styles */
    .quiz-container { background: white; padding: 20px; border-radius: 10px; max-width: 500px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.2); }
    .quiz-container h2 { margin-bottom: 15px; }
    .quiz-container ul { list-style: none; margin-bottom: 20px; }
    .quiz-container li { margin: 10px 0; }
    .quiz-container button { background: #333; color: white; padding: 10px 15px; border: none; border-radius: 5px; cursor: pointer; }
    .quiz-container button:hover { background: #555; }
    .result { font-size: 18px; font-weight: bold; text-align: center; }

    /* Blog Styles */
    .post { background: white; padding: 15px; margin-bottom: 20px; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1); }
    .post h2 { margin-bottom: 10px; }
    .post small { color: gray; font-size: 12px; }

    /* Responsive Website Layout */
    .container { display: grid; grid-template-columns: 3fr 1fr; gap: 1rem; }
    .content, .sidebar { background: white; padding: 15px; border-radius: 8px; }
    @media (max-width: 768px) { .container { grid-template-columns: 1fr; } }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <div class="logo">MyPortfolio</div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#quiz">Quiz</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#responsive">Responsive Site</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero">
    <h1>Hello, I'm <span>MR__ GOPINATH</span></h1>
    <p>I am the student</p>
    <a href="#projects" class="btn">View My Work</a>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div class="about-content">
      <img src="IMG_20250817_142903.jpg" alt="Profile Photo">
      <p>
        I am a student enthusiastic about technology and design. 
        I love building interactive, user-friendly web applications and exploring new tools in the tech world.
      </p>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card"><h3>Project 1</h3><p>A simple responsive website.</p></div>
      <div class="project-card"><h3>Project 2</h3><p>JavaScript-based quiz app.</p></div>
      <div class="project-card"><h3>Project 3</h3><p>Personal blog with CMS.</p></div>
    </div>
  </section>

  <!-- Quiz App -->
  <section id="quiz">
    <h2>Quiz App</h2>
    <div class="quiz-container" id="quiz-container">
      <h2 id="question">Question text</h2>
      <ul>
        <li><label><input type="radio" name="answer" class="answer" id="a"> <span id="a_text">Answer A</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="b"> <span id="b_text">Answer B</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="c"> <span id="c_text">Answer C</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="d"> <span id="d_text">Answer D</span></label></li>
      </ul>
      <button id="submit">Submit</button>
      <div class="result" id="result"></div>
    </div>
  </section>

  <!-- Blog -->
  <section id="blog">
    <h2>My Blog</h2>
    <div id="postsContainer"></div>
  </section>

  <!-- Responsive Website Demo -->
  <section id="responsive">
    <h2>Responsive Layout</h2>
    <div class="container">
      <div class="content">
        <h3>Main Content</h3>
        <p>This is the main content area. Resize the window to see the responsive effect.</p>
      </div>
      <div class="sidebar">
        <h3>Sidebar</h3>
        <p>This is a sidebar with some extra information or links.</p>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" name="user_name" placeholder="Your Name" required>
      <input type="email" name="user_email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 MR__ GOPINATH | All rights reserved</p>
  </footer>

  <!-- Scripts -->
  <script>
    // Quiz Data
    const quizData = [
      { question: "What does HTML stand for?", a: "Hyper Text Markup Language", b: "High Text Markup Language", c: "Hyperlinks and Text Markup Language", d: "Home Tool Markup Language", correct: "a" },
      { question: "HTML comments are written like?", a: "/*comment*/", b: "//comment", c: "<!--comment-->", d: "**comment**", correct: "c" },
      { question: "Which tag is used to create a hyperlink in HTML?", a: "<link>", b: "<a>", c: "<href>", d: "<hyper>", correct: "b" },
      { question: "Which is used for database?", a: "PHP", b: "MySQL", c: "HTML", d: "CSS", correct: "b" }
    ];
    const questionEl = document.getElementById("question");
    const answerEls = document.querySelectorAll(".answer");
    const a_text = document.getElementById("a_text");
    const b_text = document.getElementById("b_text");
    const c_text = document.getElementById("c_text");
    const d_text = document.getElementById("d_text");
    const submitBtn = document.getElementById("submit");
    const resultEl = document.getElementById("result");
    let currentQuiz = 0; let score = 0;
    loadQuiz();
    function loadQuiz() {
      deselectAnswers();
      const currentQuizData = quizData[currentQuiz];
      questionEl.innerText = currentQuizData.question;
      a_text.innerText = currentQuizData.a;
      b_text.innerText = currentQuizData.b;
      c_text.innerText = currentQuizData.c;
      d_text.innerText = currentQuizData.d;
    }
    function getSelected() {
      let answer;
      answerEls.forEach(el => { if (el.checked) answer = el.id; });
      return answer;
    }
    function deselectAnswers() { answerEls.forEach(el => el.checked = false); }
    submitBtn.addEventListener("click", () => {
      const answer = getSelected();
      if (answer) {
        if (answer === quizData[currentQuiz].correct) score++;
        currentQuiz++;
        if (currentQuiz < quizData.length) loadQuiz();
        else {
          document.getElementById("quiz-container").innerHTML =
            `<h2>You answered correctly ${score}/${quizData.length} questions.</h2>
             <button onclick="location.reload()">Restart</button>`;
        }
      }
    });

    // Blog Posts Loader
    function loadPosts() {
      const postsContainer = document.getElementById("postsContainer");
      const posts = JSON.parse(localStorage.getItem("blogPosts")) || [];
      postsContainer.innerHTML = "";
      posts.reverse().forEach(post => {
        const postEl = document.createElement("div");
        postEl.classList.add("post");
        postEl.innerHTML = `<h2>${post.title}</h2><small>${new Date(post.date).toLocaleString()}</small><p>${post.content}</p>`;
        postsContainer.appendChild(postEl);
      });
    }
    loadPosts();
  </script>
</body>
</html>
