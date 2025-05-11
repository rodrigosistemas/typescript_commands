```markdown
# 🚀 TypeScript Starter Project

This repository is a basic template to kickstart any Node.js project using **TypeScript**. It includes essential configuration and useful commands for development.

---

## 📁 Project Structure

```

project-root/
│
├── src/               # Source files (TypeScript)
│   └── index.ts
│
├── dist/              # Compiled JavaScript output
│   └── index.js
│
├── package.json       # Project metadata and scripts
├── tsconfig.json      # TypeScript compiler configuration
└── README.md

````

---

## 📦 Installation

Install dependencies:

```bash
npm install
````

---

## ⚙️ Scripts

Add these scripts to your `package.json`:

```json
"scripts": {
  "build": "tsc",
  "watch": "tsc --watch",
  "start": "node dist/index.js"
}
```

---

## 🛠 TypeScript Commands

| Command            | Description                               |
| ------------------ | ----------------------------------------- |
| `tsc --init`       | Create a `tsconfig.json` file             |
| `tsc`              | Compile project based on `tsconfig.json`  |
| `tsc index.ts`     | Compile a specific file                   |
| `tsc --watch`      | Recompile files on change (watch mode)    |
| `tsc --noEmit`     | Check for type errors without emitting JS |
| `tsc --target ES6` | Compile to specific JS version            |
| `tsc -v`           | Show installed TypeScript version         |

---

## ✅ Example Workflow

```bash
# Initialize project
npm init -y
npm install --save-dev typescript

# Create TypeScript config
npx tsc --init

# Create source and dist folders
mkdir src dist
touch src/index.ts

# Build the project
npm run build

# Run the compiled app
npm start
```
