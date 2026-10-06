# La nova web de Valua Travel — el projecte explicat de forma simple

*Última actualització: 06/10/2026. Estat: esborrany, pendent de l'OK escrit de Gonçal en algunes decisions.*

## Què fem i per què
La web actual (`valuatravel.com`) està feta amb **WordPress** i un tema antic (TravelTour). Volem passar-la a una web nova feta amb **Next.js (React)**, més ràpida, més fàcil de mantenir i pensada per millorar la visibilitat a Google.

**Regla d'or:** no es perd res. Primer es guarda tot, després es construeix, i només al final es canvia la web antiga per la nova.

## Què és Valua Travel
Agència de viatges especialitzada en **viatges per a grups escolars**, estades lingüístiques i viatges d'aventura. El públic són centres educatius, professorat i famílies. Té diverses línies de negoci (Valua Groups, Valua Languages, Attitude, I2EU…).

## Idiomes
La web nova serà en **català, castellà i anglès**.
- Ara mateix la web té català i castellà (el castellà és més petit del que sembla).
- **L'anglès és contingut nou**: hi ha esborranys fets amb IA que **s'han de revisar** abans de publicar-los.
- Els textos legals no s'han de traduir amb IA: els ha de revisar un jurista.

## Com anem: les fases
| Fase | Què és | Estat |
|---|---|---|
| 0–1 | Accessos i programes | Fet |
| **2** | **Còpies de seguretat i exportació de tot el contingut** | **Fet** |
| **3** | **Inventari SEO: totes les URLs, errors i metadades** | **Quasi fet.** Falten les dades de visites (Google Search Console, esperant el DNS) |
| 4 | Repositori de codi a GitHub | **En curs.** Falta que existeixi `main` i el permís d'escriptura |
| 5 | Contingut classificat, mapa de la web nova i redireccions | Pendent |
| 6 | Disseny | Pendent |
| 7 | Construcció de la web | Pendent (hi ha un esquelet inicial) |
| 8–9 | Proves a Vercel i pas a producció | Pendent |
| 10 | Seguiment durant 4 setmanes | Pendent |

Abans de passar d'una fase a la següent hi ha un **punt de parada**: Gonçal ha de donar l'OK per escrit.

## On és cada cosa
Tot és dins la carpeta de SharePoint `TI / WEB / NOVA WEB _ WP A REACT_SEPT2026`.

| Carpeta | Què hi ha |
|---|---|
| `backups_wordpress_2026-10-05/` | Còpia de seguretat completa de WordPress (base de dades, plugins, temes, imatges) |
| `wp-content.zip` | Segona còpia, feta per FTP |
| `SEO_yoast/` | Configuració de Yoast i un CSV amb títols i meta descripcions |
| `SEO_crawl/` | Inventari de les 271 URLs de la web actual |
| `INVENTARI_PLUGINS/` | Llista dels 35 plugins i què cal substituir |
| `captures-formularis/` | Especificació dels 4 formularis de contacte |
| `sitemap/` | Arbre del sitemap fet amb Claude |
| `valua-web/` | **El codi de la web nova** (Next.js) i la documentació |
| `valua-web/_fuentes/` | Material de treball (text original, 93 traduccions a l'anglès, 509 imatges, redireccions). **No es puja mai a GitHub** |

## El que hem descobert de la web actual
- **128 tours** (viatges), gestionats pel plugin Tourmaster. És la part més gran.
- **60 % de les pàgines no tenen meta descripció** i hi ha 31 títols duplicats.
- **Totes les imatges tenen el text alternatiu buit** (dolent per a SEO i accessibilitat).
- 8 pàgines donen error 404.
- Hi ha errors de contingut: meta descripcions de Lisboa copiades a altres tours, preus ambigus, tours en castellà dins la web catalana, dos tours d'Eslovènia duplicats…
- El plugin de redireccions té un **bucle** (una URL que redirigeix cap a ella mateixa).
- Google Analytics no funcionava. Search Console no tenia la propietat creada.

## Decisions que ha de prendre Gonçal
1. **Els 128 tours:** reserva en línia o només fitxa informativa?
2. **Idiomes** CA / ES / EN: confirmar per escrit.
3. **Tours i entrades en esborrany o a la paperera:** es migren o no?
4. **Anglès:** qui el revisa, i es publica tot de cop o per fases?
5. **Formularis:** el desplegable d'assumpte (només existeix en castellà) s'afegeix al català?

## Normes de treball
- **No s'esborra ni es mou res a SharePoint.** Mai.
- **No s'inventa contingut.** Tot text surt de la web actual o l'aprova Gonçal.
- **No es guarden DNI ni dades personals** al projecte.
- **No es demanen ni es comparteixen contrasenyes.**
- El codi a GitHub es treballa en una **branca pròpia** (`xinhao`) i l'equip decideix quan fer el *merge* a `main`.
- Les fonts (`_fuentes/`) i les còpies de seguretat es queden en local i a SharePoint, no a GitHub.

## Què fa falta ara
- Que a GitHub existeixi `main` i es doni permís d'escriptura.
- El correu d'empresa per als commits.
- Verificar el DNS per activar Search Console i exportar les visites.
- L'OK escrit de Gonçal a les fases tancades.
