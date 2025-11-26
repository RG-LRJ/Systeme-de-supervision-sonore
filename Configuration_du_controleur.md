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
