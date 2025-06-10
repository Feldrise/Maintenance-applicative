## 📁 Dossier du projet – Fil rouge TP DEVE426

### 🧩 Titre : Maintenance évolutive et corrective de l'application "GestConge"

---

### 📘 1. Contexte professionnel

L’entreprise **NexaGroup** est une PME française spécialisée dans les services numériques (ESN), basée à Lyon. Elle accompagne principalement des TPE et PME dans leur transformation digitale : refonte de site web, automatisation de processus, déploiement de solutions collaboratives, etc.

Avec un effectif de 120 salariés répartis sur 3 agences (Lyon, Nantes, Montpellier), NexaGroup dispose d’une équipe RH restreinte mais très sollicitée. En 2021, dans un souci d’efficacité interne et pour répondre à une frustration croissante concernant les outils RH “trop rigides” du marché, la direction décide de faire développer une application web sur-mesure pour la **gestion des congés et du télétravail**.

Cette application, baptisée **GestConge**, a été conçue par un alternant développeur en collaboration avec la responsable RH. L’idée initiale était de créer un outil simple, rapide à déployer et totalement adapté aux besoins spécifiques de l’entreprise. À l’époque, le projet a été considéré comme un “bonus interne” sans réelle stratégie long terme.

---

Trois ans plus tard, **GestConge est devenue indispensable**. Tous les collaborateurs l’utilisent pour poser leurs congés, signaler des jours de télétravail ou consulter les absences de leurs collègues. Le back-office permet à la RH de gérer les soldes de congés, d’exporter les données pour la paie et d’avoir une vue consolidée des absences.

Cependant, le code n’a quasiment pas évolué depuis sa mise en production. Le développeur initial a quitté l’entreprise, la documentation est partielle, et aucune procédure de test ou de versionnage n’a été mise en place. Aujourd’hui, **les bugs se multiplient** : solde incorrect, affichage inadapté sur certains navigateurs, coupures de session fréquentes… L’équipe RH commence à perdre confiance dans l’outil.

En parallèle, de **nouvelles demandes** ont émergé. La direction souhaite intégrer les jours de télétravail au planning, la finance réclame des exports mensuels au format Excel, et la DSI pousse pour une connexion unifiée avec Microsoft 365.

---

Pour couronner le tout, le contrat avec l’hébergeur arrive à échéance dans six mois, et la question de la **maintenabilité** de l’application est désormais stratégique. La direction a décidé de traiter cette problématique en interne, sans recourir à une TMA. Elle mandate une **équipe projet transverse** pour :

- identifier les priorités
- corriger les anomalies les plus critiques
- planifier les évolutions sur 3 mois
- restaurer la confiance des utilisateurs.

Vous faites partie de cette équipe.

### 🖥️ 2. Environnement technique

- **Langage back-end :** PHP 7.4
- **Framework :** Laravel 7 (non maintenu)
- **Base de données :** MySQL
- **Front-end :** HTML/CSS + jQuery
- **Hébergement :** mutualisé OVH
- **Authentification :** interne, non fédérée (login/password)
- **Dépôt Git :** disponible en interne sur GitLab
- **Méthodologie initiale :** cycle en V

---

### 🧑‍💼 3. Équipe projet actuelle

| Rôle                | Nom               | Fonction                     |
| ------------------- | ----------------- | ---------------------------- |
| Référente métier RH | Isabelle Martin   | Responsable RH               |
| Dev interne         | Kévin Dias        | Dev fullstack junior         |
| Responsable infra   | Céline Morel      | Admin système OVH & sécurité |
| Externe             | Aucun prestataire |                              |

---

### ⚠️ 4. Dysfonctionnements signalés (anomalies)

| Réf. Bug | Description                                                                                                             | Impact     | Priorité perçue             |
| -------- | ----------------------------------------------------------------------------------------------------------------------- | ---------- | --------------------------- |
| #BUG001  | Solde de congés incorrect après suppression d’un congé                                                                  | Élevé      | Urgent                      |
| #BUG002  | Déconnexion automatique toutes les 5 minutes                                                                            | Moyen      | Moyenne                     |
| #BUG003  | Affichage du calendrier illisible sous Safari                                                                           | Faible     | Faible                      |
| #BUG004  | "L'application met du temps à s'ouvrir certains matins"                                                                 | Non évalué | Faible (?)                  |
| #BUG005  | Message d'erreur "Accès interdit" lors de la demande de congé annuel (pas toujours reproductible)                       | Élevé      | Basse                       |
| #BUG006  | Erreur 500 après clic rapide sur plusieurs jours du calendrier                                                          | Moyen      | Non remontée officiellement |
| #BUG007  | Le champ “Motif” disparaît si on coche “Télétravail” au lieu de “Congé”                                                 | Faible     | Moyenne                     |
| #BUG008  | Deux collègues ont pu poser un congé le même jour alors que leur manager a activé la règle “1 seule absence par équipe” | Élevé      | Non identifié par RH        |
| #BUG009  | Export PDF illisible (tableau tronqué à droite) quand l’export dépasse une semaine                                      | Moyen      | Urgent (?)                  |
| #BUG010  | Un manager a signalé qu’un congé posé le 1er janvier s’est affiché le 2 janvier dans le récapitulatif                   | Moyen      | Faible                      |

---

### ✨ 5. Demandes d’évolution

| Réf. Evo | Description                                                                                            | Origine              | Statut                           |
| -------- | ------------------------------------------------------------------------------------------------------ | -------------------- | -------------------------------- |
| #EVO001  | Intégration des jours de télétravail au planning (affichage différencié)                               | Direction RH         | À étudier                        |
| #EVO002  | Export Excel mensuel des absences (tri par équipe, type d’absence, dates)                              | Manager Finance      | Demandée                         |
| #EVO003  | Connexion via SSO Microsoft 365 (authentification unique)                                              | DSI                  | Priorisée pour Q4                |
| #EVO004  | Ajout d’un système de validation à deux niveaux (manager + RH) pour les congés longs                   | RH                   | Non planifiée                    |
| #EVO005  | Pouvoir poser des demi-journées de congés (matin/après-midi)                                           | Plusieurs salariés   | Demande récurrente (non cadrée)  |
| #EVO006  | Coloration automatique des jours fériés dans le calendrier                                             | Direction            | Rejetée en 2022 (re-soumise)     |
| #EVO007  | Intégration automatique avec le logiciel de paie Silae                                                 | Responsable Paie     | Complexité technique à clarifier |
| #EVO008  | Notifications email personnalisées (validation, refus, rappel)                                         | RH                   | À documenter                     |
| #EVO009  | Responsive mobile (application difficile à utiliser sur smartphone)                                    | Utilisateurs terrain | Jamais priorisé                  |
| #EVO010  | Possibilité de bloquer les demandes de congés pendant certaines périodes définies (fermeture annuelle) | Direction générale   | Acceptée sous conditions         |

---

### 🛠️ 6. Contraintes et exigences

- **Continuité de service obligatoire** : l’app ne peut être mise hors ligne plus de 2h
- **Pas de budget TMA** : tout doit être internalisé
- **Sensibilité RGPD** : les données RH sont sensibles
- **Attentes métier fortes** : la RH est sous pression pour fiabiliser les absences avant la paie

---

### 🗂️ 7. Livrables attendus des étudiants

1. Synthèse de la situation et priorisation des demandes
2. Proposition de découpage en lots (correctif / évolutif)
3. Plan de maintenance évolutive (jalons, versioning)
4. Stratégie de test (non-régression + sécurité)
5. Document métier à destination de la RH (fiche de prise en charge)
