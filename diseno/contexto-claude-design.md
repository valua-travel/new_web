# Brief per a Claude Design — web nova de Valua Travel (ESBORRANY)

*07/10/2026. Elaborat a partir de `CLAUDE.md`, `classificacio.xlsx`, `arquitectura/mapa-web.md` i els textos de `_fuentes/ca/`. Incorpora les decisions de Gonçal del 07/10/2026 (§0). **Falta l'OK final dels entregables.** Tot el text surt de la web actual. Res d'inventat: el que falta és `[PENDENT]`.*

## 0. Decisions de Gonçal (07/10/2026) — ja resoltes
1. **És una web informativa.** No es pot comprar, pagar ni triar/reservar en línia.
2. **Tours:** només **fitxa informativa** amb formulari «Demana informació». Sense reserva.
3. **Durades:** **una sola fitxa per destí amb selector de durada** (p. ex. Berguedà 2/3/4/5 dies = una fitxa).
4. **Valua Groups i I2EU:** **pàgina pròpia** cadascuna. `[PENDENT]` no hi ha text original: l'ha d'aportar Gonçal; no s'ha d'inventar.
5. **Valua Tribes:** **línia nova** (existeix `/tribes/` en català).
6. **Es migra tot:** esborranys, paperera i els 52 tours antics.
7. **Idiomes:** català, castellà i anglès. Els tours i la resta de pàgines han d'existir en els tres.

Encara oberts (no bloquegen l'estructura): xifres contradictòries (§2), to de veu i identitat visual (§3, §8), textos de Groups, I2EU, Tribes en ES/EN.
Els textos en anglès són esborranys fets amb IA i els legals els revisa un jurista: no són contingut final.

## 1. Qui és Valua Travel
Agència de viatges amb seu a Mataró (Barcelona) i delegació a València, especialitzada en **viatges per a grups escolars**, estades lingüístiques i viatges d'aventura. Públic: **centres educatius, professorat i famílies** (i, en algunes línies, esportistes, organitzadors i adults en grup).

Línies de negoci: **Valua Groups, Valua Languages, Attitude, I2EU, Valua Tribes** (línia nova: viatges per a col·lectius, grups o comunitats que comparteixen una passió) **i Valua Services** (sisena línia, confirmat per Gonçal 07/10/2026). Cadascuna tindrà pàgina pròpia. Avui només tenen pàgina Languages, Attitude i Tribes (`/tribes/`, publicada el 02/10/2026). `[PENDENT]` Valua Groups i I2EU: no hi ha text original; l'ha d'aportar Gonçal i no s'ha d'inventar. **Valua Services** té una pàgina en esborrany (serveis turístics per a grups i empreses: bitllets d'avió, allotjaments, transport); `[PENDENT]` slug i relació amb `/serveis/`.

## 2. Valors, xifres i avals (tal com diu la web actual)
Valors que apareixen a la web: **Proximitat, Innovació, Rigor** (lemes: «Familiars, experts, professionals», «T'ho fem fàcil»).

Avals que es repeteixen a la web actual: assistència 24/7 durant el viatge; resposta en 24h; inscripció online de tots els passatgers; contractació directa a proveïdors; treball amb les principals asseguradores europees; compliment de la llei de protecció de dades; dossier extens del viatge; preus ajustats; pressupost en 24h. Estades lingüístiques: avalades per Quality English.

**Xifres que es contradiuen a la web actual** `[PENDENT]` (no s'han de posar al disseny fins que Gonçal les aclareixi):

| Dada | Pàgines | Valors que apareixen |
|---|---|---|
| Anys d'experiència | Qui som / Serveis | «més de 20 anys» / «més de 15 anys» |
| Alumnes o passatgers gestionats | Qui som / Serveis | «més de 80.000 alumnes» / «més de 50.000 passatgers» |
| Equip | Languages / Serveis / Qui som | «21 professionals» / «10 professionals» / 19 fitxes de persona |
| Altres | Serveis / Valua Services (esborrany) | 7000 passatgers, 98 % satisfets, ~5.500 proveïdors, +3.000 bitllets d'avió l'any, 230 grups, 176 empreses de transport |
| Comptadors de la portada | Inici / Qui som | El text original només conserva «0Mil», «0 %»: s'animen amb JS i els valors es van perdre en l'extracció |

## 3. Tono i personalitat de marca
Segons el **Manual d'Identitat de Marca** (Nóctope, juliol 2017): el logotip busca transmetre «aventura i descobriment». Els conceptes que defineixen la marca són vuit adjectius: **Apassionats, Propers, Compromesos, Curiosos, Vitals, Racionals, Oberts i Resolutius.**
Observat als textos actuals de la web: tracte proper i directe (tu), frases curtes, lemes tipus «T'ho fem fàcil», «Nosaltres gestionem, tu ensenyes». `[PENDENT]` Gonçal ha de confirmar que el to continua sent aquest.

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
| **Valua Groups** | Pàgina pròpia | `[PENDENT]` text de Gonçal |
| **Valua Services** | Sisena línia: serveis turístics independents per a grups i empreses | Esborrany a `_fuentes/xml_extra/pagines_esborrany_paperera/`: bitllets d'avió, allotjaments, transport, trasllats; botó «Demana pressupost». `[PENDENT]` slug i relació amb `/serveis/` |
| **I2EU** | Pàgina pròpia | `[PENDENT]` text de Gonçal |
| **Valua Tribes** | Línia de viatges per a col·lectius, grups o comunitats que comparteixen una passió: captar creadors, clubs, experts, associacions i comunitats | Text a `_fuentes/ca/Pagines__tribes.md`: «Viatges creats per compartir», 9 passos de la idea a l'experiència (comunitat, disseny, gestió integral, personalització, suport, legalitat, inscripcions i pagaments, experiència, benefici), formulari amb nom, email, telèfon i missatge. Només en català |

### Elements globals a decidir `[PENDENT]`
Apareixen a la web actual a totes les pàgines (detall a `_fuentes/ca/Pagines__tribes.md`):
- **Menú:** Nosaltres, Blog, Serveis, Any escolar, Programes d'estiu, Contacte, **Àrea client**, selector d'idioma. L'Àrea Client era una plataforma d'accés online al viatge (hi ha un tutorial en esborrany). **Gonçal creu que ningú l'usa a WordPress:** provisionalment no es porta al menú nou `[PENDENT]` confirmar.
- **Peu:** «El nostre compromís» (textos de subvenció FSE i LABORA), «Grup Valua» (només Travel, Languages, Attitude i Services: sense Groups, I2EU ni Tribes), dades de contacte i enllaços legals, entre ells **Política de Turisme Responsable** i **Reclamació Gencat**: **Gonçal confirma que es mantenen**, però no tenen pàgina a l'inventari `[PENDENT]` text o enllaç. Copyright de 2024.

## 6. Idiomes
Català (per defecte, a l'arrel), castellà (`/es/`) i anglès (`/en/`): **confirmat per Gonçal**. El disseny ha de preveure el selector d'idioma i textos més llargs en castellà i anglès. Tours, blog i pàgines noves han de poder existir en els tres.

## 7. Restriccions
- **Accessible** (contrast, teclat, text alternatiu: avui totes les imatges tenen l'alt buit).
- **Responsive** (requisit de la hoja de ruta).
- **Ràpida** (requisit de la hoja de ruta). `[PENDENT]` no s'ha mesurat la velocitat de la web actual.
- **Sense dependre de Revolution Slider, WPML ni Tourmaster**: són plugins de la web actual (alguns desactualitzats) que no s'han de portar. `[PENDENT]` confirmar-ho amb Gonçal.
- Públic mixt: centres educatius, professorat i famílies (segons `CLAUDE.md`).

## 8. Identitat visual (del Manual d'Identitat de Marca, 2017)
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
- `[PENDENT]` Referències de disseny que li agraden o no a Gonçal.

## 9. Pendents (resum)
**Resolt el 07/10/2026:** reserva de tours (no), durades (selector), Groups/I2EU (pàgina pròpia), Tribes (línia nova), què es migra (tot), idiomes (CA/ES/EN).

**Pendent de Gonçal**
1. Text de Valua Groups i I2EU, i de Tribes en ES/EN.
2. Xifres contradictòries (§2).
3. To de veu (§3) i identitat visual (§8).
4. Què es diu de la «inscripció online» ara que la web és només informativa; confirmar que l'Àrea Client no s'usa.
5. Valua Services: slug i relació amb `/serveis/`. Text o enllaç de Turisme Responsable i Reclamació Gencat. (Les 4 pàgines de paperera «Valua Tribes» són còpies d'Attitude i un esborrany ES antic de Tribes: no es migren.)

**Feina nostra (sense decisions)**
6. **Fet:** extracció de l'XML a `_fuentes/xml_extra/` (24 tours en esborrany amb contingut, 18 entrades en esborrany, 10 de paperera, pàgines). Falta que Gonçal confirmi quins es publiquen.
7. Passar les versions per durada a dades del selector (les durades dels 13 tours que faltaven **ja s'han trobat** a `tours_dades_tourmaster.csv`); Praga–Berlín (dues versions).
8. Traduccions ES i EN de tots els tours i del blog; revisió dels esborranys EN; revisió legal pel jurista.
9. Alt de les imatges i quines es reutilitzen.
10. Meta descripcions (156 pàgines no en tenen) i dades de Search Console per saber quines pàgines porten tràfic.
11. Errates dels textos originals (p. ex. Tribes: «¿Vols saber més?», «y remuneració», «Seguretat I legalitat»).
