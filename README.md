# SimpleFloatingText

**SimpleFloatingText** est un plugin PocketMine-MP avancé permettant d’afficher des textes flottants dynamiques et persistants,  
configurés et modifiables facilement via des menus interactifs, commandes et fichiers de configuration.

---

## Fonctionnalités

- 📄 Textes persistants enregistrés dans `floating_texts.json`
- ✅ Apparition propre au-dessus des blocs, sans hitbox ni entité
- ✏️ Création, modification, suppression en jeu **sans restart**
- 📝 Support du placeholder `{PLAYER}`, `{DISPLAY_NAME}`, `{WORLD}`, `{PING}`
- 🔄 Mise à jour automatique pour tous les joueurs connectés
- 🪄 Support d’un **item flottant en 360°** au-dessus du texte
- ⚙️ Sauvegarde et synchronisation automatiques
- 📦 Architecture DTO propre, meilleure stabilité
- 🛡️ Compatible PMMP 5.0+

---

## Commandes

| Commande                     | Description                                             |
|------------------------------|---------------------------------------------------------|
| `/floatingtext create`       | Crée un nouveau texte flottant avec un formulaire       |
| `/floatingtext list`         | Liste tous les floating texts existants                 |
| `/floatingtext delete`       | Supprime un texte flottant en le sélectionnant          |
| `/floatingtext modify`       | Modifie un texte existant (changer le contenu, l'item)  |

---

## Fonctionnement

- **Création**: formulaire interactif pour définir texte, position, et éventuellement l’item flottant
- **Modification**: sélection depuis une liste, édition ligne par ligne, ajout/suppression d’une ligne,
  + possibilité de lier l’item en main comme icône flottante
- **Suppression**: sélection simple et confirmation
- **Affichage**:
  - le texte apparaît à 1.25 blocs au-dessus de la position
  - l’item flottant (optionnel) apparaît au-dessus, et tourne à 360°
  - la hauteur de l’item s’adapte dynamiquement au nombre de lignes
- **Synchronisation**: tout changement est propagé à tous les joueurs instantanément
- **Reconnexion**: les floating texts sont resynchronisés automatiquement quand un joueur rejoint
- **Configuration DTO**: robustesse et fiabilité du code, plus d’erreurs d’array

---

## Fichier de configuration

- `floating_texts.json` est généré automatiquement, tu n’as pas besoin de le toucher à la main.
- Chaque floating text y est sauvegardé avec:
  - sa position (x,y,z, world)
  - son texte
  - l’item affiché (si défini)
- À chaque changement, la sauvegarde est instantanée.

---

## Config.yml

```yaml
update-interval: 0 # en secondes, 0 = pas d'update auto, 20 = 1 seconde
```

* `update-interval` permet d’actualiser automatiquement les textes flottants (utile si tu veux changer dynamiquement le contenu).
* _Par exemple 20 signifie une mise à jour toutes les secondes._
* **0 désactive l’update automatique.**

---
