# TSDP2 · Entrega 1 · Tasca 5 — Arquitectura de la informació

**Projectes:** Rocanolich · Estètica i perruqueria · Graduació  
**Criteri d'avaluació:** 7.1.3 — Arquitectura de la informació i mapes del lloc  
**Modalitat:** treball de definició en grup; documentació i justificació individual  
**Lliurament:** incorporar l'apartat **5. Arquitectura de la informació** al dossier individual de Google Drive de l'Entrega 1.

## 1. Què aprendrem?

Abans de dissenyar pantalles, cal decidir **quines pàgines o vistes necessita el producte, què conté cadascuna i com s'organitzen**. Aquesta feina s'anomena _arquitectura de la informació_.

> **Pregunta clau:** Si una persona arriba a la nostra web, sabrà on trobar allò que necessita?

**Important:** una **funcionalitat** és una cosa que l'usuari pot fer (_reservar una pista_); una **pàgina o vista** és un espai de la interfície on pot fer una o diverses accions (_Calendari de disponibilitat_). No cal crear una pàgina nova per cada botó ni cada funcionalitat.

El resultat d'aquesta tasca serà un **inventari de pàgines** i un **mapa del lloc (sitemap)**. Encara **no** cal dibuixar l'aspecte visual de les pantalles ni elaborar el diagrama de decisions d'una reserva: això es treballarà en tasques posteriors.

## 2. Materials i eines

- **Per pensar i ordenar:** pòstits, targetes de paper o una pissarra compartida.
- **Per registrar les decisions:** taules en Google Docs o Google Sheets.
- **Per dibuixar el mapa del lloc:** [diagrams.net](https://app.diagrams.net/), Figma/FigJam o una eina equivalent.
- **Punt de partida obligatori:** les cinc funcionalitats seleccionades per a l'**MVP** i les històries d'usuari de la Tasca 4.

## 3. Procediment pas a pas

### Pas 1 — Recuperar les necessitats i funcionalitats

En grup, reviseu:

1. El vostre **User Persona** i què necessita aconseguir.
2. Les **cinc funcionalitats de l'MVP**.
3. Les **històries d'usuari**, incloent el **frontoffice** i el **backoffice**.

Per cada funcionalitat, completeu aquesta frase: **«Perquè l'usuari pugui [acció], ha de trobar [informació / control / resultat]».**

Exemple: Perquè l'usuari pugui consultar les pistes disponibles, ha de trobar un calendari on seleccionar el dia i veure les pistes i els horaris lliures.

### Pas 2 — Fer el llistat inicial de pàgines i vistes

Per cada funcionalitat, pregunteu-vos:

- **On comença?** Cal una pàgina d'inici, una llista o un panell?
- **Quina informació necessita veure?** Calendari, preus, detalls, inscripcions, butaques…?
- **Què ha de poder fer?** Cercar, filtrar, seleccionar, omplir un formulari, confirmar…?
- **Què veu en acabar?** Resum, confirmació, missatge d'error…?
- **Qui ho fa?** Un visitant/client (**frontoffice**) o un gestor (**backoffice**)?
- **Ja existeix una altra pàgina on això encaixa?** Eviteu duplicats innecessaris.

Escriviu **una pàgina o vista per targeta**. En aquesta fase podeu proposar-ne més de les necessàries: després les agrupareu.

**Plantilla A — De funcionalitats a pàgines**

| Funcionalitat de l'MVP | Qui la fa? (rol)         | Què necessita veure o fer? | Pàgina o vista candidata |
| ---------------------- | ------------------------ | -------------------------- | ------------------------ |
| [Funcionalitat 1]      | [Client / administrador] | [Informació i accions]     | [Nom de pàgina]          |
| [Funcionalitat 2]      |                          |                            |                          |
| [Funcionalitat 3]      |                          |                            |                          |
| [Funcionalitat 4]      |                          |                            |                          |
| [Funcionalitat 5]      |                          |                            |                          |

> Una mateixa pàgina pot donar resposta a diverses funcionalitats. Una funcionalitat també pot necessitar diverses vistes.

### Pas 3 — Agrupar les targetes amb _card sorting_

Reuniu totes les pàgines candidates sobre una taula o pissarra. Agrupeu-les **segons el que les persones esperen trobar junt**, no segons la distribució del codi.

1. Separeu primer **frontoffice** (web pública o d'usuari) i **backoffice** (gestió interna).
2. Dins de cada zona, poseu juntes les pàgines amb una mateixa finalitat: _consultar_, _reservar_, _gestionar_, _compte_, etc.
3. Poseu un **nom clar a cada grup**. Prioritzeu paraules que l'usuari entendria.
4. Elimineu duplicats o combineu vistes que tinguin sentit juntes.
5. Comproveu que cap de les cinc funcionalitats de l'MVP queda sense lloc.

**Exemple:** «Veure horaris» i «Escollir pista» poden quedar dins l'àrea **Reserva**, mentre que «Crear o bloquejar franges» pertany a **Gestió de pistes** del backoffice.

### Pas 4 — Classificar i establir la jerarquia

Ara decidiu quina importància té cada pàgina i com s'hi arriba.

- **Zona:** frontoffice / backoffice.
- **Nivell 1:** pàgines o apartats principals, accessibles des de la navegació principal.
- **Nivell 2:** pàgines subordinades a un apartat principal.
- **Nivell 3:** pàgines de detall o d'un subapartat, només si són necessàries.
- **Tipus:** principal / secundària / vista de suport (p. ex., confirmació).
- **Accés:** públic, client identificat o administrador.

**Plantilla B — Inventari definitiu**

| ID  | Pàgina o vista | Zona        | Grup / secció | Nivell | Tipus     | Qui hi accedeix? | Funcionalitat relacionada |
| --- | -------------- | ----------- | ------------- | ------ | --------- | ---------------- | ------------------------- |
| F01 | [Nom]          | Frontoffice | [Grup]        | 1      | Principal | Públic           | [Funcionalitat]           |
| F02 |                |             |               |        |           |                  |                           |
| B01 | [Nom]          | Backoffice  | [Grup]        | 1      | Principal | Administrador    | [Funcionalitat]           |
| B02 |                |             |               |        |           |                  |                           |

### Pas 5 — Dibuixar el mapa del lloc

Feu un **diagrama jeràrquic** amb caixes i línies. Les caixes són les pàgines o vistes; les línies indiquen de quin apartat depenen. Mostreu per separat el **frontoffice** i el **backoffice**.

Recomanacions:

- Situeu a dalt la pàgina d'entrada o el panell principal de cada zona.
- Feu servir noms breus i coherents: «Pistes», «Reserva», «Les meves reserves», «Gestió de pistes».
- No confongueu una **acció** amb una pàgina: «Desar» habitualment és un botó, no un apartat del menú.
- No dibuixeu rombes de decisió («Hi ha disponibilitat?»): aquests corresponen al **diagrama de flux**, no al mapa del lloc.
- Afegiu una llegenda si feu servir colors, símbols o línies especials.

## 4. Exemple guiat — Reserva de pistes de pàdel a Andorra

**Cinc funcionalitats d'MVP (exemple didàctic):**

1. Consultar les pistes disponibles per data i hora (**frontoffice**).
2. Consultar preus i detalls de les pistes (**frontoffice**).
3. Fer i confirmar una reserva (**frontoffice**).
4. Consultar les reserves rebudes (**backoffice**).
5. Bloquejar una franja horària perquè no sigui reservable (**backoffice**).

**Conversió de funcionalitats a pàgines:**

| Funcionalitat      | Pàgina o vista proposada           | Motiu                                    |
| ------------------ | ---------------------------------- | ---------------------------------------- |
| Disponibilitat     | Calendari de disponibilitat        | Centralitza dies, hores i pistes lliures |
| Detalls i preus    | Detall de pista                    | Mostra la informació abans de decidir    |
| Fer la reserva     | Formulari de reserva + Confirmació | Recull les dades i comunica el resultat  |
| Consultar reserves | Gestió de reserves                 | Permet al personal veure les reserves    |
| Bloquejar horaris  | Gestió de disponibilitat           | Permet modificar franges disponibles     |

**Possible mapa del lloc (text):**

```text
PLATAFORMA DE PÀDEL
├── FRONTOFFICE
│   ├── Inici
│   ├── Pistes
│   │   └── Detall de pista i preus
│   └── Reserva
│       ├── Calendari de disponibilitat
│       ├── Formulari de reserva
│       └── Confirmació
└── BACKOFFICE (accés restringit)
    └── Panell d'administració
        ├── Gestió de reserves
        └── Gestió de disponibilitat
```

Aquest arbre és **una opció possible**, no l'única correcta. En un projecte real, un calendari podria integrar-se en una única pàgina de reserva. El més important és justificar l'organització pensant en l'usuari.

**Exemples de classificació:**

| Pàgina                 | Zona        | Nivell | Tipus           | Accés                        |
| ---------------------- | ----------- | -----: | --------------- | ---------------------------- |
| Pistes                 | Frontoffice |      1 | Principal       | Públic                       |
| Detall de pista        | Frontoffice |      2 | Secundària      | Públic                       |
| Reserva                | Frontoffice |      1 | Principal       | Públic                       |
| Confirmació            | Frontoffice |      2 | Vista de suport | Usuari que ha fet la reserva |
| Panell d'administració | Backoffice  |      1 | Principal       | Administrador                |
| Gestió de reserves     | Backoffice  |      2 | Secundària      | Administrador                |

## 5. Aplicació al vostre projecte

Feu servir les preguntes següents per adaptar el procediment:

| Projecte                   | Preguntes de guia per al frontoffice                                      | Preguntes de guia per al backoffice                       |
| -------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------- |
| **Rocanolich**             | On es consulten les curses, modalitats i inscripcions?                    | On es consulten i gestionen participants i inscripcions?  |
| **Estètica i perruqueria** | On es veuen serveis, professionals, horaris i reserves?                   | On es gestionen cites, serveis, horaris i disponibilitat? |
| **Graduació**              | On s'identifica l'alumne, es veuen les butaques i es confirma la reserva? | On es consulten ocupació, reserves i incidències?         |

No cal que **tots** aquests apartats acabin essent pàgines separades. Decidiu-ho segons les funcionalitats reals del vostre MVP.

## 6. Què heu d'afegir al dossier individual?

Dins del vostre document de Google Drive, creeu l'apartat **«5. Arquitectura de la informació»** i incorporeu-hi:

1. **Taula A:** relació entre les cinc funcionalitats de l'MVP i les pàgines candidates.
2. **Taula B:** inventari definitiu de les pàgines i vistes, classificades per zona i jerarquia.
3. **Mapa del lloc visual** fet amb l'eina escollida (captura llegible o enllaç accessible).
4. **Justificació individual breu** (100–150 paraules): per què heu agrupat així les pàgines? Quina decisió facilita més la navegació del vostre User Persona?
5. **Resultat de la revisió:** una observació del company i si ha provocat algun canvi.

El llistat i el mapa s'acorden **en grup**; cadascú els documenta i redacta **la seva justificació individual**. No s'ha de lliurar un document a part.

## 7. Requisits mínims

- [ ] S'han tingut en compte les **cinc funcionalitats de l'MVP** de la Tasca 4.
- [ ] Hi ha un **inventari de pàgines i vistes**, sense confondre-les amb botons o accions.
- [ ] Cada pàgina té un **nom clar**, una funció i una classificació.
- [ ] S'identifica clarament **frontoffice i backoffice**.
- [ ] Les pàgines estan agrupades per **seccions** i ordenades per **nivells jeràrquics**.
- [ ] Hi ha un **mapa del lloc visual** llegible amb les dues zones.
- [ ] Es pot localitzar en el mapa on s'implementen les cinc funcionalitats de l'MVP.
- [ ] S'ha fet una **revisió amb un company** i n'hi ha constància.
- [ ] S'ha inclòs la **justificació individual** al dossier inicial.

> **Criteri de qualitat:** no es valora tenir moltes pàgines. Es valora que l'organització sigui coherent, comprensible i útil per als usuaris.

## 8. Extra voluntari

**Test de cerca de contingut (_tree testing_ senzill):** prepareu tres tasques concretes (per exemple, «trobar on canviar l'horari d'una cita») i demaneu a dues persones que indiquin per quines seccions del mapa navegarien. Registreu encerts, dubtes i canvis que faríeu al sitemap.

També podeu preparar **dues alternatives d'arquitectura** i justificar, amb dades de la prova, quina funciona millor.

---

**Recordatori:** la **Tasca 5** respon «**on és cada cosa?**». La propera tasca, el **diagrama de flux**, respondrà «**quins passos i decisions segueix l'usuari per completar una acció?**».
