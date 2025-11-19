<h1 align="center">👋 Hi, I'm Abhishek Jadhav</h1>
<h3 align="center">Software Engineer | Full-Stack Developer | Problem Solver</h3>

<p align="center">
  🚀 Passionate about building scalable systems, clean UI, and real-world applications.  
  Focused on Java, Spring Boot, React, DSA, and modern engineering practices.
</p>

---

## 🔥 About Me
- 🎯 Aspiring **Software Engineer** with strong fundamentals in **DSA, OOP, and Web Development**
- 💻 I build **clean, scalable, and production-ready applications**
- 🌱 Currently improving my **React**, **Java**, and **System Design** skills  
- 🎓 Preparing for **placements** and building real-world projects  
- ⚡ Love solving problems & writing readable maintainable code  

---

## 🛠️ Tech Stack & Skills

### 🚀 Languages & Frameworks
<p align="left">
  <img src="https://skillicons.dev/icons?i=java,js,react,nodejs,html,css,bootstrap,tailwind,git,github,figma,linux" />
</p>

### 🧠 Core Skills
- Data Structures & Algorithms  
- OOP, SOLID Principles  
- REST APIs & Backend Architecture  
- System Design Basics  
- Clean code practices  
- Debugging & Problem Solving  

---

## 🌐 Connect With Me  
<p align="left">
  <a href="https://linkedin.com/in/YOUR-LINK"><img src="https://skillicons.dev/icons?i=linkedin"></a>
  <a href="mailto:your-email@gmail.com"><img src="https://skillicons.dev/icons?i=gmail"></a>
  <a href="https://github.com/YOUR-USERNAME"><img src="https://skillicons.dev/icons?i=github"></a>
</p>

---

# 🎮 Playable Maze Game (Fully Working!)
### ⬇ **Use Arrow Keys to Move – Reach the Green Goal!**

<div align="center">
<canvas id="mazeCanvas" width="300" height="300" style="border:2px solid #444"></canvas>

<script>
// Maze layout (1 = wall, 0 = path)
const maze = [
  [1,1,1,1,1,1,1,1,1,1],
  [1,0,0,0,1,0,0,0,0,1],
  [1,0,1,0,1,0,1,1,0,1],
  [1,0,1,0,0,0,0,1,0,1],
  [1,0,1,1,1,1,0,1,0,1],
  [1,0,0,0,0,1,0,1,0,1],
  [1,1,1,1,0,1,0,1,0,1],
  [1,0,0,1,0,0,0,0,0,1],
  [1,0,1,0,0,1,1,1,0,1],
  [1,1,1,1,1,1,1,1,1,1]
];

const canvas = document.getElementById("mazeCanvas");
const ctx = canvas.getContext("2d");

const tile = 30;
let player = { x: 1, y: 1 };
const goal = { x: 8, y: 8 };

// Draw Maze
function drawMaze() {
  for (let y = 0; y < 10; y++) {
    for (let x = 0; x < 10; x++) {
      ctx.fillStyle = maze[y][x] === 1 ? "#000" : "#fff";
      ctx.fillRect(x * tile, y * tile, tile, tile);
    }
  }

  // Goal
  ctx.fillStyle = "limegreen";
  ctx.fillRect(goal.x * tile, goal.y * tile, tile, tile);

  // Player
  ctx.fillStyle = "red";
  ctx.beginPath();
  ctx.arc(player.x * tile + 15, player.y * tile + 15, 10, 0, Math.PI * 2);
  ctx.fill();
}

// Movement
document.addEventListener("keydown", (e) => {
  let nx = player.x;
  let ny = player.y;

  if (e.key === "ArrowUp") ny--;
  if (e.key === "ArrowDown") ny++;
  if (e.key === "ArrowLeft") nx--;
  if (e.key === "ArrowRight") nx++;

  if (maze[ny][nx] === 0) {
    player.x = nx;
    player.y = ny;
  }

  drawMaze();

  // Win check
  if (player.x === goal.x && player.y === goal.y) {
    setTimeout(() => alert("🎉 You won!"), 10);
  }
});

drawMaze();
</script>
</div>

---

## ✨ Fun Fact  
💬 “A great developer is not the one who knows everything, but the one who never stops learning.”

---

## 🤝 Let's Build Something Cool  
Open to collaborations, projects, or brainstorming new ideas!
