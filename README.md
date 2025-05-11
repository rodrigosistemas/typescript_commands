````markdown
# 🚀 TypeScript Starter Project

This repository is a basic template to kickstart any Node.js project using **TypeScript**. It includes essential configuration and useful commands for development.

## 📦 Installation

Install dependencies:

```bash
npm install
````

And add the dev-tools for watch & reload:

```bash
npm install --save-dev typescript nodemon concurrently ts-node-dev
```

---

## ⚙️ Scripts

Add these scripts to your `package.json`:

```json
"scripts": {
  "build": "tsc",
  "watch": "tsc --watch --preserveWatchOutput",
  "start": "node dist/index.js",

  // Watch & restart the compiled JS
  "start:watch": "nodemon --watch dist --exec \"node dist/index.js\"",

  // Dev mode: compila en watch y reinicia el servidor automáticamente
  "dev": "concurrently \"npm run watch\" \"npm run start:watch\"",

  // Alternativa sin folder dist: compila al vuelo y reinicia
  "dev:ts": "ts-node-dev --respawn --transpile-only src/index.ts",

  // Solo chequeo de tipos (útil en CI)
  "type-check": "tsc --noEmit"
}
```

---

## 🛠 TypeScript Commands

| Command                             | Description                                              |
| ----------------------------------- | -------------------------------------------------------- |
| `tsc --init`                        | Create a `tsconfig.json` file                            |
| `tsc`                               | Compile project based on `tsconfig.json`                 |
| `tsc index.ts`                      | Compile a specific file                                  |
| `tsc --watch`                       | Recompile files on change (watch mode)                   |
| `tsc --watch --preserveWatchOutput` | Same as above, pero mantiene la salida previa en consola |
| `tsc --noEmit`                      | Check for type errors without emitting JS                |
| `tsc --target ES6`                  | Compile to specific JS version                           |
| `tsc -v`                            | Show installed TypeScript version                        |

---

## ✅ Example Workflow

```bash
# 1. Instala dependencias:
npm install
npm install --save-dev typescript nodemon concurrently ts-node-dev

# 2. Inicializa TSConfig:
npx tsc --init

# 3. Crea carpetas:
mkdir src dist
touch src/index.ts

# 4. Desarrollo en caliente:
npm run dev

# 5. Para producción:
npm run build
npm start
```
