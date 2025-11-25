# **Rapport de Projet \- PoketraFinday**

## **Examen Final Machine Learning & Data Science**

Réalisé au sein de ISPM - Madagascar (www.ispm-edu.com)

### **1\. Informations sur le Groupe**

Merci de lister tous les membres de l'équipe ayant participé au Hackathon.

#### Membre 1 : 
* nom : ARIMALALA  
* prénom(s) : Miarintsoa Itokiana Michael
* classe : ESIIA 5
* numéro : 07
* rôle : *(développeur, analyste, présentateur, ...)*

#### Membre 2 : 
* nom : RAMAMONJISOA
* prénom(s) :  Herilala Julio Gladys
* classe : ESIIA5
* numéro : 25
* rôle : *(développeur, analyste, présentateur, ...)*

#### Membre 3 : 
* nom : SANDROS
* prénom(s) : Junior
* classe : ESIIA5
* numéro : 18
* rôle : *(développeur, analyste, présentateur, ...)*

#### Membre 4 : 
* nom : RAJERISON
* prénom(s) : Hajatiana Olivier 
* classe : ESIIA5
* numéro : 21
* rôle : *(développeur, analyste, présentateur, ...)*

#### Membre 5 : 
* nom : RAJAONAH 
* prénom(s) : Anjara Fanomezantsoa
* classe : ESIIA 5
* numéro : 22
* rôle : *(développeur, analyste, présentateur, ...)*

#### Membre 6 : 
* nom : RAKOTOZAFY
* prénom(s) :Harimanda Zoeliniaina Valerio
* classe : ESIIA 5
* numéro : 14
* rôle : *(développeur, analyste, présentateur, ...)*

#### Membre 7 : 
* nom : ZAFINDRAMALA
* prénom(s) : Ramanantsoa Flavio
* classe : ESIIA 5
* numéro : 23
* rôle : *(développeur, analyste, présentateur, ...)*

### **2\. Résumé du Travail**

Problématique :  
Face à l’augmentation des fraudes ciblant les comptes utilisateurs, comment développer un modèle prédictif fiable capable d’identifier les comportements suspects afin de protéger la plateforme sans nuire aux opérations normales des clients ? 
Méthodologie Adoptée :  
(Résumez votre approche technique : EDA, pré-traitement spécifique, choix des modèles, stratégie de validation).  
Résultats Obtenus :  
(Indiquez votre meilleur F1-Score sur le jeu de validation et mentionnez une découverte clé de votre analyse).  
Mots-clés :  
(Citez 5 mots-clés techniques ou métier, ex: Fraude, Imbalanced Data, XGBoost, ...)

### **3\. Contenu du Repository**

Voici la liste des fichiers et liens importants pour évaluer notre travail :

* **notebook.ipynb** : Le code complet (EDA, Preprocessing, Modélisation) avec commentaires.  
* **submission.csv** : Nos prédictions sur le fichier test.csv.  
* **readme.md** : Ce présent rapport.  
* *(Ajoutez ici d'autres fichiers si nécessaire, ex: requirements.txt)*

**🔗 Liens Utiles :**

* [**LIEN VERS LA VIDÉO DE PRÉSENTATION** (Google Drive / YouTube)](https://www.youtube.com/)  
* [Lien vers d'autres ressources (Optionnel)](https://www.google.com/)

### **4\. Réponses aux Questions d'Analyse**

*Répondez de manière précise aux questions posées dans le sujet. Utilisez des chiffres ou des références à vos graphiques pour justifier vos réponses.*

**Q1. Pourquoi on utilise F1-Score au lieu de accuracy ?**

*car les données sont très déséquilibrées.*

**Q2. Qu'est ce qui est plus grave ici, les Faux Positifs ou les Faux Négatifs ?**

*les Faux Négatifs (FN) sont plus graves que les Faux Positifs.*

**Q3. Stratégie de Modélisation : Quelles nouvelles variables (Feature Engineering) ont le plus amélioré votre modèle par rapport à la Baseline ?**

Les nouvelles caractéristiques ajoutées (Feature Engineering) sont les suivantes : * nb_total_transactions (Fréquence globale des transactions) : Nombre total de transactions effectuées par le client. * avg_amount_customer (Montant moyen historique du client) : Le montant moyen des transactions passées de ce client. * transaction_hour (Heure de la transaction) : L'heure précise à laquelle la transaction a eu lieu (pour capturer les schémas jour/nuit). * is_weekend (Indicateur de fin de semaine) : Une variable binaire indiquant si la transaction a été effectuée durant un week-end (samedi/dimanche).*

**Q4. Enoncez tous les types de fraudes que vous avez décelé lors de votre analyse**

* *TRANSFER*
* *CASH_OUT*

**Q5. Selon vous, quelle décision prendre si une transaction *en cours* est détectée comme *fraude* par le modèle ?**
*Plutôt que d'opter pour une simple décision binaire (Accepter/Refuser), il est crucial d'établir des seuils de risque basés sur la probabilité $\mathbf{P(Fraude)}$ donnée par le modèle.*

### **5\. Bibliographie**
*(si vous avez des livres, liens ou articles qui vous ont servi dans ce travail)*
