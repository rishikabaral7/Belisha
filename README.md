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

## **4. Install Tailwind CSS and Vite Plugin**

Next, we need to install **Tailwind CSS** and the **Vite plugin** for Tailwind. Run the following command:

```bash
npm install tailwindcss @tailwindcss/vite
```

This will install **Tailwind CSS** and its **Vite plugin** to make Tailwind work with Vite.

---

## **5. Install `svelte-spa-router`**

To enable routing in your Svelte application, install the `svelte-spa-router` package:

```bash
npm install svelte-spa-router
```

This package is used to define and manage routes in the application.

---

## **6. Configure the Vite Plugin**

Add the `@tailwindcss/vite` plugin to your Vite configuration:

```javascript
import { defineConfig } from 'vite';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
});
```

---

## **7. Import Tailwind CSS**

Add an `@import` to your CSS file that imports **Tailwind CSS**:

```css
@import "tailwindcss";
```

---

## **8. Run the Development Server**

To run your development server, use the following command:

```bash
npm run dev
```

This will start the **Vite development server**, and you can view your project in your browser.

---

## **9. Build for Production**

When you're ready to deploy your project, you can build it for production by running:

```bash
npm run build
```

This will create an optimized version of your project in the `dist` folder.





