# CLAUDE.md — Migració web Valua Travel (WordPress → Next.js)

Context del projecte per a Claude Code. Font de veritat: `valua-web/documentació/EL-PROJECTE.md` i el full de ruta (`valua-web/documentació/Hoja de ruta migración web ...md`).

## Què és Valua Travel
Agència de viatges especialitzada en **viatges per a grups escolars**, estades lingüístiques i viatges d'aventura.

## Les sis línies de negoci
1. **Valua Groups** (pàgina pròpia: decisió de Gonçal 07/10/2026; text pendent)
2. **Valua Languages**
3. **Attitude**
4. **I2EU** (pàgina pròpia; text pendent)
5. **Valua Tribes** (línia nova, 07/10/2026): viatges per a col·lectius, grups o comunitats que comparteixen una passió. Ja existeix `/tribes/` en català
6. **Valua Services** (sisena línia, confirmat per Gonçal 07/10/2026): serveis turístics per a grups i empreses. Hi ha una pàgina en esborrany; el peu de la web ja la llista

No descriguis què fa cada línia amb paraules pròpies: usa només el que diu la web actual o el que aprovi Gonçal.

## Públic
Centres educatius, professorat i famílies.

## Idiomes
La web nova serà en **català, castellà i anglès**.
- L'actual només té CA + ES (WPML); l'ES és més petit del que sembla.
- L'anglès és contingut nou: els esborranys fets amb IA (`valua-web/_fuentes/en/`) s'han de revisar abans de publicar.
- Els textos legals no es tradueixen amb IA: els revisa un jurista.
- Confirmat per Gonçal el 07/10/2026: CA + ES + EN. Tours i pàgines han d'existir en els tres.

## Regla principal: no inventar contingut
**Tot text surt de la web actual (`valua-web/_fuentes/ca/`, XML de WordPress) o l'aprova Gonçal.** No escriguis textos de màrqueting, descripcions de tours, preus, dates ni claims nous. Si falta un text, deixa un marcador visible (`[PENDENT: ...]`) i pregunta.

## Decisions de Gonçal (07/10/2026)
- **Web informativa:** no es pot comprar, pagar ni reservar. Tours amb només fitxa informativa + formulari.
- **Tours:** una fitxa per destí amb selector de durada.
- **Es migra tot:** esborranys, paperera i 52 tours antics.

## Normes de treball
- **No s'esborra ni es mou res a SharePoint.** Mai, sense excepcions.
- **No es guarden DNI ni dades personals** al projecte. No es demanen ni es comparteixen contrasenyes.
- Segueix el full de ruta fase a fase; als punts de parada cal l'**OK escrit de Gonçal**.
- Codi a `valua-web/`, en la branca `xinhao`. Cap push ni merge a `main` sense que l'equip ho decideixi. Cal correu d'empresa abans de qualsevol commit.
- `valua-web/_fuentes/` i les còpies de seguretat **no van mai a GitHub**.
- Repo remot: `valua-travel/new_web`.
- L'usuari té poca experiència amb WordPress: dona instruccions clic a clic.

## Estructura
- `valua-web/` — codi Next.js i documentació (veure `valua-web/AGENTS.md`: aquesta versió de Next.js té canvis incompatibles; llegeix `node_modules/next/dist/docs/` abans de programar).
- `valua-web/_fuentes/` — text original, traduccions EN, imatges, redireccions.
- `SEO_yoast/`, `SEO_crawl/`, `sitemap/`, `INVENTARI_PLUGINS/`, `captures-formularis/` — lliurables d'inventari.
- `backups_wordpress_2026-10-05/`, `wp-content.zip` — còpies de seguretat; no tocar.
