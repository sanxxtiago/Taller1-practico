
# 🌍 Taller 1 - Consumo de API con TypeScript y NestJS

Aplicación web simple que consume la **REST Countries API** para consultar información de países.
El proyecto está dividido en **backend con NestJS** y **frontend con React + TypeScript**.

El objetivo del taller es practicar:

- Consumo de APIs públicas mediante **HTTP GET**
- Uso correcto de **TypeScript**
- Programación **asíncrona con async/await**
- Definición de **interfaces**
- Manejo de **errores**
- Construcción de una **interfaz gráfica sencilla**

---

# 🧠 Tecnologías utilizadas

### Backend
- NestJS
- TypeScript
- Axios (HttpService de NestJS)
- REST Countries API

### Frontend
- React
- TypeScript
- Vite

### API utilizada
https://restcountries.com

---

# ⚙️ Arquitectura del proyecto

```
Taller1-Practico
│
├── backend
│   ├── src
│   │   ├── countries
│   │   │   ├── countries.controller.ts
│   │   │   ├── countries.service.ts
│   │   │   ├── countries.module.ts
│   │   │   └── country.interface.ts
│   │   ├── app.module.ts
│   │   └── main.ts
│
└── frontend
    ├── src
    │   ├── App.tsx
    │   ├── main.tsx
    │   ├── types.ts
    │   └── styles.css
    └── index.html
```

---

# 🚀 Cómo ejecutar el proyecto

## 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/sanxxtiago/Taller1-Practico
```

---

# ▶️ Ejecutar Backend (NestJS)

Entrar a la carpeta:

```bash
cd backend
```

Instalar dependencias:

```bash
npm install
```

Iniciar servidor:

```bash
npm run start:dev
```

Servidor disponible en:

http://localhost:3000

Endpoints disponibles:

GET /countries  
GET /countries/:name

---

# 💻 Ejecutar Frontend (React)

Entrar a la carpeta:

```bash
cd frontend
```

Instalar dependencias:

```bash
npm install
```

Ejecutar proyecto:

```bash
npm run dev
```

Abrir en el navegador:

http://localhost:5173

---

# 🔎 Funcionalidades

La aplicación permite:

### 🔍 Buscar países por nombre

Ejemplo:

Colombia  
Argentina  
Canada  

---

### 🌍 Mostrar información del país

Se visualiza:

- Nombre
- Capital
- Población
- Región
- Bandera

---

### 🎲 Carga inicial de países

Cuando la aplicación se abre:

- Se genera **una letra aleatoria**
- Se consulta la API con esa letra
- Se muestran **3 países aleatorios**

Esto evita que la interfaz aparezca vacía al iniciar.

---

### ⌨️ Búsqueda rápida con Enter

El usuario puede:

- escribir un país
- presionar **Enter**
- ver los resultados inmediatamente

---

# 📦 Uso de TypeScript

Se implementa tipado mediante **interfaces**.

Ejemplo:

```ts
export interface Country {
  name:{
    common:string
  }
  capital?:string[]
  population:number
  region:string
  flags:{
    png:string
  }
}
```

Esto permite:

- mejor control de datos
- autocompletado
- reducción de errores

---

# ⚡ Programación asíncrona

Las peticiones a la API se manejan con:

async / await

Ejemplo:

```ts
const res = await fetch(`http://localhost:3000/countries/${search}`)
const data:Country[] = await res.json()
```

---

# 🛑 Manejo de errores

La aplicación incluye manejo de errores usando:

try / catch

En caso de que el país no exista o falle la API, se muestra un mensaje en pantalla.

---

# 🎯 Criterios del taller cubiertos

✔ Consumo de API pública (GET)  
✔ Uso de TypeScript  
✔ Interfaces y tipado  
✔ Programación asíncrona  
✔ Manejo de errores  
✔ Interfaz gráfica funcional  
✔ Organización clara del código  

---

# 👨‍💻 Autor

**Santiago Rios**

Proyecto desarrollado para la asignatura **Introducción a Backend con NestJS**.
