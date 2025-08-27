# Tadiran POC

A test proof-of-concept project using Node-RED with Git integration, `.env` configuration, and secure credential management.

---

## 📦 Setup Instructions

### 1. Install Node-RED
Follow the official guide:  
[https://nodered.org/docs/getting-started/](https://nodered.org/docs/getting-started/)

---

### 2. Enable Projects in Node-RED
Edit your `settings.json` to enable project mode.

📂 Typical locations for `settings.json`:
- **Linux/macOS**: `~/.node-red/settings.json`
- **Windows**: `%HOMEPATH%\.node-red\settings.json`
- **Custom install**: `<your_project>/.node-red/settings.json`

Update or add:

```js
require('dotenv').config({ path: process.env.DOTENV_PATH || '.env' });

module.exports = {
  // Enable projects
  editorTheme: {
    projects: {
      enabled: true
    }
  },

  credentialSecret: process.env.NODERED_CREDENTIAL_SECRET,
};


3. Add Environment Variables

Create a .env file in your project root:

NODERED_CREDENTIAL_SECRET=supersecretkey
DOTENV_PATH=.env



4. Run Node-RED
npx node-red



5. Stop Node-RED

Press CTRL + C in the terminal.


6. Clone Your Project Repo
cd projects
git clone <your-repo-url>