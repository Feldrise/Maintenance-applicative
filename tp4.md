## 🧪 TP 4 – Tests et stratégie qualité

### 🎯 Objectifs pédagogiques

- Définir des **scénarios de test concrets** à partir des bugs identifiés
- Identifier les **points critiques** de l’application à surveiller en priorité
- Décrire une approche de **tests de sécurité** adaptée au contexte
- Adopter une **démarche de fiabilisation** des livraisons de maintenance

---

### 📘 Contexte du TP

Après avoir construit votre plan de maintenance et défini un PAQ, il est maintenant essentiel de **formaliser une stratégie de test**.

La finalité n’est pas d’implémenter les tests de manière technique, mais de :

- réfléchir aux scénarios à vérifier à chaque version
- repérer les zones sensibles (ex : calcul des soldes, calendrier, export)
- imaginer des **tests de vulnérabilité** simples, accessibles même sans outils spécialisés

L’objectif est de professionnaliser votre démarche de livraison : **tester avant de livrer, valider avant de communiquer.**

---

### 📂 Ressources fournies

- Backlog des bugs (cf TP1)
- Planning des versions (cf TP3)
- Mini PAQ (cf TP3)
- Fiche des bonnes pratiques de test (synthèse)

---

### 📋 Étapes du TP

#### 🧪 Partie 1 : Scénarios de test fonctionnel

- Reprendre 3 à 5 bugs majeurs (#BUG001, #BUG005, #BUG010…)
- Pour chacun, formuler un **scénario de test** clair :

  - Étapes à suivre
  - Comportement attendu
  - Résultat OK / KO

#### 🔍 Partie 2 : Points critiques à surveiller

- Listez les **composants ou fonctionnalités sensibles**

  - Calculs automatiques
  - Export PDF / Excel
  - Planning multi-utilisateur

- Associez à chacun une **vérification systématique**

#### 🔐 Partie 3 : Esquisse de tests sécurité

- Décrire des **vérifications simples de sécurité** :

  - Injection dans les champs (ex : ‘ or 1=1 --)
  - Test de mot de passe vide / double connexion
  - Navigation directe via URL interdite

- Proposer un **outil ou méthode simple** : OWASP ZAP, navigateur, Postman…

---

### 📌 Exemple de tableau attendu

| Test ID | Objectif                          | Type           | Fréquence            | Outil        | Résultat attendu                         |
| ------- | --------------------------------- | -------------- | -------------------- | ------------ | ---------------------------------------- |
| T001    | Vérifier calcul du solde congé    | Fonctionnel    | À chaque version     | Manuel       | Le solde reste correct après suppression |
| T002    | Tester champ motif en télétravail | Fonctionnel    | Hebdomadaire         | Navigateur   | Le champ est visible à chaque fois       |
| T003    | Injection champ “motif”           | Sécurité       | Ponctuel             | OWASP ZAP    | Aucune donnée injectée acceptée          |
| T004    | Export PDF > 7 jours              | Non-régression | À chaque déploiement | Chrome / PDF | Le fichier s’affiche entièrement         |

---

### 🗃️ Livrables attendus

1. **Tableau de stratégie de test** (fonctionnel + sécurité + non-régression)
2. **Exemples de résultats attendus**, explicites (textes ou captures annotées)

---

### ✅ Critères d’évaluation

| Critère                                    | Barème  |
| ------------------------------------------ | ------- |
| Pertinence des scénarios proposés          | /5      |
| Identification correcte des zones à risque | /3      |
| Clarté et rigueur du tableau de tests      | /4      |
| Respect des consignes formelles            | /2      |
| **Total**                                  | **/14** |
