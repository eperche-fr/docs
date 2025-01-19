# <img src="../images/MyTado_icon.png" width="60"/> Plugin MyTado

Le plugin **MyTado** permet de récupérer les données de vos objets connectés Tado et Tado X ainsi que les infos météo gérées par Tado.

Le rafraîchissement de ces données s’effectue toutes les 30 minutes.

>**Equipements gérés**
>
>Seuls les modèles BU0X, BP0, BR0X, CK04, RU0X, SU0X, VA0X et WR0X sont pleinement pris en charges à ce jour (a priori quel que soit leur version). 
>Pour tout objet non pris en charge à ce jour, voire un soucis avec l'un de ceux listés, suivre les instructions de la partie [En cas de problèmes](#en-cas-de-problèmes).

# Configuration

## Configuration du plugin

Dans un premier temps, allez dans la configuration du plugin.
Assurez vous de lancer l'installation des dépendances, puis du démon.
Si vous n'arrivez pas à lancer le démon, il se peut que le port du démon utilisé par défaut (59969) soit déjà pris. 
Dans ce cas, définissez un port que vous savez disponible dans la partie configuration, sauvez et tentez de relancer le démon.  
Si le problème persiste, suivre les instructions de la partie [En cas de problèmes](#en-cas-de-problèmes).

Si vous le souhaitez, vous pouvez également changer les deux paramètres suivants:
1. L'unité de mesure de température à afficher. **Le Celsius est l'unité par défaut**.
2. La convention de nommage de vos objets qui sera appliquée.

Une fois le démon en marche, fermez la page de configuration pour revenir sur la page principale du plugin, et suivez les étapes suivantes:
1. Cliquez sur "Ajouter une maison"
2. Donnez un nom à votre maison (le nom n'a pas besoin d'être le même que chez Tado), puis cliquer sur "Ok"
3. Saisissez les trois informations liées à votre compte Tado
    - l'adresse mail utilisée pour créer votre compte sur Tado
    - le mot de passe de votre compte Tado
    - le nom exact (sensible à la casse) de votre maison sur l'application Tado
4. Sauvez votre maison

Si les informations saisies sont exactes, les information complémentaires de votre maison seront ajoutées, et les objets Tado our TadoX (selon votre maison) seront synchronisés au bout de quelques secondes.
Fermez la maison pour vérifier que vos objets apparaissent.
Si après quelques secondes rien ne se passe, rafraichissez la page manuellement. 
Si vous n'obtenez pas vos objets, vérifiez les logs afin de voir si vous pouvez corriger un problème remonté par vous-même.
Sinon, suivre les instructions de la partie [En cas de problèmes](#en-cas-de-problèmes).

Enfin, si vous rajoutez des équipements à votre maison Tado/TadoX, le bouton **Synchronisation** est là pour les récupérer.

>**INFORMATION**
>
>Si vous possédez des objets Tado et TadoX, vous avez donc deux maisons. Vous devez alors créer une maison pour chacun de vos comptes Tado.
>Tous les objets seront ainsi listés, peu importe de quelle maison ils viennent.

## Configuration des équipements

>**RAPPEL**
>
>Il suffit d'utiliser la commande **Synchronisation** pour récupérer tout nouvel objet connecté ajouté à votre maison Tado, ou après une mise à jour du plugin qui permettrait la prise en charge d'un nouveau type d'objet que vous possédez.

### Vos objets connectés Tado
<img src="../images/WR0X.png" width="60"/><img src="../images/BU0X.png" width="60"/><img src="../images/RU0X.png" width="60"/><img src="../images/VA0X.png" width="60"/><img src="../images/VA04.png" width="60"/><img src="../images/RU04.png" width="60"/><img src="../images/CK04.png" width="60"/>

En cliquant sur un objet connecté Tado, on arrive directement sur sa page de configuration :

- **Nom de l’équipement** : Nom de l'équipement basé sur son numéro de série.
- **Objet parent** : Indique l’objet parent auquel appartient l’équipement. A vous de le défnir.
- **Catégorie** : Permet de choisir la catégorie de l'équipement.

En cliquant sur l'onglet **Commandes**, on retrouve la liste de toutes les commandes disponibles ainsi que la possibilité d’historiser les valeurs numériques.
Les données sont mises à jour toutes les 30mn, mais vous pouvez forcer la mise à jour à la demande avec la commande **Rafraîchir**.

Dans le dashboard, le widget affiche l'image correspondant à votre équipement ainsi que les informations et configurations actuelles de vos équipements.
Vous pouvez également définir le mode de fonctionnement de votre objet:
- 'Autonome': La programmation faite sur l'appli Tado est prise en compte;
- 'Manuel': Offre la possibilité de sortir du mode automatique et de définir le ou les paramètre(s) de votre choix;
- 'Eteint': L'objet est totalement éteint.

>**Information importante**
>
>Dans le cas d'un changement manuel de la température désirée, cette dernière sera appliquée à tous les objets présents dans la même zone que votre objet (c'est ainsi que fonctionne Tado). 

### La maison Tado <img src="../images/HomeEq.svg" width="60"/>

En cliquant sur votre maison Tado, on arrive directement sur sa page de configuration :

- **Nom de l’équipement** : Nom que vous avez donné à votre maison sur jeedom.
- **Objet parent** : Indique l’objet parent auquel appartient l’équipement. A vous de le défnir.
- **Catégorie** : Permet de choisir la catégorie de l'équipement.
- **Latitude** : Latitude référencée sur Tado pour votre maison et utilisée pour récupérer la météo correspondante.
- **Longitude** : Longitude référencée sur Tado pour votre maison et utilisée pour récupérer la météo correspondante.

Ainsi que vos informations de connexion à Tado pour cette maison (n'oubliez pas de changer votre mot de passe ici si vous êtes amené à le changer sur le site Tado!).

En cliquant sur l'onglet **Commandes**, on retrouve la liste de toutes les commandes disponibles ainsi que la possibilité d’historiser les valeurs numériques ainsi que l'état météorologique.
Les données sont mises à jour toutes les 30mn, mais vous pouvez forcer la mise à jour à la demande avec la commande **Rafraîchir** (notez que cela force la mise à jour des données de météo mais également de tous vos objets appartenant à cette maison).

Le widget affiche le temps qu'il fait sous forme d'image ainsi que la température et la luminosité actuelle.

# Gérer des scénarios

Différentes commandes nécessitent un ou des paramètres. En attendant une future version de MyTado qui permettra de saisir ou sélectionner les paramètres désirés, uen fis ajouter la commande désirée, il vous faut utiliser la version json des scénarios pour transmettre le paramètre désiré (bouton "Edition texte" dans la configuration des commandes du scénario). 
>**ATTENTION**
>Ne plus enregitrer les changements de votre scénario que par le bouton pésent en mode édition du json, ou vous perdrez vos configurations d'options spécifiques.

Dans tous les cas, avec MyTado, il est fortement conseillé de n'utiliser dans vos scénarios que les commandes suivantes:
- "activer": Mets en mode "AUTO" votre module.
- "désactiver": Eteins votre module.
- "changer de mode": Permet en particulier de basculer en mode manuel et de définir tout autre paramètre que vous souhaitez changer.

**Comment utliser la commande "changer de mode"?**

Ajouter dans les options la clé "mode" associé à la valeur "MANUAL".
Pour changer la température désirée, utilisée la clé "expected_temperature" suivie de la température désirée (le point est à utiliser comme séparateur de décimales).
Pour les modules air conditionné, mettre la valeur souhaitée **en lettres captitales** (les valeurs disponibles sont visibles dans le widget) précédée d'une des clés suivantes:
- "AC_mode"
- "fan_speed"
- "vertical_swing_mode"
- "horizontal_swing_mode"

>Exemple de la balise "options" pour une vanne thermostatique:
>"options": {
>            "mode": "MANUAL",
>            "expected_temperature": "17.5",
>            "enable": "1",
>            "background": "0"
>        }

>Exemple de la balise "options" pour une module d'air conditionné:
>"options": {
>            "mode": "MANUAL",
>            "expected_temperature": "17.5",
>            "AC_mode": "HEAT",
>            "enable": "1",
>            "background": "0"
>        }

# En cas de problèmes

Contactez le développeur en spécifiant les modèles d'objet Tado/TadoX que vous avez, les fonctionalités manquantes ou présentants un disfonctionnement, ainsi que toute information que vous jugerez utile. 
Et n'oubliez pas de fournir les logs du plugin et de son démon (en prenant garde de masquer vos données personnelles).