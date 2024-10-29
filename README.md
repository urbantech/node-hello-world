# node-hello-world
Step by step tutorial on creating your first Hello World App in Node
To start Node.js development on your Mac laptop, you'll need to install some essential packages and applications. Here’s a comprehensive list along with the terminal commands to get everything set up:

### 1. Install Homebrew
Homebrew is a package manager for macOS that simplifies the installation of software.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Install Node.js and npm
Node.js is the runtime environment, and npm (Node Package Manager) comes with it.

```bash
brew install node
```

### 3. Verify Installation
Check that Node.js and npm were installed correctly.

```bash
node -v
npm -v
```

### 4. Install Git
Git is essential for version control and collaboration.

```bash
brew install git
```

### 5. Set Up a Code Editor
You can use any text editor, but here are some popular ones:

- **Visual Studio Code (VS Code)**: A popular editor for JavaScript development.

```bash
brew install --cask visual-studio-code
```

### 6. Install Useful Node Packages
These packages will help streamline your development process:

- **Express**: A web framework for Node.js.
- **Nodemon**: Automatically restarts the server during development.
- **dotenv**: Loads environment variables from a `.env` file.

```bash
npm install express nodemon dotenv
```

### 7. Create Your First Node.js Project
Create a new directory for your project and navigate into it.

```bash
mkdir my-node-app
cd my-node-app
```

### 8. Initialize a New Node.js Project
This command creates a `package.json` file for your project, which keeps track of dependencies.

```bash
npm init -y
```

### 9. Create a Basic Server
Create an `index.js` file in your project folder:

```bash
touch index.js
```

Open `index.js` in your text editor and add the following code:

```javascript
const express = require('express');
const app = express();
const PORT = process.env.PORT || 3000;

app.get('/', (req, res) => {
    res.send('Hello, World!');
});

app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
```

### 10. Run Your Server
Use Nodemon to start your server so it restarts automatically on changes.

```bash
npx nodemon index.js
```

### 11. Access Your App
Open your web browser and go to `http://localhost:3000`. You should see "Hello, World!"

### Additional Tools
- **Postman**: A tool for testing APIs.
  
```bash
brew install --cask postman
```

- **MongoDB**: If you plan to work with databases, you might want to install MongoDB.

```bash
brew tap mongodb/brew
brew install mongodb-community
```

### Summary of Commands
Here’s a summary of all the commands:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install node
node -v
npm -v
brew install git
brew install --cask visual-studio-code
npm install express nodemon dotenv
mkdir my-node-app
cd my-node-app
npm init -y
touch index.js
npx nodemon index.js
brew install --cask postman
brew tap mongodb/brew
brew install mongodb-community
```

This should give you a solid foundation for starting your Node.js development journey. 
