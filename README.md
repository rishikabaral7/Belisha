# **Project Setup Guide**

This guide will help you set up your project with **Svelte**, **Vite**, and **Tailwind CSS**.

---

## **1. Prerequisites**

- Make sure you have **Node.js** and **npm** installed on your system. You can download them from [nodejs.org](https://nodejs.org/).

---

## **2. Clone the Repository**

To get started, clone the repository to your local machine using the following command:

```bash
git clone <repository-url>
```

Replace `<repository-url>` with the actual URL of your Git repository. After cloning, navigate to the project folder:

```bash
cd belisha
```

---

## **3. Install Project Dependencies**

Once you have cloned or created your project, install the necessary dependencies by running:

```bash
npm install
```

This command will install all the required packages from the `package.json` file, including **Vite**, **Svelte**, and **Tailwind CSS**.

---

## **4–7. Skip These Unless Missing in the Project**

You can **skip steps 4–7** unless the project is missing Tailwind CSS or routing setup.  
Only follow these steps if you're starting from scratch or something doesn’t work:

### 4. Install Tailwind CSS and Vite Plugin

```bash
npm install tailwindcss @tailwindcss/vite
```

### 5. Install `svelte-spa-router`

```bash
npm install svelte-spa-router
```

### 6. Configure the Vite Plugin

Edit `vite.config.js`:

```javascript
import { defineConfig } from 'vite';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
});
```

### 7. Import Tailwind CSS

In your CSS file (e.g., `app.css`), add:

```css
@import "tailwindcss";
```

---

## **8. Run the Development Server**

Start the Vite development server:

```bash
npm run dev
```

Open your browser and go to the URL shown in the terminal (usually [http://localhost:5173](http://localhost:5173)).

---

## **9. Build for Production**

To create an optimized production build:

```bash
npm run build
```

The output will be in the `dist` folder, ready for deployment.