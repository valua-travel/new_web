<p align="center">
  <img src="documentaci%C3%B3/img/valua-travel-logo.jpg" alt="Logo de Valua Travel" width="120">
</p>

<h1 align="center">Valua Travel · Nova web</h1>

<p align="center">
  <em>De WordPress a Next.js: una web més ràpida, més clara i pensada per a Google.</em>
</p>

<p align="center">
  <img alt="Estat" src="https://img.shields.io/badge/estat-en%20desenvolupament-orange">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-React-black?logo=nextdotjs">
  <img alt="Idiomes" src="https://img.shields.io/badge/idiomes-CA%20%C2%B7%20ES%20%C2%B7%20EN-blue">
  <img alt="Repositori" src="https://img.shields.io/badge/repositori-privat-lightgrey">
</p>

---

## 🧭 Què és això?

Aquest repositori conté el codi de la **nova web de [Valua Travel](https://valuatravel.com)**.

La web actual està feta amb **WordPress** i un tema antic. La substituïm per una web feta amb **Next.js (React)**, més ràpida, més fàcil de mantenir i amb millor SEO.

> **Regla d'or:** no es perd res. Primer es guarda tot, després es construeix, i només al final es canvia la web antiga per la nova.

## 🌍 Qui és Valua Travel?

Agència de viatges especialitzada en **viatges per a grups escolars**, estades lingüístiques i viatges d'aventura. El públic són centres educatius, professorat i famílies. Té diverses línies de negoci: Valua Groups, Valua Languages, Attitude i I2EU.

## 🗣️ Idiomes

| Idioma | Estat |
|---|---|
| 🇨🇦 Català | Idioma principal. Contingut existent |
| 🇪🇸 Castellà | Contingut existent, més petit del que sembla |
| 🇬🇧 Anglès | **Contingut nou.** Esborranys fets amb IA, pendents de revisió |

## 🗺️ Com anem

| Fase | Què és | Estat |
|:---:|---|:---:|
| 0–1 | Accessos i programes | ✅ |
| 2 | Còpies de seguretat i exportació de tot el contingut | ✅ |
| 3 | Inventari SEO: URLs, errors i metadades | 🟡 *falten dades de visites* |
| 4 | Repositori a GitHub | 🟡 *en curs* |
| 5 | Contingut classificat, mapa de la web nova i redireccions | ⬜ |
| 6 | Disseny | ⬜ |
| 7 | Construcció de la web | ⬜ *hi ha un esquelet* |
| 8–9 | Proves a Vercel i pas a producció | ⬜ |
| 10 | Seguiment durant 4 setmanes | ⬜ |

Abans de passar de fase hi ha un **punt de parada**: cal l'OK per escrit de Gonçal.

## 🔍 El que hem descobert de la web actual

- **128 tours** gestionats pel plugin Tourmaster: és la part més gran.
- **60 %** de les pàgines no tenen meta descripció, i hi ha **31 títols duplicats**.
- **Totes les imatges** tenen el text alternatiu buit.
- **8 pàgines** donen error 404.
- Hi ha errors de contingut: meta descripcions copiades entre tours, preus ambigus, tours duplicats…

## 🗂️ Estructura del repositori

```text
new_web/
├─ src/                 Codi de la web (Next.js)
├─ content/pages/       Contingut de les pàgines
├─ public/              Imatges i fitxers estàtics
├─ documentació/        Full de ruta i explicació del projecte
└─ _fuentes/            Material de treball (NO es puja a GitHub)
```

> `_fuentes/` conté exportacions i dades de treball. Està al `.gitignore` i només viu en local i a SharePoint.

## 🚀 Posar-ho en marxa en local

```bash
npm install
npm run dev
```

Després obre [http://localhost:3000](http://localhost:3000).

## 🤝 Com treballem

- **Branca pròpia** per a cada persona que col·labora. Ningú treballa directament a `main`.
- Els canvis arriben a `main` amb un **pull request** que l'equip revisa.
- **No s'inventa contingut:** tot text surt de la web actual o l'aprova Gonçal.
- **No es guarden dades personals** ni contrasenyes al repositori.

## 📚 Més informació

- [El projecte explicat](documentaci%C3%B3/EL-PROJECTE.md)

---

<p align="center"><sub>Valua Travel · Projecte intern · 2026</sub></p>
