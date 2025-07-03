# React + Vite + Tailwind CSS 4.0 Setup

## Introduction

This comprehensive guide demonstrates how to install **React JSX** + **Vite** with **Tailwind CSS 4.0** (June 2025+). 

> **Why this stack?**
> - **React**: Popular JavaScript library for building user interfaces
> - **Vite**: Fast build tool and development server
> - **Tailwind CSS 4.0**: Latest utility-first CSS framework with improved performance

Follow these steps to set up a modern React development environment with the latest Tailwind CSS version.

---

## Architecture Overview

![React + Vite + Tailwind CSS 4.0 Block Diagram](https://github.com/HorizonHnk/React-Vite-Tailwind-CSS-4.0-Setup/blob/main/Block%20Diagram%20ReactJSX.png?raw=true)

> **Visual representation** of how React, Vite, and Tailwind CSS 4.0 work together in this modern development stack.

---

## Prerequisites

Before starting the installation, make sure you have the following:

### ✅ **Node.js Installation**
> **Required:** Node.js must be installed on your PC
> - Download from: [nodejs.org](https://nodejs.org/)
> - Recommended version: **Node.js 18+** or latest LTS

### ✅ **Development Environment**
> **Recommended:** Visual Studio Code IDE
> - These commands work perfectly in **VS Code's integrated terminal**
> - Download from: [code.visualstudio.com](https://code.visualstudio.com/)

### ✅ **Verify Installation**
Check if Node.js is installed by running:
```bash
node --version
npm --version
```

> You should see version numbers for both Node.js and npm.

---

## Installation Steps

### 1. Create Vite React Project

**Template:** `react`

```bash
npm create vite@latest {projectName} -- --template react
```

> This command creates a new React project using Vite's React template. Replace `{projectName}` with your desired project name.

### 2. Navigate to Project Directory

```bash
cd {projectName}
```

> Change into your newly created project directory to continue with the setup.

### 3. Install Tailwind CSS Dependencies

**Libraries:** `tailwindcss` `@tailwindcss/vite`

```bash
npm install tailwindcss @tailwindcss/vite
```

> **What these packages do:**
> - `tailwindcss`: Core Tailwind CSS framework
> - `@tailwindcss/vite`: Official Vite plugin for Tailwind CSS 4.0 integration

### 4. Configure Vite Configuration

**Path:** `vite.config.ts`

```typescript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite'

// https://vite.dev/config/
export default defineConfig({
  plugins: [
    tailwindcss(),
    react()
  ],
})
```

> **Important:** The `tailwindcss()` plugin must be placed **before** the `react()` plugin in the plugins array for proper processing order.

### 5. Update CSS Entry Point

**Path:** `src\index.css`

```css
@import "tailwindcss";
```

> This replaces the default CSS content with Tailwind's CSS import. The `@import "tailwindcss";` directive loads all of Tailwind's styles.

---

## Project Structure

After completing the setup, your project structure will look like this:

```
{projectName}/
├── public/
├── src/
│   ├── assets/
│   ├── App.jsx
│   ├── index.css          ← Modified with Tailwind import
│   └── main.jsx
├── index.html
├── package.json
├── vite.config.ts         ← Modified with Tailwind plugin
└── README.md
```

> **Key Files Modified:**
> - `vite.config.ts`: Added Tailwind CSS plugin
> - `src/index.css`: Replaced content with Tailwind import

---

## Verification

### Start Development Server

```bash
npm run dev
```

### Test Tailwind CSS

Add some Tailwind classes to your `src/App.jsx`:

```jsx
import React from 'react'

function App() {
  return (
    <div className="min-h-screen bg-blue-500 flex items-center justify-center">
      <div className="text-center">
        <h1 className="text-4xl font-bold text-white mb-4">
          🎉 Tailwind CSS 4.0 is Working!
        </h1>
        <p className="text-blue-100 text-lg mb-6">
          Your React + Vite setup is complete
        </p>
        <button className="bg-white text-blue-500 px-6 py-3 rounded-lg font-semibold hover:bg-blue-50 transition-colors">
          Get Started
        </button>
      </div>
    </div>
  )
}

export default App
```

> **What this code demonstrates:**
> - `min-h-screen`: Full viewport height
> - `bg-blue-500`: Blue background color
> - `flex items-center justify-center`: Centers content perfectly
> - `text-4xl font-bold`: Large, bold text
> - `hover:bg-blue-50`: Color changes on hover
> - `transition-colors`: Smooth color animation

If you see a blue background with centered white text and a working button, Tailwind CSS 4.0 is properly configured!

### Expected Result

![React App Running with Tailwind CSS 4.0](https://github.com/HorizonHnk/React-Vite-Tailwind-CSS-4.0-Setup/blob/main/App%20Running.png?raw=true)

> **This is what you should see** when your React app is running successfully with Tailwind CSS 4.0!

---

## What's Different in Tailwind CSS 4.0?

> **Key Improvements:**
> - ✅ **Simplified Setup**: No PostCSS configuration required
> - ✅ **Native Vite Integration**: Direct plugin support
> - ✅ **Better Performance**: Faster builds and smaller bundles
> - ✅ **Enhanced DX**: Improved developer experience

---

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |

---

## Conclusion

🎉 **Congratulations!** You now have a fully configured React application with:

- ⚡ **Vite** as the build tool for fast development
- ⚛️ **React** for building user interfaces  
- 🎨 **Tailwind CSS 4.0** for utility-first styling

The setup is complete and ready for development. You can now start building your React application with the power of Tailwind CSS 4.0!

> **Next Steps:** Start creating components and use Tailwind's utility classes to style your application efficiently.

---

## 📞 Contact & Resources

- **📦 GitHub Repository:** [React-Vite-Tailwind-CSS-4.0-Setup](https://github.com/HorizonHnk/React-Vite-Tailwind-CSS-4.0-Setup.git)
- **📧 Email:** hhnk3693@gmail.com  
- **🎥 YouTube Channel:** [Tutorial Playlist](https://www.youtube.com/playlist?list=PLrZbkNpNVSwy9neLSBQ1QH14uL_EqNtj4)

> For more tutorials and updates, check out the YouTube channel and GitHub repository!
