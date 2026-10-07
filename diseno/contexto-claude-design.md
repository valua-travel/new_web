# Brief per a Claude Design — web nova de Valua Travel (ESBORRANY)

*07/10/2026. Elaborat a partir de `CLAUDE.md`, `classificacio.xlsx`, `arquitectura/mapa-web.md` i els textos de `_fuentes/ca/`. Incorpora les decisions i respostes de Gonçal del 07/10/2026 (§0). **Falta l'OK final dels entregables.** Tot el text surt de la web actual. Res d'inventat: el que falta és `[PENDENT]`.*

## 0. Decisions de Gonçal (07/10/2026) — ja resoltes
**Primera tanda**
1. **És una web informativa.** No es pot comprar, pagar ni triar/reservar en línia.
2. **Tours:** només **fitxa informativa** amb formulari «Demana informació». Sense reserva.
3. **Durades:** **una sola fitxa per destí amb selector de durada** (p. ex. Berguedà 2/3/4/5 dies = una fitxa).
4. **Valua Groups i I2EU:** pàgina pròpia cadascuna, però **en STANDBY** (no hi ha text; no s'han de dissenyar ara ni s'ha d'inventar res).
5. **Valua Tribes:** línia nova (existeix `/tribes/` en català).
6. **Idiomes:** català, castellà i anglès. Els tours i la resta de pàgines han d'existir en els tres.

**Segona tanda (respostes a les preguntes concretes)**
7. **Valua Services** és la **sisena línia**, i **és la mateixa pàgina que `/serveis/`** («Serveis per a Grups»): no n'hi ha dues.
8. **Xifres confirmades:** més de **20 anys** d'experiència; més de **30.000 persones l'any**; equip de **20 persones** repartides en equips; les xifres de Valua Services (5.500 proveïdors, +3.000 bitllets d'avió l'any, 230 grups, 176 empreses de transport) són **actuals**.
9. **Esborranys de WordPress (24 tours i 18 entrades): STANDBY.** No es publiquen ni es porten a la web nova per ara. Les **10 entrades de la paperera es deixen fora.**
10. **Àrea Client:** és una plataforma **externa**; de moment **no es crea**, però **l'arquitectura ha de quedar preparada** per si cal afegir-la.
11. **Peu de pàgina** (Política de Turisme Responsable, Reclamació Gencat, «El nostre compromís»): **STANDBY**; Gonçal passarà els textos més endavant. L'espai ha de quedar previst.
12. **To i estil:** to **proper (tutejant)**; l'estil (colors, tipografies…) **ha de ser el mateix de la web actual de WordPress** (§8).

Els textos en anglès són esborranys fets amb IA i els legals els revisa un jurista: no són contingut final.

## 1. Qui és Valua Travel
Agència de viatges amb seu a Mataró (Barcelona) i delegació a València, especialitzada en **viatges per a grups escolars**, estades lingüístiques i viatges d'aventura. Públic: **centres educatius, professorat i famílies** (i, en algunes línies, esportistes, organitzadors i adults en grup).

Línies de negoci: **Valua Groups, Valua Languages, Attitude, I2EU, Valua Tribes** (línia nova: viatges per a col·lectius, grups o comunitats que comparteixen una passió) **i Valua Services** (sisena línia, que correspon a la pàgina actual `/serveis/`). Avui tenen pàgina Languages, Attitude, Tribes i Serveis. **Groups i I2EU** tindran pàgina pròpia però estan **en standby**: no hi ha text original i no s'ha d'inventar.

## 2. Valors, xifres i avals
Valors que apareixen a la web: **Proximitat, Innovació, Rigor** (lemes: «Familiars, experts, professionals», «T'ho fem fàcil»).

Avals que es repeteixen a la web actual: assistència 24/7 durant el viatge; resposta en 24h; inscripció online de tots els passatgers; contractació directa a proveïdors; treball amb les principals asseguradores europees; compliment de la llei de protecció de dades; dossier extens del viatge; preus ajustats; pressupost en 24h. Estades lingüístiques: avalades per Quality English.

**Xifres confirmades per Gonçal (07/10/2026)**

| Dada | Valor vigent |
|---|---|
| Anys d'experiència | **Més de 20 anys** |
| Persones que viatgen | **Més de 30.000 l'any** |
| Equip | **20 persones**, repartides en diferents equips |
| Proveïdors | 5.500 |
| Bitllets d'avió | +3.000 l'any |
| Grups | 230 |
| Empreses de transport | 176 |

Aquestes xifres **substitueixen** les de la web actual que es contradeien (15 anys, 50.000 / 80.000, 10 / 21 professionals). `[PENDENT]` Altres xifres que **no** estan confirmades i no s'han d'usar: 7.000 passatgers, 98 % de satisfets (Serveis) i el brochure de Valua Tribes (+20.000 viatgers l'any, 350 grups l'any, 4,7★ en +300 ressenyes de Google, 18 persones) que no coincideix amb les anteriors. Els comptadors animats de la portada només conservaven «0Mil», «0 %»: cal omplir-los amb les xifres confirmades.

## 3. Tono i personalitat de marca
Segons el **Manual d'Identitat de Marca** (Nóctope, juliol 2017): el logotip busca transmetre «aventura i descobriment». Els conceptes que defineixen la marca són vuit adjectius: **Apassionats, Propers, Compromesos, Curiosos, Vitals, Racionals, Oberts i Resolutius.**
Observat als textos actuals de la web: tracte proper i directe (tu), frases curtes, lemes tipus «T'ho fem fàcil», «Nosaltres gestionem, tu ensenyes». **Confirmat per Gonçal (07/10/2026):** to proper, tutejant.

## 4. Objectius del visitant
Accions principals que la web actual ja ofereix:
1. **Demanar pressupost** («El teu pressupost en 24h», «Sol·licitar pressupost»).
2. **Contactar** (telèfon +34 937 551 607, `hola@valuatravel.com` per a inscripcions, `info@valuatravel.com` per a consultes).
3. **Descarregar un PDF o catàleg** (viatges fi de curs, catàleg Languages).
4. **Veure viatges/programes** (cercador de tours i fitxa de tour amb selector de durada). Només informatiu, sense reserva ni pagament.
5. **Demanar informació** des de cada fitxa. (La web actual esmenta «inscripció online» com a servei als passatgers; `[PENDENT]` confirmar què es diu ara que la web no té flux d'inscripció.)
6. Llegir testimonis i blog (confiança).

Formularis existents: 4 de Contact Form 7 (especificació a `_fuentes/formularis_especificacio.md`).

## 5. Pàgines a dissenyar i què diu cada una
Estructura completa a `arquitectura/mapa-web.md`. Resum:

| Pàgina | Propòsit | Contingut real (resum) |
|---|---|---|
| **Portada** | Presentar les línies i portar a pressupost | 4 portes: Viatges fi de curs (11–18 anys), Setmanes d'activitats (4–18), Estades lingüístiques (+11), Any escolar (12+); «Perquè treballar plegats», xifres `[PENDENT]`, pressupost en 24h, opinions, valors, blog, contacte |
| **Qui som** | Confiança | «Què ens mou», avals, valors, equip (nom i càrrec de cada persona; ara fitxes separades que es fusionen aquí) |
| **Viatges fi de curs** | Convertir professorat | «Nosaltres gestionem, tu ensenyes»; comunicació amb famílies; un únic interlocutor; serveis gestionats (allotjament, transport, assegurança, visites, àpats, monitors); PDF |
| **Sortides d'1 dia** | Grups de 4 a 18 anys | Platja i mar, muntanya i neu, parcs temàtics, indoor, cultural |
| **Setmanes d'aventura** (+ blanca, verda, blava) | Colònies escolars | Blanca: neu, esquí, snowboard, raquetes (Cerdanya). Verda: muntanya (Alt Berguedà, Cerdanya). Blava: mar, Malgrat de Mar/Maresme. Monitors 24h, assegurança inclosa |
| **Valua Languages** | Estades lingüístiques | Summer camps, programes lingüístics (anglès, francès, alemany), any escolar; avals; catàleg PDF; testimonis |
| **Summer camps / Ministays / Any escolar** | Detall de programes | Summer camps: a partir d'11 anys, allotjament, àpats, classes, activitats, vols, monitor. Ministays: grups escolars, mínim 5 i màxim 15 dies, famílies natives. Any escolar: trimestre o any, assessorament a la família |
| **Attitude** | Esdeveniments esportius | Gestió integral de serveis turístics per a curses (allotjament, vols, transport, assegurances); casos d'èxit; botiga online `[PENDENT]` enllaç |
| **Serveis** | Estudiants i adults | Viatges per a estudiants i serveis per a grups d'adults |
| **Catàleg / Tours** | Cercar i informar-se | Cercador de tours; **una fitxa per destí amb selector de durada** (53 fitxes), amb botó «Demana informació». Preus i dates actuals del catàleg són de l'estiu 2026: `[PENDENT]` actualitzar |
| **Destinacions, Cursos, Allotjament** | Informació de suport | 7 destinacions (Anglaterra, Irlanda, Canadà…), 1 curs, 2 tipus d'allotjament |
| **Testimonis** | Confiança | Opinions de centres; enllaç a ressenyes de Google |
| **Blog** | SEO i confiança | 32 entrades CA; `[PENDENT]` abast ES/EN |
| **Contacte** | Convertir | Telèfon, correus, adreça a Mataró, delegació de València, formulari |
| **Legals** | Obligació | Avís legal, condicions de viatge, cookies, confirmació d'inscripció (noindex) |
| **Valua Groups** `STANDBY` | Pàgina pròpia | Sense text original: no es dissenya ara |
| **Valua Services = Serveis** | Serveis turístics per a grups: estudiants i adults (és la pàgina `/serveis/`) | Text actual de `/serveis/` més l'esborrany de Valua Services (`_fuentes/xml_extra/pagines_esborrany_paperera/`): bitllets d'avió, allotjaments, transport, trasllats; botó «Demana pressupost». `[PENDENT]` quina de les dues redaccions preval |
| **I2EU** `STANDBY` | Pàgina pròpia | Sense text original: no es dissenya ara (hi ha material antic de 2015–2017 a `TI/WEB/I2EU/` per a quan es reactivi) |
| **Valua Tribes** | Línia de viatges per a col·lectius, grups o comunitats que comparteixen una passió: captar creadors, clubs, experts, associacions i comunitats | Text a `_fuentes/ca/Pagines__tribes.md`: «Viatges creats per compartir», 9 passos de la idea a l'experiència (comunitat, disseny, gestió integral, personalització, suport, legalitat, inscripcions i pagaments, experiència, benefici), formulari amb nom, email, telèfon i missatge. Només en català |

### Elements globals
Apareixen a la web actual a totes les pàgines (detall a `_fuentes/ca/Pagines__tribes.md`):
- **Menú:** Nosaltres, Blog, Serveis, Any escolar, Programes d'estiu, Contacte, selector d'idioma. **Àrea Client:** és una plataforma **externa**; no es crea ara, però el menú i les rutes han de **deixar un lloc previst** per a un enllaç futur (decisió de Gonçal).
- **Peu:** dades de contacte i enllaços legals. En **standby** (Gonçal passarà els textos): «Política de Turisme Responsable», «Reclamació Gencat» i «El nostre compromís» (subvencions FSE i LABORA). L'espai ha de quedar previst. «Grup Valua» a la web actual només llista Travel, Languages, Attitude i Services (sense Groups, I2EU ni Tribes) `[PENDENT]`. Copyright de 2024: actualitzar.

## 6. Idiomes
Català (per defecte, a l'arrel), castellà (`/es/`) i anglès (`/en/`): **confirmat per Gonçal**. El disseny ha de preveure el selector d'idioma i textos més llargs en castellà i anglès. Tours, blog i pàgines noves han de poder existir en els tres.

## 7. Restriccions
- **Accessible** (contrast, teclat, text alternatiu: avui totes les imatges tenen l'alt buit).
- **Responsive** (requisit de la hoja de ruta).
- **Ràpida** (requisit de la hoja de ruta). `[PENDENT]` no s'ha mesurat la velocitat de la web actual.
- **Sense dependre de Revolution Slider, WPML ni Tourmaster**: són plugins de la web actual (alguns desactualitzats) que no s'han de portar. `[PENDENT]` confirmar-ho amb Gonçal.
- Públic mixt: centres educatius, professorat i famílies (segons `CLAUDE.md`).

## 8. Identitat visual
**Decisió de Gonçal (07/10/2026): l'estil de la web nova (colors, tipografies, etc.) ha de ser el mateix que el de la web actual de WordPress, i aquesta és també la referència d'inspiració (no calen altres webs).** El manual de 2017 és referència secundària. Aquests valors surten del CSS de la web en producció (tema TravelTour amb personalització de Valua):

| Element | Web actual |
|---|---|
| Tipografia principal (text, menú, formularis) | **Montserrat** |
| Tipografia de títols en blocs de la portada | **Oswald** |
| Altres | Roboto (sliders), Poppins (text del peu) |
| Mida de text base | 14 px |
| Color d'accent principal | `#D93D67` (rosa/vermell); `#C1495C` a les cintes dels tours |
| Blau d'enllaços i elements | `#468AE7` / `#4F99E4` / `#5990E0` |
| Grisos de text | `#565556`, `#424242`, `#333333`, `#3A3A3A`; fons clar `#F3F3F3`; blanc i negre |

`[PENDENT]` Gonçal ha de confirmar que aquesta paleta i aquestes fonts són les que vol mantenir. **Els colors del manual de 2017 (verd, blau, vermell, vermell taronja, llima) i la tipografia Calibri no coincideixen amb la web actual**: s'han de mantenir només per als logotips de cada línia, no com a paleta de la web, tret que Gonçal digui el contrari.

Font: `LOGOS & SEGELL/Manual_Identidad_LOGOS.pdf` (versió completa, amb colors) i `MKG & COMUNICACIÓ/ESTRATEGIA DE MARCA/ESTRATEGIA DE MARCA/VALUA_Manual_Identidad.pdf` (versió una mica anterior, sense especificacions de color). **Són de juliol de 2017: cal confirmar que continuen vigents.**

**Logotip**
- Creat a partir de formes tipogràfiques pròpies; la «V» té un element superior que recorda un ocell alçant el vol. Existeix com a **isotip** (la «V» sola, només en usos limitats) i com a logotip + «travel» (horitzontal o vertical).
- El logotip només pot anar en **blanc o negre** (positiu o negatiu, mai barrejats), mai en cap altre color, ni degradats, ni amb vora. Zona d'exclusió: l'alçada de les lletres.
- **Mida mínima web: 115 px d'ample** (3 cm en paper).
- Sub-marques amb logotip propi (en tipografia Travel): **Attitude, Groups, Languages**. Hi ha també fitxers de Services, Incoming i Tribes (2026) que el manual no recull.
- Fitxers: PNG a `LOGOS & SEGELL/FORMATO_NORMAL/` i vectorials EPS a `MKG & COMUNICACIÓ/LOGOS-TIPOGRFIA_VALUA/FORMATO_PROGRAMING/`.

**Colors** (secundaris: només per a bases de color, icones i il·lustracions, mai pel logotip)

| Color | HTML | RGB | Pantone |
|---|---|---|---|
| Verd | `#00AE65` | 0 174 101 | 3405 |
| Blau | `#0099CC` | 0 153 204 | 639 |
| Vermell | `#EA2839` (RGB indica 205 32 44 = `#CD202C`: el manual es contradiu) | 205 32 44 | 1795 |
| Vermell taronja | `#F7403A` | 247 64 58 | Warm Red |
| Llima | `#DFDF00` | 223 223 0 | 396 |

Colors principals de la marca: **blanc i negre**. Cada sub-marca té una parella: Attitude (aventura, natura, passió, contrastos), Groups (càlids, propers, alegres) i Languages (món anglosaxó, tranquil·litat, frescor). `[PENDENT]` el manual no deixa clar en text quina parella de colors correspon a cada una; pels noms dels fitxers de logo serien Attitude = verd, Groups = vermell, Languages = blau.

**Tipografies**
- **Travel** (corporativa principal): només per als logotips de les àrees i conceptes essencials. No és una font per al text.
- **FF Mark** (secundària): text general, sobretot en suports impresos.
- **Calibri** (de sistema): s'usa quan el suport digital no permet FF Mark, **com a web, PowerPoint i documents**. Per a la web, el manual indica Calibri. `[PENDENT]` FF Mark és una font de pagament: si es vol a la web, cal llicència.

**Fotografia i imatge:** naturals i creïbles, no forçades ni «de revista»; punt de vista de la persona (evitar plànols aeris irreals). Attitude: aventura, descobriment, amistat, curiositat, desconnexió de la rutina, rebel·lia, flexibilitat. Groups: humor, diversió, llibertat, independència, protecció, amistat, importància del grup, primeres vegades. Languages: responsabilitat, primers passos cap a la maduresa, valor de l'esforç, conèixer gent nova, seguretat, independència, il·lusió pel futur.

**Pendent / a tenir en compte**
- El manual és de 2017 i no inclou Services, Tribes, I2EU ni els logos del 2024 (`VALUA_Logo_1.png`, `VALUA_Logo_2.png`). A `VALUA TRIBES/` hi ha una carpeta d'identitat de marca (IA) i logotip propis.
- El manual dóna l'adreça antiga (Carrer Sant Josep 4); la web actual diu Muralla de Sant Llorenç 37.
- Per a Claude Design cal el logotip **en vectorial (SVG/PDF) o PNG gran amb transparència**; hi ha EPS i PNG petits (el de GitHub, `valua-travel-logo.jpg`, és només de 3,7 KB). `[PENDENT]` demanar a Màrqueting un SVG.
- **Referència de disseny: la pròpia web actual de WordPress** (valuatravel.com). No calen altres webs d'inspiració (Gonçal, 07/10/2026): la web nova s'ha d'inspirar en l'estructura, l'estil i el to de l'actual, millorant-ne la usabilitat i el rendiment.

## 9. Pendents (resum)
**Resolt el 07/10/2026 (dues tandes):** reserva de tours (no), durades (selector), Tribes i Services (línies), Services = `/serveis/`, idiomes (CA/ES/EN), xifres, esborranys (standby), paperera (fora), Àrea Client (externa, arquitectura preparada), to (proper) i estil (el de la web actual).

**En STANDBY (a l'espera de textos de Gonçal)**
1. Pàgines de **Valua Groups** i **I2EU**.
2. Peu de pàgina: Política de Turisme Responsable, Reclamació Gencat, «El nostre compromís».
3. **24 tours i 18 entrades** en esborrany.

**Pendent de confirmar**
4. Que la paleta i les fonts de la web actual (§8) són les que Gonçal vol mantenir.
5. Quina redacció preval a `/serveis/`: el text actual o l'esborrany de Valua Services.
6. ~~Referències de disseny~~: **no calen**; la referència és la web actual de WordPress.
7. Un logotip en vectorial (SVG/PDF) o PNG gran amb transparència; el de GitHub és un JPG de 3,7 KB.
8. Text de Tribes en ES i EN, amb les errates de l'original corregides.

**Feina nostra (sense decisions)**
9. Passar les versions per durada a dades del selector de tours.
10. Traduccions ES i EN de tours i blog; revisió dels esborranys EN; revisió legal pel jurista.
11. Alt de les imatges i quines es reutilitzen.
12. Meta descripcions (156 pàgines no en tenen) i dades de Search Console per saber quines pàgines porten tràfic.
13. Omplir els comptadors de la portada amb les xifres confirmades (§2).
