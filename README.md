# SimpleFloatingText

**SimpleFloatingText** est un plugin PocketMine-MP pour afficher des textes flottants dynamiques et persistants,  
configurés et modifiables facilement via des menus interactifs, commandes et fichiers de configuration.

---

## Fonctionnalités

- 📄 Textes persistants enregistrés dans `floating_texts.json`
- ✅ Apparition propre au-dessus des blocs, sans hitbox ni entité.
- ✏️ Création, modification, suppression en jeu **sans restart**
- 🔄 Mise à jour automatique pour tous les joueurs connectés
- 📝 Support du placeholder `{PLAYER}`
- ⚙️ Sauvegarde et synchronisation automatiques

---

## Commandes

| Commande               | Description                                       |
|------------------------|---------------------------------------------------|
| `/floatingtext create` | Crée un nouveau texte flottant avec un formulaire |
| `/floatingtext list`   | Liste tous les floating texts existants           |
| `/floatingtext delete` | Supprime un texte flottant en le sélectionnant    |
| `/floatingtext modify` | Modifie un texte existant (changer le contenu)    |

---

## Fichier de configuration

- `floating_texts.json` est généré automatiquement, tu n’as pas besoin de le toucher à la main.
- Chaque floating text y est sauvegardé avec:
    - sa position (x,y,z, world)
    - son texte
- À chaque changement, la sauvegarde est instantanée.

---

## Fonctionnement

- **Création**: tu ouvres un formulaire pour entrer le texte et la position.
- **Modification**: tu sélectionnes dans la liste, puis tu modifies le texte.
- **Suppression**: tu sélectionnes simplement le texte à retirer.
- **Affichage**: le texte flotte à 1.25 blocs au-dessus de la position que tu choisis, centré.
- **Synchronisation**: le plugin recharge la liste pour tous les joueurs sans restart.

---

## Config.yml

```yaml
update-interval: 0 # en secondes, 0 = pas d'update auto, 20 = 1 seconde
```

- `update-interval` permet d’actualiser automatiquement les textes flottants (utile si tu veux changer dynamiquement le contenu).  
- _Par exemple 20 signifie une mise à jour toutes les secondes._
- **0 désactive l’update automatique.**

---

## Dépendances

1. ✅ CortexPE/Commando  
2. ✅ dktapps/pmforms

---
