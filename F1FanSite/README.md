# 🏎️ F1 Fan Site

---

A fan website dedicated to Formula 1 news, stats, and community engagement.

---

## 🚀 Main Features

- Latest Formula 1 news and updates
- Race statistics and driver profiles
- Interactive and modern user interface
- (To be completed as the project evolves)

---

## 🛠️ Technologies Used

- Angular (Front-end)
- NestJS (Back-end)
- HTML & CSS
- Playwright (testing)
- Docker/Podman

---

## ⚙️ Installation & Launch

### Prérequis
- Node.js >= 18
- npm
- Docker (optionnel)

### Lancer en développement

#### Front-end
```bash
cd f1-fan-frontend
npm install
ng serve
```
Accès : http://localhost:4200

#### Back-end
```bash
cd f1-fan-backend
npm install
npm run start:dev
```
Accès : http://localhost:3000

### Lancer avec Docker
```bash
docker build -t f1-fansite .
docker run -p 3000:3000 f1-fansite
```
Accès : http://localhost:3000

### Lancer les tests E2E (front)
```bash
cd f1-fan-frontend
npx playwright test
```

---

## 👤 About

This project is part of my portfolio, designed to explore web development and the world of Formula 1.

For any questions or suggestions, feel free to contact me!
