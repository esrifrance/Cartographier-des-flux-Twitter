JS-Streamlayer---Twitter
========================

Exemple : http://maps.esrifrance.fr/twitterStreamlayer.html

Cette application permet de représenter le flux twitter récupéré par ArcGIS GeoEvent Processor dans une Streamlayer de l'API ArcGIS Javascript.

Le connecteur Twitter pour ArcGIS GeoEvent Processor est disponible sur le Github Esri : https://github.com/Esri/twitter-for-geoevent

Après installation du connecteur Twitter, vous devez créer une nouvelle définition pour la sortie afin de simplifier le message Twitter entrant qui est créé automatiquement. 
La défintion en sortie des champs utilisés dans l'application est la suivante :

  <b>MyTweetDefinition</b>

  Name: <b>date<br></b>
  Type: Date<br>
  Cardinality: One<br>
  Tags:TIME_START<br>

  Name: <b>nom</b><br>
  Type: String<br>
  Cardinality: One<br>
  Tags:<br>
  
  Name: <b>lieu<br></b>
  Type: String<br>
  Cardinality: One<br>
  Tags:<br>
  
  Name: <b>texte<br></b>
  Type: String<br>
  Cardinality: One<br>
  Tags:<br>
  
  Name: <b>shape<br></b>
  Type: Geometry<br>
  Cardinality: One<br>
  Tags:GEOMETRY<br>
 
  Name: <b>ID<br></b>
  Type: Integer<br>
  Cardinality: One<br>
  Tags:TRACK_ID<br>
  
  
  INSTRUCTIONS
---------------------------------------------------------------------------------------------------------
  <b>1</b>- Créer l'Input "Receive Tweets"
  
  <b>2</b>- Créer l'Output "Publish JSON to a Web Socket"
  <br>URL WebSocket par défaut : <i>http://localhost:6180/ws
  </i>
  
  <b>3</b>- Créer le service GeoEvent Processor "Twitter"
  <br>Ajouter un filtre avec la condition attributaire <i>geolocated=true</i>
  <br>Ajouter un processus de type Mappage de champs et faire correspondre la définition en entrée (TweetStatus) avec la définition créée pour la sortie (MyTweetDefinition) :
  <i><br>$RECEIVED_TIME = date<br>
  user.name = nom <br>
  place.full_name = lieu <br>
  text = texte <br>
  coordinates = shape <br>
  id_str = ID</i>
  
  <b>4</b>- Editer le fichier <i>twitterStreamlayer.html</i> et assurez-vous que l'URL ligne 318 correspond votre WebSocket en sortie de GeoEvent Processor
