# <img src="../images/MyTado_icon.png" width="60"/> Plugin MyTado

Le plugin **MyTado** permet de récupérer les données de vos objets connectés Tado ainsi que les infos météo gérées par Tado.

Le rafraîchissement de ces données s’effectue toutes les 30 minutes.

>**Equipements gérés**
>
>Les objets des modèles AC0X, BU0X, RU0X et VA0X sont pleinement pris en charges (a priori quel que soit leur version). Pour les autres, vous aurez uniquement accès aux fonctionalités de base (accès à la température mesurée, activation/désactivation/mode automome, mise à jour des données).
>Pour tout objet non pris en charge à ce jour, contacter le développeur en spécifiant le modèle que vous avez et les fonctionalités manquantes, ainsi que toute information que vous jugez utile.

# Configuration

## Configuration du plugin

Vous devez absolument renseigner les 3 champs suivants:
1) l'adresse mail utilisée pour créer votre compte sur Tado
2) le mot de passe défini
3) le nom exact (sensible à la casse) de votre maison sur l'application Tado

L'unité de mesure de température est facultative. **Le Celsius est l'unité par défaut**.
De même pour la convention de nommage de vos objets qui sera appliquée.

Enfin, après avoir sauver votre configuration, lancez la synchronisation de votre maison avec l'option **Synchronisation**.

## Configuration des équipements

>**INFORMATION**
>
>Il suffit d'utiliser la commande **Synchronisation** pour obtenir tous vos objets connectés ainsi que l'accès à la météo gérée par Tado.

### Vos objets connectés Tado <img src="../images/AC0X.png" width="60"/><img src="../images/BU0X.png" width="60"/><img src="../images/RU0X.png" width="60"/><img src="../images/VA0X.png" width="60"/>

En cliquant sur un objet connecté Tado, on arrive directement sur sa page de configuration :

- **Nom de l’équipement** : Nom de l'équipement basé sur son numéro de série.
- **Objet parent** : Indique l’objet parent auquel appartient l’équipement. A vous de le défnir.
- **Catégorie** : Permet de choisir la catégorie de l'équipement.

En cliquant sur l'onglet **Commandes**, on retrouve la liste de toutes les commandes disponibles ainsi que la possibilité d’historiser les valeurs numériques.
Les données sont mises à jour toutes les 30mn, mais vous pouvez forcer la mise à jour à la demande avec la commande **refresh**.

Le widget affiche l'image correspondant à votre équipement ainsi que les informations et configurations actuelles de vos équipements.
Vous pouvez également définir le mode de fonctionnement de votre objet:
- 'Autonome': La programmation faite sur l'appli Tado est prise en compte;
- 'Manuel': Offre la possibilité de sortir du mode automatique et de définir le ou les paramètre(s) de votre choix;
- 'Eteint': L'objet est totalement éteint.

>**Information importante**
>
>Dans le cas d'un changement manuel de la température désirée, cette dernière sera appliquée à tous les objets présents dans la même zone que votre objet (c'est ainsi que fonctionne Tado). 

### La météo Tado <img src="../images/WeatherEq.svg" width="60"/>

En cliquant sur la météo Tado, on arrive directement sur sa page de configuration :

- **Nom de l’équipement** : Nom de l'équipement par défaut.
- **Objet parent** : Indique l’objet parent auquel appartient l’équipement. A vous de le défnir.
- **Catégorie** : Permet de choisir la catégorie de l'équipement.
- **Latitude** : Latitude référencée sur Tado pour votre maison et utilisée pour récupérer la météo correpondante.
- **Longitude** : Longitude référencée sur Tado pour votre maison et utilisée pour récupérer la météo correpondante.

En cliquant sur l'onglet **Commandes**, on retrouve la liste de toutes les commandes disponibles ainsi que la possibilité d’historiser les valeurs numériques ainsi que l'état météorologique.
Les données sont mises à jour toutes les 30mn, mais vous pouvez forcer la mise à jour à la demande avec la commande **refresh**.

Le widget affiche le temps qu'il fait sous forme d'image ainsi que la température et la luminosité actuelle.