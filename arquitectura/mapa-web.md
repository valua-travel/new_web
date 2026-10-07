# Arquitectura de la web nova — proposta (esborrany)

*06/10/2026. Proposta automàtica a partir de l'inventari actual (271 URLs), el sitemap i els esborranys de contingut. **No és una decisió:** cal l'OK de Gonçal. Tot el que és incert està marcat com a `[PENDENT]` o `[DECISIÓ]`.*

## 1. Principis
- **Es respecta l'estructura actual** excepte on hi ha una raó clara (es detalla a cada canvi).
- **El català és l'idioma per defecte i viu a l'arrel** (`/`). Així **les URLs catalanes que no canvien no necessiten redirecció** i no es perd posicionament. El castellà és `/es/` i l'anglès `/en/`.
- URLs curtes, en minúscula, sense accents i amb guions (no guions baixos).
- Les redireccions 301 de les URLs velles es faran al pas 5.4.

## 2. Mapa de la web (versió catalana; ES i EN reflecteixen el mateix arbre)

```text
/                                  Portada
├─ /qui-som/                       Qui som (inclou la secció d'equip)
├─ /testimonis/
├─ /contacte/
├─ /serveis/
├─ /cataleg/
├─ Línies de negoci
│  ├─ /languages/                  Valua Languages
│  ├─ /attitude/                   Attitude
│  ├─ /groups/   /i2eu/            Pàgina pròpia (decisió Gonçal); [PENDENT] contingut
│  └─ /tribes/                     Valua Tribes, línia nova
├─ Programes
│  ├─ /viatges-fi-curs/
│  ├─ /sortides-1-dia/
│  ├─ /any-escolar/
│  ├─ /summer-camps/   /ministays/
│  ├─ /setmana-blanca/   /setmana-verda/   /setmana-blava/
│  └─ /setmanes-aventura/
├─ /tours/                         Cercador de tours (substitueix /search-tours/)
│  └─ /tour/{destí}/               Fitxa única per destí, amb selector de durada
├─ /destinacions/{destí}/          7 fitxes
├─ /cursos/{curs}/                 1 fitxa (abans /cusos/, amb errata)
├─ /allotjament/{tipus}/           2 fitxes
├─ /blog/                          Llistat
│  └─ /blog/{slug}/                32 entrades (ara pengen de l'arrel)
└─ Legal: /avis-legal/  /condicions-viatge/  /politica-de-cookies/  /confirmacio-inscripcio/ (noindex)
```

## 3. Canvis respecte a l'estructura actual (i per què)
| Canvi | Raó |
|---|---|
| `/any_escolar/` → `/any-escolar/` | El guió baix no és bona pràctica d'URL |
| `/serveis/` + `/services/` → **`/serveis/`** | Eren duplicats (un amb slug en anglès) |
| `/search-tours/` → **`/tours/`** | Pàgina del tema antic (2018); es refà el cercador |
| Entrades: `/{slug}/` → **`/blog/{slug}/`** | Ara pengen de l'arrel i xoquen amb pàgines (p. ex. `/viatges-fi-curs/` és pàgina **i** entrada). Són 32 redireccions simples |
| `/personnel/{nom}/` (20 fitxes) → secció dins `/qui-som/` | Cada fitxa només té nom i càrrec (3 paraules) |
| Arxius de categories, etiquetes, dates, autors i paginació → **filtres** al blog/cercador | Són llistats automàtics sense contingut propi |
| `/cusos/` → `/cursos/` | Errata a la URL |
| `/cookies/` + `/politica-de-cookies-ue/` → **`/politica-de-cookies/`** | Duplicats |
| 5 URLs d'avís legal duplicades → **`/avis-legal/`** | Duplicats (inclosos camins antics `/groups/`, `/languages/`, `/services/`) |
| Tours per durada (`bergueda-2`, `bergueda-3`…) → **una fitxa `/tour/bergueda/`** | Decisió de Gonçal: fitxa única amb selector de durada |

## 4. Idiomes
| | Català | Castellà | Anglès |
|---|---|---|---|
| Pàgines | ✔ (22) | ✔ equivalents existents | ✔ esborranys fets amb IA, **pendents de revisió** |
| Tours | ✔ (fitxa única per destí) | A traduir (decisió: CA+ES+EN) | Esborranys fets amb IA; cal reajustar-los a fitxa única |
| Blog | ✔ (32) | només 6 entrades | `[PENDENT]` abast de traducció |
| Textos legals | ✔ | ✔ | **No** es tradueix amb IA: revisió d'un jurista |

## 5. Decisions de Gonçal (07/10/2026)  ✔
Resposta rebuda per l'usuari i enganxada a la sessió. L'usuari afegeix: **«és una web informativa; no cal poder comprar, pagar ni triar»**.

| # | Decisió |
|---|---|
| 1 | **Tours:** només **fitxa informativa** (+ formulari «Demana informació»). Sense reserva ni pagament. S'eliminen Tourmaster i el flux de reserva. |
| 2 | **Durades:** **una sola fitxa per destí amb selector de durada**. |
| 3 | **Valua Groups i I2EU:** **pàgina pròpia** cadascuna. `[PENDENT]` no hi ha text original: l'ha d'aportar Gonçal. |
| 4 | **Valua Tribes:** és una **línia nova**. Existeix `/tribes/` en català. |
| 5 | **Es migra TOT:** esborranys (28 tours, 18 entrades), pàgines de la paperera (4) i els 52 tours antics. |
| 6 | **Idiomes:** CA, ES i EN confirmats. Calen **tours i fitxes també en ES i EN**. |

**Per revisar amb Gonçal (derivat de les decisions):**
- **Les 4 pàgines de la paperera NO són còpies de Tribes** (rectifiquem): tres són còpies de la pàgina d'Attitude i una (id 14003) és un esborrany anterior de Tribes en castellà. Proposem no migrar-les com a pàgines; el text ES de Tribes es farà a partir de la versió publicada.
- **Les 10 entrades de la paperera** són versions antigues o duplicades d'entrades ja publicades: proposem no migrar-les (duplicarien contingut).
- **`Valua Services`:** **sisena línia de negoci** (Gonçal, 07/10/2026). Hi ha una pàgina en esborrany (24/09/2026) amb contingut real. `[PENDENT]` slug (`/services/`?) i relació amb la pàgina actual `/serveis/` («Serveis per a Grups»).
- **Peu de pàgina:** Gonçal confirma que **es mantenen** «Política de Turisme Responsable» i «Reclamació Gencat». `[PENDENT]` no tenen pàgina a l'inventari: cal el text o l'enllaç.
- **Àrea Client:** segons Gonçal, a WordPress no la fa servir ningú (a confirmar). Provisional: **no es porta al menú de la web nova**.
- **Tours en esborrany:** 24 tenen contingut real (esborranys de 2019 i 2023, p. ex. Sicília, Viena, Atenes) i 5 són buits o de prova. Es migren com a esborrany fins que Gonçal en confirmi la publicació.
- Els textos que parlen d'«inscripció online» (avals, serveis): `[PENDENT]` confirmar què es diu ara que la web no té flux d'inscripció ni compra.
- La traducció a ES i EN de tots els tours i del blog és feina nova (l'ES actual té pocs tours).

## 6. Tours: una fitxa per destí amb selector de durada

**Decisió de Gonçal (07/10/2026):** una sola fitxa per destí, amb **selector de durada**. Les versions per durada (p. ex. Berguedà 2/3/4/5 dies) es fusionen. URL: `/tour/{destí}/` (CA), `/es/tour/{destí}/`, `/en/tour/{destí}/`.

53 fitxes úniques. Cada fila mostra les URLs antigues que hi van a parar (redirecció 301, detall a `redirecciones.csv`).

**Cal fer en la fase de contingut:** per a cada fitxa, passar les versions per durada a dades del selector (durada, itinerari, preu si en consta). Hi ha tours amb la durada sense detectar a la fitxa (Amsterdam, Londres, Roma, Roma–Nàpols, Selva Negra, Canterbury, Curs anglès estranger, etc.): `[PENDENT]` s'ha de llegir de l'original. Praga–Berlín té dues versions amb la mateixa durada: `[PENDENT]` decidir quin contingut és vigent.

| Fitxa nova | URLs antigues que hi redirigeixen |
|---|---|
| `/tour/amsterdam/` | `/tour/amsterdam5dies/` |
| `/tour/andalusia/` | `/tour/andalusia-3/` |
| `/tour/andorra/` | `/tour/andorra6d/` |
| `/tour/anglaterra-programa-ascot/` | (sense canvi) |
| `/tour/anglaterra-programa-junior-broadstairs/` | (sense canvi) |
| `/tour/asturies/` | `/tour/asturies5d/` |
| `/tour/bergueda/` | `/tour/bergueda-2/`, `/tour/bergueda-3/`, `/tour/bergueda-4/` |
| `/tour/berlin/` | `/tour/berlin-4/` |
| `/tour/bolonya-roma/` | `/tour/bolonya-roma-2/` |
| `/tour/brighton/` | (sense canvi) |
| `/tour/brusselas/` | `/tour/brusselas5d/` |
| `/tour/canada-toronto/` | `/tour/canada-toronto-2/` |
| `/tour/cantabria/` | `/tour/cantabria-3/` |
| `/tour/canterbury-tour/` | (sense canvi) |
| `/tour/cerdanya-bergueda/` | (sense canvi) |
| `/tour/cerdanya/` | `/tour/cerdanya-2/`, `/tour/cerdanya-3/` |
| `/tour/curs-angles-estranger/` | (sense canvi) |
| `/tour/delta-de-lebre/` | (sense canvi) |
| `/tour/dublin/` | `/tour/dublin-9/` |
| `/tour/dubrovnik/` | `/tour/dubrovnik5d/` |
| `/tour/edimburg/` | `/tour/edimburg-2/` |
| `/tour/eslovenia/` | `/tour/viaje-en-grupo-a-eslovenia/`, `/tour/visita-en-grup-a-eslovenia/` |
| `/tour/euskadi-cantabria/` | (sense canvi) |
| `/tour/euskadi/` | `/tour/euskadi-2/` |
| `/tour/florencia-roma/` | `/tour/florencia-roma-5/` |
| `/tour/florencia-venecia/` | `/tour/florencia-venecia-2/` |
| `/tour/font-romeu/` | (sense canvi) |
| `/tour/irlanda-programa-junior-dublin-en-residencia/` | (sense canvi) |
| `/tour/lisboa-porto/` | (sense canvi) |
| `/tour/lisboa/` | `/tour/lisboa-3/` |
| `/tour/londres/` | `/tour/londres-2/` |
| `/tour/madrid/` | `/tour/madrid-11/` |
| `/tour/malgrat-de-mar/` | `/tour/malgrat-de-mar-2-2/`, `/tour/malgrat-de-mar-2/`, `/tour/malgrat-de-mar-3/`, `/tour/malgrat-de-mar-4/` |
| `/tour/mallorca/` | `/tour/mallorca-2/` |
| `/tour/maresme/` | (sense canvi) |
| `/tour/masella/` | `/tour/masella-2/` |
| `/tour/menorca/` | `/tour/menorca-12/`, `/tour/menorca-9/` |
| `/tour/napols/` | `/tour/napols-3/` |
| `/tour/paris/` | `/tour/paris-5/` |
| `/tour/praga-berlin/` | `/tour/praga-berlin-2/` |
| `/tour/puigcerda-esquiada-escolar/` | (sense canvi) |
| `/tour/puigcerda/` | `/tour/puigcerda-2/`, `/tour/puigcerda-3/`, `/tour/puigcerda-4/` |
| `/tour/roma-florencia/` | `/tour/roma-florencia-3/` |
| `/tour/roma-napols/` | (sense canvi) |
| `/tour/roma/` | `/tour/roma-16/`, `/tour/roma-2/` |
| `/tour/selva-negra-baviera/` | `/tour/selva-negra-baviera-3/` |
| `/tour/sud-de-franca/` | `/tour/sud-de-franca-7/`, `/tour/sud-de-franca-9/` |
| `/tour/toscana/` | `/tour/toscana-13/` |
| `/tour/valencia/` | `/tour/valencia-4/` |
| `/tour/vall-de-pineta/` | `/tour/vall-de-pineta-2/` |
| `/tour/venecia-florencia-roma/` | `/tour/venecia-florencia-roma-2/` |
| `/tour/venecia-florencia/` | `/tour/venecia-florencia-11/` |
| `/tour/venecia/` | `/tour/venecia-3/` |

**No es migren:** `/tour/aa-grecia-ok/`, `/tour/copy-of-grecia-ok/`, `/tour/copy-of-grecia-ok-2/` (pàgines de prova amb Lorem ipsum; resposta 410).

**Extret de l'XML (07/10/2026, `_fuentes/xml_extra/`):** 24 tours en esborrany amb contingut real, 18 entrades en esborrany, 10 a la paperera i 2 pàgines en esborrany. Encara no tenen fila ni URL al sitemap: cal que Gonçal digui quins es publiquen. Les durades dels tours que faltaven s'han trobat a `tours_dades_tourmaster.csv`. El recompte de «52 tours antics» de la nostra nota anterior no es pot reproduir amb l'XML: hi ha 99 publicats (la majoria de 2018), 28 esborranys i 1 pendent.

## 7. Blog
32 entrades es mantenen amb el mateix slug sota `/blog/`. No es migren: `/?p=3943` (404) i l'entrada amb emoji a la URL (no carrega). **Slugs molt llargs** a revisar: `viatges-escolars-a-catalunya-per-que-no-podem-deixar-que-desapareguin`, `valua-attitude-sota-la-lupa-de-ucla-anderson-…`.

## 8. Tres coses a tenir en compte
- **Cap URL té dades de visites** (Search Console pendent). Abans d'eliminar pàgines, cal revisar-ho amb dades.
- El **sitemap proposat** (`sitemap-nuevo.xml`) té 245 URLs, amb etiquetes d'idioma. És per revisar, no per publicar.
- Les traduccions a l'anglès són esborranys; cap URL `/en/` s'ha de publicar sense revisió.
