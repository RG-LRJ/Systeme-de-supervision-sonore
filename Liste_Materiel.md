# Système de supervision sonore LED

## Liste du matériel nécessaire

Cette liste correspond au matériel que nous avons acheté pour équiper la cantine de La Roche-Jaudy. Les liens des sites internet sur lesquels nous avons commandé le matériel sont présents uniquement à titre indicatif afin de retrouver les références exactes. Il ne s'agit en aucun cas de publicité.

### Contrôleur principal

- **Raspberry Pi 4B (8GB)** - [[lien](https://www.gotronic.fr/art-kit-raspberry-pi-4-b-kit-pi4-8-38591.htm)]
  - Pi 4B car sortie audio Jack 3.5
  - 8GB de RAM pour une pérennité dans le temps
- **SONOFF - Clé USB Zigbee 3.0** - [[lien](https://www.domadoo.fr/fr/dongle-zigbee/6315-sonoff-cle-usb-zigbee-30-antenne-externe-v2-6920075777659.html)]
  - Pour gérer le Zigbee (contrôleurs LED)

### LED

- **40m de bandeau LED RGB très lumineux** - [[lien](https://www.inovatlantic-led.fr/rubans-led-rgb-24v/521-3198-ruban-led-24v-rgb-10m.html#/5-couleur_led-rgb/338-indice_de_protection-ip68_etanche_adhesif/420-longueur-10_metres)]
  - 4x 10m de ruban LED
  - 1200 Lumens/m
  - 60 LED/m
  - 14,4W/m (144 Watts par bandeau)
- **4 alimentations 150W** (car 144W par bandeau) - [[lien](https://www.inovatlantic-led.fr/alimentations-24v/591-3423-alimentation-metalbox-24v-625a-150w-compact.html#/106-indice_de_protection-ip20/175-source_electrique-secteur_230v/264-alimentation-24v_625a_150w)]
- **4 contrôleurs Zigbee** (1 par alimentation) - [[lien](https://www.inovatlantic-led.fr/controleurs-rgb/1168-controleur-30a-zigbee-multizones-5-en-1-rgb-rgbw-rgb-blanc-variable-12-48v.html)]

### Capteurs

- **4 alimentations USB Type-C** - [[lien](https://www.gotronic.fr/art-alimentation-usb-type-c-30732.htm)]
- **4 modules Atom Echo C008-C** - [[lien](https://www.gotronic.fr/art-module-atom-echo-c008-c-32198.htm)]
  - Reprogrammer le capteur avec ce sketch ESPHome [[lien]](https://github.com/RG-LRJ/Systeme-de-supervision-sonore/blob/main/Capteur_dB.yaml)

### Audio

- **2 enceintes KOALA 6A BT** - [[lien](https://www.energyson.fr/koala-6a-bt.html)]
  - Puissante
  - Compacte
  - Bluetooth
  - Entrée microphone
  - Line Out pour connecter une autre enceinte
- **1 câble XLR 30m** - [[lien](https://www.energyson.fr/3-star-mmf-3000-30m.html)]
  - Pour relier les enceintes
- **1 câble jack/jack 6.35** - [[lien](https://www.energyson.fr/cl-0715-15m.html)]
  - Pour relier le microphone à l'enceinte
- **1 câble jack/jack 3.5** - [[lien](https://www.energyson.fr/cab-2058-15m.html)]
  - Pour relier le Raspberry à l'enceinte
- **1 microphone** - [[lien](https://www.energyson.fr/da-uhf-mh-100.html)]
