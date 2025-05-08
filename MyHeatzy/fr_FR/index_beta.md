# <img src="../images/MyHeatzy_icon.png" width="60"/> Plugin MyTado

Le plugin **MyHeatzy** permet de récupérer les données de vos objets connectés Heatzy.

Le rafraîchissement de ces données s’effectue de manière régulière selon votre sélection du cron actif (entre 5 et 30mn).

---

> **Équipements gérés**
>
> Seuls les modèles de type Pilote et Glow sont pleinement pris en charge à ce jour (a priori quelle que soit leur version).
> Pour tout objet non pris en charge actuellement, ou en cas de problème avec l'un de ceux listés, suivez les instructions de la section [En cas de problèmes](#en-cas-de-problèmes).

---


# Configuration

## Configuration du plugin

1. Allez dans la configuration du plugin.
2. Installez les dépendances.
3. Lancez le démon.

Si le démon ne se lance pas, il se peut que le port par défaut (59769) soit déjà utilisé. Dans ce cas, choisissez un port libre (ex : 59770), sauvegardez, puis relancez le démon. Si le problème persiste, consultez la section [En cas de problèmes](#en-cas-de-problèmes).

Vous devez aussi renseigner (et sauver) :
- Votre identifiant chez Heatzy.
- Votre mot de passe de connexion à Heatzy.
- La fréquence de rafraîchissement : cron 5, 10, 15 ou 30 minutes (ne gardez qu'un seul cron actif). Gardez aussi le cron journalier nécessaire.

Une fois les informations correctes, les objets seront synchronisés automatiquement. Fermez la page de configuration. Si vos équipements ne s'affichent pas automatiquement, rafraîchissez la page, et si cela persiste consultez les logs.

## Configuration des équipements

> **RAPPEL**
>
> Utilisez la commande **Synchronisation** pour récupérer tout nouvel objet que vous avez ajouté ou nouvellement pris en charge par une mise à jour du plugin.

### Objets connectés Heatzy
<img src="../images/Pilote.png" width="60"/><img src="../images/Glow.png" width="60"/>

En cliquant sur un objet Heatzy, vous accédez à :

- **Nom de l’équipement** : Nom que vous avez donné sur l'application Heatzy.
- **Objet parent** : À définir selon votre organisation.
- **Catégorie** : Choisissez la catégorie de l'équipement.

Onglet **Commandes** :
- Liste des commandes disponibles.
- Possibilité d’historiser les valeurs numériques.
- Rafraîchissement possible manuellement avec la commande **Rafraîchir**.

Sur le dashboard, le widget affiche l'image de l'équipement, ses informations et sa configuration actuelle.

Modes disponibles :
- **Confort**
- **Eco**
- **Hors-gel** 
- **Eteint**

Vous pouvez également selon les équipements: 
- Passer en mode boost
- Passer en mode vacances
- Définir la température désirée (préalablement, basculez en mode Confort ou Eco pour définir la température correspondante)
- Activer/désactiver la programmation

---

# Gérer des scénarios

Bien penser à changer le mode en Eco ou Confort avant de définir une température désirée dans vos scénarios! (uniquement disponible pour certains équipements).

---

# En cas de problèmes

1. Passez les logs **MyHeatzy** en mode **debug**.
2. Relancez le démon.
3. Consultez les logs pour identifier le souci.

Sinon, consultez les [FAQs](#faqs), et en dernier lieu la section [Demander de l'aide](#demander-de-laide).

## FAQs

### Erreur Fatal: [Errno 98] address already in use

Le port de communication entre votre jeedom et le démon (59769 par défaut) est occupé. Changez-le pour un autre (ex. 59770) dans la configuration, puis relancez le démon.

## Demander de l'aide

1. Vérifiez si votre problème est déjà listé dans la [communauté Jeedom](https://community.jeedom.com/tag/plugin-myheatzy)

2. Si non, créez un nouveau sujet

3. Dans tous les cas, indiquez :
   - Votre configuration Jeedom
   - Les modèles d'équipement Heatzy que vous utilisez
   - Les logs complets **MyHeatzy** et **MyHeatzy_daemon** (fichiers attachés), en vous assurant qu'ils contiennent les étapes menant au problème (en mode debug!)

> **Masquez vos données personnelles dans les logs avant de les publier !**

# Autres recommandations

1. Pensez à laisser un avis sur le market si vous aimez ce plugin.
2. Proposez vos idées d'amélioration au développeur !

---

**Merci d'utiliser le plugin MyHeatzy !**

Votre retour est précieux pour continuer à l'améliorer 😊