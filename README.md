JS-Streamlayer---Twitter
========================

Exemple : http://maps.esrifrance.fr/twitterStreamlayer.html

Cette application permet de représenter le flux twitter récupéré par ArcGIS GeoEvent Processor dans une Streamlayer de l'API ArcGIS Javascript.
Connecteur Twitter pour ArcGIS GeoEvent Processor : https://github.com/Esri/twitter-for-geoevent

Après installation du connecteur Twitter, vous devez créer une nouvelle définition pour la sortie afin de simplifier le message Twitter entrant. 
La défintion utilisée dans l'application est la suivante :

Name: myTweetDefinition
Owner: arcgis
GUID: 96b979eb-4794-46aa-9062-14be9700a1c7
Field Definitions:

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
