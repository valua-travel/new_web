# Redireccions 301 — resum (esborrany, actualitzat 07/10/2026 amb les decisions de Gonçal)

Fitxer de dades: `redirecciones.csv` (separador `;`, UTF-8). **Proposta pendent de revisió.** Encara no hi ha dades de Search Console.

## Què conté
220 regles: 216 redireccions 301 + 4 respostes 410 (pàgines de prova/ocultes).

| Confiança | Regles | Què vol dir |
|---|---|---|
| alta | 136 | Regla mecànica (slug renombrat, entrada → `/blog/`, tour → fitxa única) |
| mitjana | 66 | Raonable, però depèn d'una decisió (p. ex. arxius → llistat del blog; tours ES aparellats pel nom) |
| baixa | 18 | Cal revisar abans d'aplicar (veure sota) |

Origen: URLs de l'inventari (271) i les 28 regles que ja tenia el plugin Redirection. 68 URLs no canvien i **no necessiten regla**; 10 ja eren 404.

## Efecte de les decisions de Gonçal
- **Tours: fitxa única per destí amb selector de durada.** Les URLs per durada (`/tour/bergueda-2/`, `-3/`, `-4/`…) acaben totes a `/tour/bergueda/`. Queden **53 fitxes úniques**.
- **Tours en ES:** els 15 `/es/tour/...` ja no van a un llistat provisional: van a `/es/tour/{destí}/` (aparellats pel nom). Hi ha a més **7 tours ES publicats que el rastreig no va veure** (no enllaçats; trobats a l'XML) que també tenen regla, i un més (`/es/tour/canada-toronto/`) que ja és la fitxa única i no canvia.
- **Idiomes CA/ES/EN confirmats**, i es migra tot (esborranys, paperera, 52 tours antics). Aquests últims **no eren públics**, per tant no tenen URL antiga i no necessiten redirecció: només s'han d'afegir al sitemap quan se'n treguin de l'XML.

## Criteris
- Origen i destí són **camins** (sense domini). Les variants `http`, `www` i sense barra final es resolen amb una norma general del servidor.
- Cap cadena ni bucle. Tot destí 301 existeix a `sitemap-nuevo.xml` (excepte l'entrada amb emoji, marcada).
- Arxius automàtics (categories, etiquetes, autors, dates, paginació) → llistat del blog. Els arxius de tours van a la pàgina del programa (p. ex. `tour-tag/setmana-blava-ca` → `/setmana-blava/`).

## Cal revisar (18 de confiança baixa)
1. **16 regles antigues del plugin amb destí ES inexistent** → `/es/blog/`.
   - `/passaports-del-mon-a-la-teva-butxaca-2/` tenia 6 regles amb 6 destins diferents (només s'aplicava la primera, errònia). Es proposa l'entrada original.
   - `/es/transporte-publico-en-londres/` tenia una regla en bucle.
   - `/es/proces_inscripcio_valua/` no sembla una entrada de blog: cal comprovar què era.
2. **Praga–Berlín:** dues versions del mateix tour es fusionen en una fitxa; cal triar quin contingut és el vigent.
3. **`/es/tour/inglaterra-programa-junior-valencia-broadstairs-11-17-anos/`:** el nom diu «Valencia-Broadstairs»; cal confirmar que és el mateix programa que el de Broadstairs en català.

Mitjana però a mirar: `/tour/viaje-en-grupo-a-eslovenia/` → `eslovenia` (duplicat en castellà amb preus diferents) i l'**entrada amb emoji** a la URL (el mapa deia que no es migra, la classificació «Mantenir»; es redirigeix a l'entrada sense emoji).

## Problemes trobats en altres fitxers
- `classificacio.xlsx` marca `/viatges-fi-curs/` com a «Entrada de blog», però és una pàgina: es manté sense redirecció.
- `classificacio.xlsx` encara diu «Eliminar» per a 27 URLs i «Fusionar» per a 64, amb criteris anteriors a les decisions de Gonçal (migrar-ho tot). Cal reclassificar els esborranys i la paperera (feina pendent).

## Següents passos
1. **Fet (07/10):** extracció de l'XML a `_fuentes/xml_extra/`. Falta que Gonçal digui quins esborranys es publiquen; aleshores s'afegeixen al mapa, al sitemap i a `classificacio.xlsx`. Com no eren públics, no necessiten redirecció.
2. Quan arribin dades de Search Console: ordenar per clics i revisar primer les URLs amb tràfic.
3. Fase 7: convertir el CSV al format `redirects` de Next.js (llegir `node_modules/next/dist/docs/` abans).
