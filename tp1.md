## 🧪 TP 1 – Lecture et compréhension du contexte applicatif

### 🎯 Objectifs pédagogiques

- Lire et comprendre une fiche projet et ses enjeux métiers
- Identifier les types de maintenance à envisager (corrective, évolutive)
- Reformuler les demandes de maintenance en termes métier et technique

---

### 📘 Contexte du TP

Vous êtes intégrés à une équipe projet en charge de remettre à niveau l’application RH **GestConge**, utilisée en interne par l’entreprise **NexaGroup**.

L’application souffre aujourd’hui de **dysfonctionnements critiques** et doit également intégrer de **nouvelles fonctionnalités** demandées par la RH et la direction.
Vous allez analyser les éléments fournis dans le **dossier fil rouge** pour dégager les premiers besoins de maintenance.

---

### 📂 Ressources fournies

- Dossier complet "Projet GestConge" (fiche entreprise, fiche applicative, historique des bugs, demandes RH)
- Synthèse organisationnelle et technique
- Fiche des acteurs projet

---

### 📋 Étapes du TP

#### 👀 Partie 1 : Lecture du dossier

- Lire attentivement la fiche projet et les documents joints
- Repérer les éléments techniques et fonctionnels clés
- Identifier les acteurs métier et les contraintes organisationnelles

#### 🐞 Partie 2 : Recensement des besoins

- Extraire les anomalies (#BUG001 à #BUG003)
- Lister les demandes d’évolution (#EVO001 à #EVO003)
- Préciser leur origine, leur impact et leur urgence

#### 🧠 Partie 3 : Reformulation métier & technique

- Pour chaque élément, proposer une double lecture :

  - Formulation **métier** : comment l’utilisateur exprimerait le besoin
  - Formulation **technique** : comment l’équipe de développement le comprend

---

### 📌 Exemple de tableau attendu

| Réf.   | Type       | Description (métier)                                     | Reformulation technique                        | Impact |
| ------ | ---------- | -------------------------------------------------------- | ---------------------------------------------- | ------ |
| BUG001 | Corrective | "Le solde de congés est faux après modification"         | Mauvaise gestion des annulations en BDD        | Élevé  |
| EVO001 | Évolutive  | "On veut voir les jours de télétravail dans le planning" | Ajouter un type d’absence + affichage planning | Moyen  |

---

### 🗃️ Livrables attendus

1. **Tableau de synthèse** des anomalies et évolutions (tableur ou tableau formaté)
2. **Note synthétique (max 1 page)** présentant votre compréhension globale du projet :

   - Objectifs de l'application
   - Problèmes prioritaires
   - Enjeux métier identifiés

---

### ✅ Critères d’évaluation

| Critère                         | Barème |
| ------------------------------- | ------ |
| Exhaustivité du tableau         | /4     |
| Pertinence des reformulations   | /4     |
| Clarté de la note de synthèse   | /4     |
| Respect des consignes formelles | /2     |
| Total                           | /14    |
