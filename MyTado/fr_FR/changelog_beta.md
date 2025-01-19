# Changelog plugin MyTado - beta

# 01/2025 - Version 3.1

- Résolution d'un problème de récupération des modules d'air conditionné dans le cas où ils sont éteints
- Résolution d'un problème de récupération de l'état d'un objet TadoX dans le cas où il est en mode manuel pour une durée définie

# 12/2024 - Version 3.0

- Les objets TadoX sont à présent pris en charge
- La météo est convertie en maison, et la configuration de la connexion à la maison a basculé sur cet équipement "maison"
- Il est possible de configurer plusieurs maisons dans le cas où l'on possède des objets Tado et TadoX (ce qui nécessite 2 maisons séparées)
- Ajout de 4 nouvelles commandes pour les objets Tado(X): activer, désactiver, la date de dernière mise à jour des données, et le niveau de batterie

# 11/2024 - Version 2.0

- La gestion de la connexion à Tado utilise maintenant un démon pour éviter les temps de latence en PHP

# 30/10/2024 - Version 1.6

- Les erreurs de récupération des capacités d'un objet de type AC n'entraîne plus le blocage de la récupération des autres objets

# 17/10/2024 - Version 1.5

- La puissance de chauffe est maintenant récupérée et affichée
- Il est maintenant possible de changer le nommage par défaut des objets connectés Tado
- Traduction espagnole ajoutée

# 13/10/2024 - Version 1.4

- Correction de bug : Ajout d'un nom par défaut aux commandes météorologiques
- Les différentes versions d'un même type de modèle d'objet connu sont à présent configurées de la même manière

# 25/05/2024 - Version 1.3

- Ajout des objets de gestion d'air conditionné et de chauffe-eau
- Ajout de la traduction en allemand

# 08/05/2024 - Version 1.2

- Les commandes activer/désactiver sont remplacées par la commande 'mode' de type info et par la commande 'set_mode' de type action
- Le widget des objets a été mis à jour en conséquence

# 05/05/2024 - Version 1.1

- Ajout de commandes pour activer/désactiver des modules ainsi que pour définir une température manuellement
- Première version des widgets

# 25/04/2024 - Version 1.0

- Première version stable