# Système de supervision sonore

## Configuration du contrôleur

Le contrôleur fonctionne à l'aide de Home Assistant, un système de domotique Open Source. C'est lui qui va centraliser les contrôles audio et lumineux en fonction des mesures remontées par les capteurs sonore et des règles que nous appliquerons.

Pour plus d'information sur Home Assistant, consulter le site internet <https://www.home-assistant.io/>

Le choix matériel du contrôleur s'est porté sur le Raspberry Pi 4B car il possède une sortie audio Jack 3.5 qui permet à Home Assistant de diffuser des messages audio ou des musiques. Les système Home Assistant Green et Raspberry Pi 5 n'ont pas de sortie audio Jack.

## Assemblage du contrôleur

L'assemblage du Raspberry Pi 4B est très simple. Une fois réalisé, il faut y connecter les 2 modules USB afin de pouvoir gérer les protocoles Zigbee et Matter.

![Raspberry Pi 4B](img/Controleur.png)

## Installation du contrôleur

La documentation officielle pour installer Home Assistant sur le Raspberry Pi 4B est très bien faite et maintenue à jour par la communauté. Je vous oriente directement vers elle pour cette première étape, elle est disponible via cette page :  
<https://www.home-assistant.io/installation/raspberrypi>

Une fois démarré, il faut installer manuellement plusieurs modules additionnels à Home Assistant.

### Voici la liste des modules:

- OpenBorder router Thread
- Matter
- Zigbee
- Media player

## Appairage des composants

Une fois le controleur et les modules installés, il faut appairer les bandeau LED et les capteurs sonores.
Pour se faire, il faut installer l'application Home Assistant sur votre Smartphone indispensable pour l'appairage des capteurs Matter.

## Creation de templates

Pour faire fonctionner le système correctement, il est important de calculer la valeur moyenne des capteurs pour avoir un niveau sonore global de la pièce, mais il est également indispensable de gérer une éventuelle déconnection d'un capteur. Pour se faire, on va créer un template nommé Capteur Sonore Global qui sera la référence pour gérer les déclenchements en fonction du niveau sonore mesuré.

Dans la cantine de La Roche-Jaudy, ce capteur gobal calcul le niveau sonore moyen à partir des 3 valeurs les plus elevées remontées par les 4 capteurs que comporte le système. 
Par ailleurs, pour éviter toute défaillance ou valeur incohérente, ce capteur écarte toute valeur ayant été transmise depuis plus de 7 secondes. Ce template va également un peut plus loin dans la gestion des capteurs hors ligne, car la moyenne se calcul uniquement avec des capteurs en ligne, s'il n'est reste plus qu'un seul de connecté, le système continuera de fonctionner avec ce seul capteur. Enfin, dans l'éventualité qu'il ne reste plus aucun capteur en ligne, un automatisme fera passé le bandeau LED en Bleu afin de signaler un problème de fonctionnement.
