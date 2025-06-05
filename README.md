# 🚀 Node.js Setup & Exploration Lab

## 📥 1. Install Node.js
- 🔗 Visit the [Node.js Downloads Page](https://nodejs.org/)
- ⬇️ Download the **LTS** version for your operating system
- 🖱️ Run the installer and follow prompts:
  - Accept license ✅
  - Choose default settings ⚙️
  - Click “Install” 📦
- 💡 *Note: Instructions may vary by OS—check with your instructor if unsure.*

---

## 🖥️ 2. Verify Installation via Command Line
- Open **Git Bash** or your terminal of choice
- Run:
  ```bash
  node -v     # 🟢 Node version
  npm -v      # 📦 npm version
✅ If successful, continue. If not, review installation or ask for help.

Test JS directly in CLI:
bash
Copy
Edit
node -p "17 + 25"   # ➕ Runs and prints result

📄 3. Write and Run a JS File
Create a file named index.js
Add code like:
js
Copy
Edit
console.log("Hello, World! 🌍");
Run:
bash
Copy
Edit
node index.js

📦 4. Initialize npm
From your project folder:
bash
Copy
Edit
npm init      # Step-by-step init
npm init -y   # 🧙‍♂️ Quick init with defaults
Update package.json:
json
Copy
Edit
"scripts": {
  "start": "node index.js"
}
Then run:
bash
Copy
Edit
npm start  # ▶️ Runs index.js

⚙️ 5. Install & Use nodemon
Install:
bash
Copy
Edit
npm install --save-dev nodemon
Update your start script:
json
Copy
Edit
"scripts": {
  "start": "nodemon index.js"
}
Run your app with:
bash
Copy
Edit
npm start  # 🔁 Auto-reloads on changes

🌐 6. Build a Basic Server
Use Node’s http module:
js
Copy
Edit
const http = require('http');
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World! 🌍\n');
});
server.listen(3000, '127.0.0.1', () => {
  console.log('Server running at http://127.0.0.1:3000/');
});
Open browser and visit: http://localhost:3000

🛣️ 7. Add Custom Routes (Optional Exploration)
Modify server to handle multiple routes 🧪
Example:
js
Copy
Edit
if (req.url === "/about") {
  res.end("<h1>About Page 👤</h1>");
}