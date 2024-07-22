# obsidian-kanban-fr
mkdir obsidian-kanban-fr
cd obsidian-kanban-fr
npm init -y
npm install obsidian
obsidian-kanban-fr/
├── .obsidian/
│   └── plugins/
│       └── obsidian-kanban-fr/
│           ├── main.js
│           ├── manifest.json
│           └── styles.css
├── package.json
└── README.md
{
  "id": "obsidian-kanban-fr",
  "name": "Obsidian Kanban FR",
  "version": "0.0.1",
  "minAppVersion": "0.12.0",
  "description": "Plugin Kanban pour Obsidian en français avec gestion des dates multiples",
  "author": "VotreNom",
  "authorUrl": "https://votre-site-web.com",
  "isDesktopOnly": false
}
const { Plugin } = require('obsidian');

class ObsidianKanbanFR extends Plugin {
  onload() {
    console.log('Chargement du plugin Obsidian Kanban FR');
    this.addRibbonIcon('dice', 'Kanban', () => {
      new Notice('Bienvenue dans Obsidian Kanban FR!');
    });

    this.addCommand({
      id: 'open-kanban',
      name: 'Ouvrir Kanban',
      callback: () => {
        // Ouvrir la vue Kanban ici
      }
    });
  }

  onunload() {
    console.log('Déchargement du plugin Obsidian Kanban FR');
  }
}

module.exports = ObsidianKanbanFR;
/* Styles de base pour le plugin Kanban */
.kanban-board {
  display: flex;
}
.kanban-column {
  margin: 10px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: #f9f9f9;
}
.kanban-task {
  margin: 5px 0;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  background-color: #fff;
}
