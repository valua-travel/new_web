# CLAUDE.md — Migració web Valua Travel (WordPress → Next.js)

Context del projecte per a Claude Code. Font de veritat: `valua-web/documentació/EL-PROJECTE.md` i el full de ruta (`valua-web/documentació/Hoja de ruta migración web ...md`).

## Què és Valua Travel
Agència de viatges especialitzada en **viatges per a grups escolars**, estades lingüístiques i viatges d'aventura.

## Les sis línies de negoci
1. **Valua Groups** (pàgina pròpia prevista, **en STANDBY**: no hi ha text)
2. **Valua Languages**
3. **Attitude**
4. **I2EU** (pàgina pròpia prevista, **en STANDBY**: no hi ha text)
5. **Valua Tribes** (línia nova, 07/10/2026): viatges per a col·lectius, grups o comunitats que comparteixen una passió. Ja existeix `/tribes/` en català
6. **Valua Services** (sisena línia, Gonçal 07/10/2026): és la mateixa pàgina que `/serveis/` (serveis turístics per a grups i empreses)

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
- **Esborranys (24 tours, 18 entrades): STANDBY.** Entrades de la paperera: fora.
- **Àrea Client:** plataforma externa; no es crea ara, però l'arquitectura deixa lloc previst.
- **Peu de pàgina** (Turisme Responsable, Reclamació Gencat, «El nostre compromís»): standby; Gonçal passarà els textos.
- **Xifres vigents:** +20 anys, +30.000 persones l'any, 20 persones d'equip, 5.500 proveïdors, +3.000 bitllets, 230 grups, 176 empreses de transport.
- **To i estil:** to proper (tutejant); l'estil visual (colors, tipografies) ha de ser el de la web actual de WordPress. La web actual és també la referència d'inspiració: no calen webs de referència externes.

## Normes de treball
- **No s'esborra ni es mou res a SharePoint.** Mai, sense excepcions.
- **No es guarden DNI ni dades personals** al projecte. No es demanen ni es comparteixen contrasenyes.
- Segueix el full de ruta fase a fase; als punts de parada cal l'**OK escrit de Gonçal**.
- Codi a `valua-web/`. Els fitxers es pugen **a mà a `main`** amb el compte de l'empresa (decisió de l'usuari, 07/10/2026). No es fan commits ni push des de Claude Code i la branca local `xinhao` ja no es fa servir.
- `valua-web/_fuentes/` i les còpies de seguretat **no van mai a GitHub**.
- Repo remot: `valua-travel/new_web`.
- L'usuari té poca experiència amb WordPress: dona instruccions clic a clic.

## Estructura
- `valua-web/` — codi Next.js i documentació (veure `valua-web/AGENTS.md`: aquesta versió de Next.js té canvis incompatibles; llegeix `node_modules/next/dist/docs/` abans de programar).
- `valua-web/_fuentes/` — text original, traduccions EN, imatges, redireccions.
- `SEO_yoast/`, `SEO_crawl/`, `sitemap/`, `INVENTARI_PLUGINS/`, `captures-formularis/` — lliurables d'inventari.
- `backups_wordpress_2026-10-05/`, `wp-content.zip` — còpies de seguretat; no tocar. (La carpeta del backup es diu així, no `01_backup_completo_...` com diu el full de ruta; no es reanomena.)
