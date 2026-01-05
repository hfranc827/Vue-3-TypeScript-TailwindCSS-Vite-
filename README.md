# Vue-3-TypeScript-TailwindCSS-Vite-
# Vue 3 + TypeScript + Vite

This template should help get you started developing with Vue 3 and TypeScript in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

Learn more about the recommended Project Setup and IDE Support in the [Vue Docs TypeScript Guide](https://vuejs.org/guide/typescript/overview.html#project-setup).
📘 GUÍA COMPLETA
Vue 3 + TypeScript + TailwindCSS (Vite)
Proyecto visual / landing page (sin backend)
🧩 REQUISITOS PREVIOS

Antes de empezar, debes tener instalado:

Node.js (LTS)
👉 verifica con:

node -v
npm -v

🚀 PASO 1: Crear el proyecto con Vite

En la carpeta donde guardarás tu proyecto:

npx create-vite

Respuestas del asistente:
Project name: web_design1
Select a framework: Vue
Select a variant: TypeScript
Use rolldown-vite?: No
Install with npm and start now?: No


✔ Esto crea la estructura base del proyecto

📂 PASO 2: Entrar al proyecto
cd web_design1

📦 PASO 3: Instalar dependencias iniciales
npm install


✔ Instala Vue, Vite y TypeScript
✔ Crea la carpeta node_modules

▶️ PASO 4: Ejecutar el proyecto base
npm run dev


✔ Abre el navegador en:

http://localhost:5173


👉 Aquí confirmas que Vue funciona

🎨 PASO 5: Instalar TailwindCSS (forma moderna con Vite)
npm install tailwindcss @tailwindcss/vite


✔ Tailwind queda listo para integrarse con Vite
✔ No genera errores (los mensajes HMR son normales)

⚠️ Este comando se ejecuta SOLO UNA VEZ

⚙️ PASO 6: Conectar Tailwind con Vite
📌 Editar vite.config.ts
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    vue(),
    tailwindcss(),
  ],
})


📌 ¿Qué hace esto?

Activa Vue

Activa Tailwind dentro de Vite

🎨 PASO 7: Configurar los estilos globales
📌 Editar src/style.css
@import "tailwindcss";


📌 Este archivo será el CSS global del proyecto

🔌 PASO 8: Importar el CSS en la app
📌 Editar src/main.ts
import { createApp } from 'vue'
import App from './App.vue'
import './style.css'

createApp(App).mount('#app')


📌 Esto conecta:

Vue

App.vue

Tailwind

🧪 PASO 9: Probar que Tailwind funciona
📌 Editar src/App.vue
<template>
  <div class="h-screen flex items-center justify-center bg-black">
    <h1 class="text-6xl font-bold text-pink-500">
      GAMMA POLOS
    </h1>
  </div>
</template>


✔ Fondo negro
✔ Texto rosado
✔ Clases Tailwind funcionando

🔁 PASO 10: Hot Reload (HMR)

Cuando ves en consola:

hmr update /src/App.vue


👉 Significa:

Guardaste un archivo

Vite actualizó la página automáticamente

❌ NO es error
✅ Es una ventaja

📁 ESTRUCTURA BÁSICA DEL PROYECTO
web_design1/
├─ index.html
├─ package.json
├─ vite.config.ts
├─ src/
│  ├─ main.ts
│  ├─ style.css
│  └─ App.vue
└─ node_modules/

🎯 CONCEPTOS CLAVE QUE APRENDISTE

✔ Vite = entorno de desarrollo rápido
✔ Vue = framework frontend
✔ TypeScript = JavaScript tipado
✔ Tailwind = estilos por clases
✔ HMR = recarga automática
✔ main.ts conecta todo
✔ App.vue es la raíz visual
