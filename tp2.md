## 🧪 TP 2 – Structuration des demandes de maintenance

### 🕒 Durée estimée : 2h

---

### 🎯 Objectifs pédagogiques

- Prioriser les demandes de maintenance selon leur criticité
- Regrouper les corrections et évolutions en **lots cohérents**
- Élaborer un premier **plan de versioning réaliste** (v1.1, v1.2…)

---

### 📘 Contexte du TP

À partir des **anomalies et évolutions identifiées** dans le TP 1, vous êtes désormais chargés de structurer les actions à mener de manière progressive.

L’objectif est double :

1. **Répondre rapidement aux urgences RH** sans interrompre le service
2. **Planifier les évolutions** pour redonner confiance aux utilisateurs et à la direction

Vous devez proposer une structuration claire du backlog en **lots de maintenance** (corrective et évolutive), et établir une projection en **versions successives**.

---

### 📂 Ressources fournies

- Résultat du TP 1 : tableau des anomalies et évolutions
- Rappel des contraintes (ex. : pas de TMA, temps limité, priorité à la RH)
- Exemples de versioning agile (v1.1, v1.2, etc.)
- Dossier projet "GestConge" (enrichi)

---

### 📋 Étapes du TP

#### 🧮 Partie 1 : Priorisation des demandes

- Classez chaque **anomalie et évolution** selon 3 niveaux :

  - Critique (impact fort, à traiter immédiatement)
  - Importante (à planifier à court terme)
  - Secondaire (à discuter ou reporter)

- Appuyez-vous sur les **impacts métier** et le **niveau d’urgence perçu**

#### 📦 Partie 2 : Regroupement en lots

- Créez **2 à 3 lots de maintenance** logiques (ex : "Bug RH urgents", "Améliorations planning", "Sécurité & UX")
- Distinguez maintenance **corrective** et **évolutive**

#### 📅 Partie 3 : Proposition de versioning

- Associez à chaque lot une **version cible** : v1.1 (urgence), v1.2 (fonctionnel), v1.3 (long terme…)
- Estimez un ordre de passage réaliste en tenant compte des ressources internes (Kevin Dias seul en dev)

---

### 📌 Exemples de structuration attendue

#### 📊 Backlog priorisé (extrait)

| Réf.    | Type       | Criticité  | Lot      | Version |
| ------- | ---------- | ---------- | -------- | ------- |
| #BUG001 | Corrective | Critique   | Bugs RH  | v1.1    |
| #BUG005 | Corrective | Critique   | Bugs RH  | v1.1    |
| #EVO001 | Évolutive  | Importante | Planning | v1.2    |

#### 🗓️ Plan de versions (extrait)

| Version | Objectif principal         | Contenu                   | Échéance visée |
| ------- | -------------------------- | ------------------------- | -------------- |
| v1.1    | Stabilisation              | #BUG001, #BUG005, #BUG009 | D+7 jours      |
| v1.2    | Amélioration fonctionnelle | #EVO001, #EVO002, #BUG003 | D+3 semaines   |

---

### 🗃️ Livrables attendus

1. **Backlog priorisé complet** (Excel ou tableau structuré)
2. **Plan de versioning synthétique**, sous forme de tableau ou frise temporelle

---

### ✅ Critères d’évaluation

| Critère                                  | Barème  |
| ---------------------------------------- | ------- |
| Pertinence de la priorisation            | /4      |
| Cohérence des regroupements en lots      | /4      |
| Réalisme du plan de versioning proposé   | /4      |
| Clarté et lisibilité des supports rendus | /2      |
| **Total**                                | **/14** |
