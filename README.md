HTML 
<link rel="stylesheet" href="style.css" />

  <header>
    <h1>こんにちは、〇〇です！</h1>
    <nav>
      <a href="#about">自己紹介</a>
      <a href="#contact">お問い合わせ</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>自己紹介</h2>
      <p>ここにプロフィールや自己紹介文を入れます。</p>
    </section>

    <section id="contact">
      <h2>お問い合わせ</h2>
      <p>メールはこちらまで：example@example.com</p>
    </section>
  </main>

  <footer>
    <p>© 2025 〇〇 All rights reserved.</p>
  </footer>

  <script src="script.js"></script>

    ...
  <footer>
    <p>© 2025 〇〇 All rights reserved.</p>
  </footer>

  <!-- JavaScriptファイルを読み込む -->
  <script src="script.js"></script>

  CSS
  body {
  font-family: sans-serif;
  line-height: 1.6;
  margin: 0;
  padding: 0;
  background: #f0f0f0;
  color: #333;
}

header {
  background: #4caf50;
  color: white;
  padding: 1rem;
  text-align: center;
}

nav a {
  margin: 0 10px;
  color: white;
  text-decoration: none;
}

main {
  padding: 2rem;
  background: white;
}

footer {
  text-align: center;
  padding: 1rem;
  background: #333;
  color: white;
}
section {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.6s ease;
}

section.show {
  opacity: 1;
  transform: translateY(0);
  transition: all 0.6s ease;
}

JAVA SCRIPT
// ふわっと表示するアニメーション
const elements = document.querySelectorAll("section");

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("show");
    }
  });
});

elements.forEach(el => observer.observe(el));

// お問い合わせをクリックしたらアラート表示
const contactSection = document.querySelector("#contact");

contactSection.addEventListener("click", () => {
  alert("メールを送ってくださいね！📩");
});
