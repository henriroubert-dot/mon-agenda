# Mon Agenda — projet personnel

Application web installable (PWA) en HTML, CSS et JavaScript, conçue pour être développée dans Visual Studio Code.

## Lancer sur Windows

1. Décompresse `mon-agenda.zip`.
2. Ouvre le dossier `mon-agenda` dans Visual Studio Code.
3. Installe l'extension **Live Server**.
4. Clique droit sur `index.html` puis **Open with Live Server**.
5. Teste les écrans dans ton navigateur.

Pour l'installation sur iPhone, le site doit être servi en HTTPS (ou depuis localhost pour le développement). Publie gratuitement le dossier sur un hébergeur statique compatible HTTPS, par exemple GitHub Pages, puis ouvre l'adresse dans Safari sur l'iPhone et choisis **Partager → Sur l’écran d’accueil**.

## Fonctionnalités présentes

- Tableau de bord et progression des tâches
- Calendrier mensuel avec sélection d'une date
- Événements, tâches, dates limites, priorités, catégories et répétitions enregistrées
- Filtres de tâches (aujourd'hui, à venir, en retard, terminées)
- Notes et recherche
- Habitudes quotidiennes
- Objectifs avec progression
- Suivi des dépenses et devise
- Minuteur de concentration
- Thème clair/sombre, premier jour de semaine
- Export/import JSON
- Cache hors ligne via service worker

## Limites importantes (notifications et iPhone)

Cette première version stocke les données localement dans le navigateur de l'appareil. Elle ne synchronise pas automatiquement PC et iPhone.

Les notifications programmées à une heure future ne sont **pas garanties** par une PWA seule : les navigateurs peuvent suspendre le JavaScript lorsque l'application est fermée. Sur iOS, les notifications Web Push nécessitent iOS 16.4 ou ultérieur, une PWA ajoutée à l'écran d'accueil, l'autorisation de l'utilisateur et un serveur push configuré. Le bouton d'autorisation ne met pas en place à lui seul un serveur de notifications.

Pour de vrais rappels fiables même lorsque l'app est fermée, il faudra ajouter une partie serveur (push) ou plus tard empaqueter l'application en application native avec les outils Apple et un Mac.

## Sécurité et données

Les données sont enregistrées dans `localStorage` sur l'appareil. Ne stocke pas de mots de passe ni d'informations très sensibles. Utilise régulièrement l'export JSON. Effacer les données du navigateur peut supprimer les informations locales.
