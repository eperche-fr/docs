# Changelog plugin MyTado - beta

# 06/04/2025 - Version 7.0

- Commande de détection de fenêtre ouverte ajoutée. **Attention: Nécessité de mettre à jour les dépendances et de resynchroniser.**
- La commande **Définir la température désirée** est maintenant de sous-type *curseur*. **Attention: Impact sur les scénarios, donc prévoyez leur correction après mise à jour.**
- Simplification de la gestion des commandes pour une plus grande flexibilité à l'avenir.

# 05/04/2025 - Version 6.2

- Bug lors de la synchronisation corrigé (introduit en version 6.0)

# 01/04/2025 - Version 6.1

- Bug lors de la création des commandes d'une nouvelle maison corrigé (introduit en version 6.0)

# 23/03/2025 - Version 6.0

- Adaptation de la connexion à Tado suite au changement d'API du 21/03/2025

# 19/03/2025 - Version 5.1

- Réorganisation de l'affichage de la page équipement  
- Problème résolu sur la synchronisation lors d'une nouvelle installation du plugin  
- Correction de l'affichage de l'image pour les appareils du modèle RU02B (RU02 gérant thermostat et eau chaude)  

# 09/03/2025 - Version 5.0

- Refonte de la gestion des configurations d'équipements pour une plus grande flexibilité à l'avenir, indépendamment des versions du plugin.
- Ajout des équipements de type **utilisateurs** afin d'obtenir du détail sur la localisation des utilisateurs Tado pour vos scénarios.
- Il est possible de personnaliser l'image des utilisateurs, et celle-ci est affichée sur le widget **maison** en cas de présence.
- Possibilité de choisir la fréquence de rafraichissement des données.

# 20/02/2025 - Version 4.1

- Pour les objets **TadoX**, la température affichée est maintenant celle **mesurée par l'objet** (et non plus celle de la zone).
- Le widget **maison Tado** affiche désormais **le nombre de personnes présentes**.

# 16/02/2025 - Version 4.0

- Le démon s'appuye maintenant sur le module jeedomdaemon de Mips qui supprime toute fuite mémoire.
- L'équipement maison a une nouvelle action permettant de savoir combien d'utilisateurs sont présents à la maison.
- Les objets jouant plusieurs rôles (par exemple: contrôle chaudière et chauffe-eau) sont maintenant représentés par un équipment par fonction.
- Les paramètres des actions sont maintenant disponibles lors des tests de commande et dans les scénarios.

# 19/01/2025 - Version 3.1

- Les valeurs possibles des différents paramètres des modules d'air conditionné sont à présent recupérées dynamiquement.
- Résolution d'un problème de récupération de l'état d'un objet TadoX dans le cas où il est en mode manuel pour une durée définie.
- Mise à jour de la documentation afin de décrire la manière de gérér des scénarios avec MyTado.

# 12/2024 - Version 3.0

- Les objets TadoX sont à présent pris en charge
- La météo est convertie en maison, et la configuration de la connexion à la maison a basculé sur cet équipement "maison".
- Il est possible de configurer plusieurs maisons dans le cas où l'on possède des objets Tado et TadoX (ce qui nécessite 2 maisons séparées).
- Ajout de 4 nouvelles commandes pour les objets Tado(X): activer, désactiver, la date de dernière mise à jour des données, et le niveau de batterie.

# 11/2024 - Version 2.0

- La gestion de la connexion à Tado utilise maintenant un démon pour éviter les temps de latence en PHP.

# 30/10/2024 - Version 1.6

- Les erreurs de récupération des capacités d'un objet de type AC n'entraîne plus le blocage de la récupération des autres objets.

# 17/10/2024 - Version 1.5

- La puissance de chauffe est maintenant récupérée et affichée.
- Il est maintenant possible de changer le nommage par défaut des objets connectés Tado.
- Traduction espagnole ajoutée

# 13/10/2024 - Version 1.4

- Correction de bug : Ajout d'un nom par défaut aux commandes météorologiques.
- Les différentes versions d'un même type de modèle d'objet connu sont à présent configurées de la même manière.

# 25/05/2024 - Version 1.3

- Ajout des objets de gestion d'air conditionné et de chauffe-eau.
- Ajout de la traduction en allemand.

# 08/05/2024 - Version 1.2

- Les commandes activer/désactiver sont remplacées par la commande 'mode' de type info et par la commande 'set_mode' de type action.
- Le widget des objets a été mis à jour en conséquence.

# 05/05/2024 - Version 1.1

- Ajout de commandes pour activer/désactiver des modules ainsi que pour définir une température manuellement.
- Première version des widgets.

# 25/04/2024 - Version 1.0

- Première version stable.