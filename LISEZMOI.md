# Stockage ferrailles, zone AT1 – fichiers sources

Maquette 3D du stockage des aciers de la zone AT1 : plan du site, cantilevers, stockage au sol sous le portique, plan de rangement, export PDF et gestion du stock.

Auteur : MOULID HUSSEIN Badri (SNCF RESEAU / EIV BOURGOGN / METHODES INDUSTRIELLES)

## Ouvrir la maquette

Double-cliquez sur `index.html`. Une connexion Internet est nécessaire pour charger les bibliothèques (moteur 3D, PDF, Excel).

Ouvert depuis un PC, le fichier fonctionne en mode local : les modifications et les mouvements de stock restent sur ce PC.

## Organisation des fichiers

| Emplacement | Contenu |
| --- | --- |
| `index.html` | Structure de la page. En-tête : titre, métadonnées et feuille de style. Fin de page : les scripts, dans l'ordre de chargement. |
| `css/style.css` | Mise en forme, thème clair et sombre, adaptation aux écrans. |
| `js/app.js` | Toute la logique de l'application. Un sommaire en tête de fichier liste ses sections. |
| `js/donnees/references.js` | Plan de rangement du classeur : une ligne par référence (`REFS`). |
| `js/donnees/site.js` | Plan du site repris de Mavimplant (`SITE`). |
| `js/donnees/stock-initial.js` | Stock initial et seuils par référence (`STOCK0`). |
| `js/donnees/vehicules-3d.js` | Modèles 3D des véhicules (`GLB`). |
| `js/donnees/polices-pdf.js` | Police Carlito (équivalent de Calibri) pour le rapport PDF (`FONT_R`, `FONT_B`). |
| `js/donnees/logo-pdf.js` | Logo du rapport PDF (`LOGO_SRC`). |
| `img/` | Photo de fond, logo et icône. |

## Ordre de chargement (à respecter)

1. Bibliothèques : three.js r128, OrbitControls, GLTFLoader, jsPDF, jsPDF-AutoTable, SheetJS.
2. Données : les fichiers de `js/donnees/`.
3. Application : `js/app.js`, qui utilise les données ci-dessus.

## Modifier les données

- **Plan de rangement :** depuis la page (tableau, glisser-déposer, modification en masse par Excel), ou dans `js/donnees/references.js`.
- **Seuils et stock initial :** dans `js/donnees/stock-initial.js`, ou depuis la page « Gestion du stock » (bouton « Seuils »).

## Crédits

- Pick-up et moto : Innerscene Corp, domaine public CC0 1.0.
- Semi-remorque bâchée : modèle fourni par l'utilisateur, licence à vérifier auprès de sa source.
- Police Carlito : licence SIL Open Font License.
