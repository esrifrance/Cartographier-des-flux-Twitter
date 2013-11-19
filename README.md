JS-Streamlayer---Twitter
========================

Exemple : http://maps.esrifrance.fr/twitterStreamlayer.html

Cette application permet de représenter le flux twitter récupéré par ArcGIS GeoEvent Processor dans une Streamlayer de l'API ArcGIS Javascript.

Le connecteur Twitter pour ArcGIS GeoEvent Processor est disponible sur le Github Esri : https://github.com/Esri/twitter-for-geoevent

Après installation du connecteur Twitter, vous devez créer une nouvelle définition pour la sortie afin de simplifier le message Twitter entrant qui est créé automatiquement. 
La défintion des champs utilisés dans l'application est la suivante :

  Name: date
  Type: Date
  Cardinality: One
  Tags:
  TIME_START

  Name: nom
  Type: String
  Cardinality: One
  Tags:
  
  Name: lieu
  Type: String
  Cardinality: One
  Tags:
  
  Name: texte
  Type: String
  Cardinality: One
  Tags:
  
  Name: shape
  Type: Geometry
  Cardinality: One
  Tags:
  GEOMETRY
 
  Name: ID
  Type: Integer
  Cardinality: One
  Tags:
  TRACK_ID
  
  
---------------------------------------------------------------------------------------------------------
  INSTRUCTIONS
---------------------------------------------------------------------------------------------------------
  1- Créer l'Input "Receive Tweets"
  2- Créer l'Out
