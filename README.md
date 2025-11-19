<h1 align="center">👋 Hi, I'm Abhishek Jadhav</h1>
<h3 align="center">Software Engineer | Frontend Developer | Problem Solver</h3>

<p align="center">
  🚀 Passionate about building clean UI, scalable systems, and real-world applications.  
  Focused on React, JavaScript, Java, and strong DSA skills.
</p>

---

## 🔥 About Me
- 🎯 Aspiring **Software Engineer** aiming for high-quality placements  
- 💻 I build **clean, scalable, and user-friendly applications**  
- 🌱 Currently learning **React**, **Java**, and **System Design basics**  
- 🎓 Actively preparing for **placement interviews**  
- ⚡ Passionate about problem-solving and writing clean code  

---

## 🛠️ Tech Stack & Skills

### 🚀 Languages & Tools
<p align="left">
  <img src="https://skillicons.dev/icons?i=java,js,react,nodejs,html,css,bootstrap,tailwind,git,github,figma,linux" />
</p>

### 🧠 Core Skills
- Data Structures & Algorithms  
- OOP & Clean Code  
- REST APIs  
- Debugging & Problem Solving  
- Frontend UI Engineering  

---

## 📚 Currently Learning
- React Advanced Concepts  
- Java + Backend Fundamentals  
- System Design Basics  
- DSA for Placements  

---

## 🌐 Connect With Me  
<p align="left">
  <a href="https://linkedin.com/in/YOUR-LINK"><img src="https://skillicons.dev/icons?i=linkedin"></a>
  <a href="mailto:youremail@gmail.com"><img src="https://skillicons.dev/icons?i=gmail"></a>
  <a href="https://github.com/abhishekjadhav45"><img src="https://skillicons.dev/icons?i=github"></a>
</p>

---

# 🎮 Working Mini Maze Game (HTML + CSS + JavaScript)
A fully working mini maze game you can run locally.  
👉 Copy the code into a file named **maze.html** and open it in a browser.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>Mini Maze Game</title>
<style>
  body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: #111;
    color: #fff;
    font-family: Arial;
  }
  #maze {
    display: grid;
    grid-template-columns: repeat(10, 40px);
    grid-template-rows: repeat(10, 40px);
    gap: 2px;
  }
  .cell {
    width: 40px;
    height: 40px;
    background: #333;
  }
  .wall {
    background: #555;
  }
  .player {
    background: #4CAF50;
  }
  .goal {
    background: #ffca28;
  }
</style>
</head>
<body>

<h2>Use Arrow Keys to Move</h2>
<div id="maze"></div>

<script>
const maze = document.getElementById("maze");

const layout = [
  "##########",
  "#P.......#",
  "#.######.#",
  "#.#....#.#",
  "#.#.##.#.#",
  "#.#.##.#.#",
  "#.#....#.#",
  "#.######.#",
  "#........#",
  "########G#"
];

let playerX = 1;
let playerY = 1;

function drawMaze() {
  maze.innerHTML = "";
  for (let y = 0; y < layout.length; y++) {
    for (let x = 0; x < layout[y].length; x++) {
      const div = document.createElement("div");
      div.classList.add("cell");

      if (layout[y][x] === "#") div.classList.add("wall");
      if (x === playerX && y === playerY) div.classList.add("player");
      if (layout[y][x] === "G") div.classList.add("goal");

      maze.appendChild(div);
    }
  }
}

function move(dx, dy) {
  const newX = playerX + dx;
  const newY = playerY + dy;

  if (layout[newY][newX] === "#") return;
  playerX = newX;
  playerY = newY;

  drawMaze();

  if (layout[playerY][playerX] === "G") {
    setTimeout(() => alert("🎉 You Reached the Goal!"), 50);
  }
}

document.addEventListener("keydown", (e) => {
  if (e.key === "ArrowUp") move(0, -1);
  if (e.key === "ArrowDown") move(0, 1);
  if (e.key === "ArrowLeft") move(-1, 0);
  if (e.key === "ArrowRight") move(1, 0);
});

drawMaze();
</script>
</body>
</html>
