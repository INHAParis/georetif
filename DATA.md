## Données exportées du Géo RETIF

### Structure du fichier
* L’encodage des fichiers .csv et .geojson est le **UTF-8**
* le séparateur du fichier .csv est la **virgule** (« , »)

#### Champs communs :
* **UUID** : l’identifiant unique de la notice sur la base AGORHA. On peut utiliser ce champ pour construire l’URI de chaque notice [`"https://agorha.inha.fr/ark:/54721/" + "UUID"`]
* **TIT** : le titre ou les titres de l’œuvre 
* **AUT** : la personne liée à l’œuvre (la première dans la liste des attributions sur la base AGORHA)
* **SIE** : le siècle dans lequel l’œuvre a été créée
* **LIE** : le lieu de conservation actuel 
* **ATT** : l’attribution lié au champ **AUT** (ex. *de*, *copié d’après*, *genre de*… etc.) 
* **LKP** : la partie final du lien de l’image à basse résolution de l’œuvre, si présente dans la base AGORHA. Pour obtenir le lien il faut concaténer [`"https://agorha.inha.fr/ark:/54721/" + "LKP"`] ; les œuvres sans images renvoie à une image commune : "3e6f35f9-2e24-430e-becc-ead414a48838/doc/068be177-fb92-4a25-b8c9-b7206a19ea82/thumbnail.jpg"

#### csv :
* **latitude** [csv] : la latitude du lieu de conservation exprimée en dégrées décimaux. Le système de référence géographique (crs) EPSG :4326 – WGS84
* **longitude** [csv] : la longitude du lieu de conservation de l’œuvre exprimée en dégrées décimaux Le système de référence géographique (crs) EPSG :4326 – WGS84

#### geojson :
* **coordinates** [geojson] : la longitude et la latitude du lieu de conservation de l’œuvre exprimées en dégrées décimaux Le système de référence géographique (crs) EPSG :4326 – WGS84
