# 🪐 Planet Explorer

<div align="center">

![Planet Explorer Banner](https://img.shields.io/badge/Planet-Explorer-blueviolet?style=for-the-badge&logo=nasa&logoColor=white)

**An interactive journey through our solar system — explore planets, moons, and cosmic data in one place.**

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Stars](https://img.shields.io/github/stars/yourusername/planet-explorer?style=social)](https://github.com/yourusername/planet-explorer)
[![Forks](https://img.shields.io/github/forks/yourusername/planet-explorer?style=social)](https://github.com/yourusername/planet-explorer)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Status](https://img.shields.io/badge/status-active-brightgreen)

[🚀 Live Demo](https://premshah-22.github.io/Planet-Explorer/) · [📖 Documentation](#documentation) · [🐛 Report Bug](#) · [✨ Request Feature](#)

</div>

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Project Structure](#project-structure)
- [API / Data Source](#api--data-source)
- [Configuration](#configuration)
- [Available Scripts](#available-scripts)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

---

## 🌌 About the Project

**Planet Explorer** is an educational and visually rich web application that lets users explore every planet in our solar system. From Mercury's scorching surface to Neptune's icy winds, discover key facts, orbital data, atmospheric composition, and stunning visuals — all in an intuitive, interactive interface.

Whether you're a student, space enthusiast, or just curious about the cosmos, Planet Explorer makes learning about our solar system engaging and fun.

> "The cosmos is within us. We are made of star-stuff." — Carl Sagan

---

## ✨ Features

- 🪐 **Browse all 9 planets** with detailed information cards
- 📊 **Compare planets** side-by-side by size, mass, distance, and temperature
- 🔭 **Orbital data** — period, distance from Sun, inclination, and more
- 🌡️ **Atmospheric details** — composition, pressure, and surface conditions
- 🎨 **Beautiful UI** — space-themed dark design with smooth animations
- 📱 **Fully responsive** — works on desktop, tablet, and mobile
- 🔍 **Search & filter** — quickly find planets or facts
- 🌐 **3D planet viewer** *(optional feature — if applicable)*
- 🌙 **Dark mode** built-in

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|------------|
| Frontend | React.js / Next.js |
| Styling | Tailwind CSS / CSS Modules |
| Animations | Framer Motion |
| Data | NASA API / Local JSON |
| 3D Graphics | Three.js *(if applicable)* |
| Deployment | Vercel / Netlify |
| Version Control | Git & GitHub |

> Update this table to match your actual stack.

---

## 🚀 Getting Started

Follow these steps to run Planet Explorer locally on your machine.

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Git](https://git-scm.com/)

Check your versions:

```bash
node --version
npm --version
git --version
```

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/planet-explorer.git
```

2. **Navigate into the project directory**

```bash
cd planet-explorer
```

3. **Install dependencies**

```bash
npm install
# or
yarn install
```

4. **Set up environment variables**

```bash
cp .env.example .env.local
```

Then open `.env.local` and fill in the required values:

```env
NEXT_PUBLIC_NASA_API_KEY=your_nasa_api_key_here
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

> Get your free NASA API key at [https://api.nasa.gov/](https://api.nasa.gov/)

### Running the App

**Development mode:**

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

**Production build:**

```bash
npm run build
npm start
```

---

## 📁 Project Structure

```
planet-explorer/
├── public/
│   ├── images/
│   │   └── planets/          # Planet images and textures
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── PlanetCard/       # Individual planet card component
│   │   ├── PlanetDetail/     # Full planet detail view
│   │   ├── ComparePanel/     # Side-by-side comparison component
│   │   ├── Navbar/           # Navigation bar
│   │   └── UI/               # Shared UI components (Button, Badge, etc.)
│   ├── pages/
│   │   ├── index.js          # Home page — planet grid
│   │   ├── planet/[id].js    # Dynamic planet detail page
│   │   └── compare.js        # Comparison page
│   ├── data/
│   │   └── planets.json      # Static planet data (fallback)
│   ├── hooks/
│   │   └── usePlanets.js     # Custom hook for fetching planet data
│   ├── styles/
│   │   └── globals.css       # Global styles
│   └── utils/
│       └── formatters.js     # Number/unit formatting helpers
├── .env.example
├── .gitignore
├── package.json
├── README.md
└── LICENSE
```

---

## 🌐 API / Data Source

Planet Explorer uses the following data sources:

- **[NASA Solar System Exploration API](https://api.nasa.gov/)** — planetary imagery and mission data
- **[Le Système Solaire API](https://api.le-systeme-solaire.net/)** — detailed planetary facts (free, no key required)
- **Local JSON fallback** — static data in `/src/data/planets.json` used when APIs are unavailable

### Example API call

```js
const response = await fetch(
  'https://api.le-systeme-solaire.net/rest/bodies/mars'
);
const data = await response.json();
console.log(data.meanRadius); // 3389.5 km
```

---

## ⚙️ Configuration

| Variable | Description | Required |
|----------|-------------|----------|
| `NEXT_PUBLIC_NASA_API_KEY` | Your NASA API key | Yes |
| `NEXT_PUBLIC_APP_URL` | Base URL of the app | No |
| `NEXT_PUBLIC_ENABLE_3D` | Enable 3D planet viewer (`true`/`false`) | No |

---

## 📜 Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm start` | Start production server |
| `npm run lint` | Run ESLint |
| `npm run format` | Format code with Prettier |
| `npm test` | Run test suite |

---

## 🤝 Contributing

Contributions are welcome and appreciated! Here's how you can help:

1. **Fork** the repository
2. **Create** a new branch

```bash
git checkout -b feature/your-feature-name
```

3. **Make** your changes and commit them

```bash
git commit -m "feat: add your feature description"
```

4. **Push** to your branch

```bash
git push origin feature/your-feature-name
```

5. **Open** a Pull Request

Please make sure your code follows the existing style and passes all lint checks before submitting.

### Commit Convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

| Prefix | Use for |
|--------|---------|
| `feat:` | New features |
| `fix:` | Bug fixes |
| `docs:` | Documentation changes |
| `style:` | Formatting, no logic change |
| `refactor:` | Code restructuring |
| `chore:` | Maintenance tasks |

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

```
MIT License

Copyright (c) 2025 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 🙏 Acknowledgements

- [NASA Open APIs](https://api.nasa.gov/) — for planetary data and imagery
- [Le Système Solaire API](https://api.le-systeme-solaire.net/) — for detailed solar system data
- [Three.js](https://threejs.org/) — 3D rendering
- [Framer Motion](https://www.framer.com/motion/) — animations
- [Tailwind CSS](https://tailwindcss.com/) — utility-first styling
- [Shields.io](https://shields.io/) — README badges
- [Carl Sagan](https://en.wikipedia.org/wiki/Carl_Sagan) — for inspiring a generation of space lovers

---

## 📬 Contact

**PREM SHAH**

- GitHub: [@PremShah-22](https://github.com/PremShah-22)
- Email: shahprem1745@gmail.com
- LinkedIn: [linkedin.com/in/prem-shah-848054389](https://linkedin.com/in/prem-shah-848054389)

Project Link: [https://github.com/premshah-22/planet-explorer](https://github.com/premshah-22/planet-explorer)

---

<div align="center">

Made with ❤️ and a love for the cosmos 🌌

⭐ If you found this project useful, please consider giving it a star!

</div>
