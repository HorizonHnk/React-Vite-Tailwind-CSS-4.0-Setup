# React + Vite + Tailwind CSS 4.0 Setup

## Introduction

This guide shows how to install React JSX + Vite with Tailwind CSS 4.0 (June 2025+). Follow these steps to set up a modern React development environment with the latest Tailwind CSS version.

## Installation Steps

### 1. Create Vite React project
**Template:** `react`
```bash
npm create vite@latest {projectName} -- --template react
```

### 2. Navigate to project
```bash
cd {projectName}
```

### 3. Install Tailwind CSS
**Libraries:** `tailwindcss` `@tailwindcss/vite`
```bash
npm install tailwindcss @tailwindcss/vite
```

### 4. Configure vite.config.ts
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

### 5. Update src/index.css
**Path:** `src\index.css`
```css
@import "tailwindcss";
```

That's it! Your React + Vite + Tailwind CSS 4.0 setup is ready.

## Project Structure

```
{projectName}/
├── public/
├── src/
│   ├── assets/
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── index.html
├── package.json
├── vite.config.ts
└── README.md
```

## Conclusion

You now have a fully configured React application with Vite as the build tool and Tailwind CSS 4.0 for styling. The setup is complete and ready for development.
