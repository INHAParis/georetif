# georetif
The webmapping of RETIF program

Based on: 
* [leaflet.js](https://github.com/Leaflet/Leaflet)
* [Autolinker.js](https://github.com/gregjacobs/Autolinker.js/)
* [jquery](https://github.com/jquery/jquery)
* [leaflet.markercluster.js](https://github.com/Leaflet/Leaflet.markercluster)
* [leaflet-hash.js](https://github.com/mlevans/leaflet-hash)
* [leaflet-sidebar.js](https://github.com/Turbo87/sidebar-v2)
* [qgis2web](https://github.com/tomchadwin/qgis2web)

[![Caption](https://georetif.inha.fr/images/icons-128.png)](https://georetif.inha.fr/)

## Données exportées du Géo RETIF

### Structure du fichier
* L’encodage des fichiers .csv et .geojson est le **UTF-8**
* le séparateur du fichier .csv est la **virgule** (« , »)

#### Champs communs :
* **UK** : l’identifiant unique de la notice sur la base AGORHA. On peut utiliser ce champ pour construire l’URI de chaque notice [`"https://agorha.inha.fr/inhaprod/ark:/54721/003" + "UK"`]
* **TIT** : le titre ou les titres de l’œuvre 
* **AUT** : la personne liée à l’œuvre (la première dans la liste des attributions sur la base AGORHA)
* **SIE** : le siècle dans lequel l’œuvre a été créée
* **LIE** : le lieu de conservation actuel 
* **ATT** : l’attribution lié au champ **AUT** (ex. *de*, *copié d’après*, *genre de*… etc.) 
* **LKP** : la partie final du lien de l’image à basse résolution de l’œuvre, si présente dans la base AGORHA. Pour obtenir le lien il faut concaténer [`"https://agorha.inha.fr/inhaoai/servlet/DocViewerServlet?file=folder_0001/folder_0001/" + "LKP"`] ; les œuvres sans images renvoie à une image commune : "folder_0006/folder_0007/elem_0054/pas_d_image_disponible_low.jpg"

#### csv :
* **latitude** [csv] : la latitude du lieu de conservation exprimée en dégrées décimaux. Le système de référence géographique (crs) EPSG :4326 – WGS84
* **longitude** [csv] : la longitude du lieu de conservation de l’œuvre exprimée en dégrées décimaux Le système de référence géographique (crs) EPSG :4326 – WGS84

#### geojson :
* **coordinates** [geojson] : la longitude et la latitude du lieu de conservation de l’œuvre exprimées en dégrées décimaux Le système de référence géographique (crs) EPSG :4326 – WGS84
