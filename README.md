
# DHCP relay

Mise en place de 2 LAN avec routage et DHCP relay.

Pour que le dnsmasq se lance automatiquement, penser à rajouter la commande dans le GUI du serveur.

clic droit, configure, general settings, start command, ajouter : sh -c "dnsmasq && sh"

La ligne "post-up" dans le FRRouter config sert également à lancer en auto le dhcp-helper pour le routage du réseaux de droite.

Idem pour les PC clients, si vous voulez obtenir une IP du DHCP automatiquement au démarrage du projet, ajoutez : sh -c "udhcpc && sh"
dans le start command du GUI.
## Documentation

[Dnsmasq.conf](DHCP_relay/dnsmasq.conf.txt)

[FRRouter config](DHCP_relay/FRR_Interface_auto.txt)

## Screenshots

![App Screenshot](DHCP_relay/images/Topology.png)
![App Screenshot](DHCP_relay/images/Adressage_IP.png)
