Objectif 
Le turnover du personnel (l’abandon du post) est un problème très coûteux pour les entreprises. Le coût de remplacement d'un employé s'il est souvent supérieur à 100 000 USD, compte tenu du temps passé à interviewer et à trouver un remplaçant, des frais de placement, des primes de connexion et la perte de productivité pendant plusieurs mois. 
Comprendre pourquoi et quand les employés sont les plus susceptibles de quitter peut conduire à des actions pour améliorer la rétention des employés ainsi que planifier de nouvelles embauches à l'avance.
Dans ce défi, vous disposez d'un ensemble de données avec des informations sur les employés et devez prévoir quand les employés vont quitter en comprenant les principaux facteurs de désabonnement des employés.
Données 
Vous avez les données sur les employés de quelques entreprises. Vous avez les données sur tous les employés qui se sont joints à partir 24/01/2011 au 13/12/2015. Pour chaque employé, nous savons également s'il est toujours dans l'entreprise au 13/12/2015 ou s'il a démissionné. Aussi, vous avez des informations générales sur l'employée, telles que le salaire moyen pendant son mandat, son département et ses années d'expérience. 
Colonnes:
employee_id: id de l'employé. Unique par employé par entreprise
company_id: id de l'entreprise.
dept: département des employés
seniority: nombre d'années d'expérience de travail au moment de l'embauche
salary: salaire annuel moyen du salarié pendant son mandat au sein de l'entreprise
join_date: lorsque l'employé a rejoint l'entreprise, cela ne peut se faire qu'entre le 24/01/2011 et le 13/12/2015
quit_date: date à laquelle l'employé a quitté son emploi (si il est toujours employé au 13/12/2015, ce champ est NA)
churn : yes si l'employé a quitté son emploi, No au cas où il est toujours dans l’entreprise.
duration_days : durée en jours entre join_date et quit_date 
Enoncé 
	•	Prétraitement de données
	•	Uniformiser les titres de colonnes en des noms minuscules 
	•	Vérifier les types de données des colonnes
	•	Transformer join_date et quit_date en des dates
	•	Eliminer les valeurs manquantes pour l’attribue « salary »
	•	Changer le type de l’attribue « salary » à float

	•	Description
	•	Générer une description du jeu de données (nombre de lignes, de colonnes)
	•	Identifier les principales caractéristiques statistiques du jeu de données (Count, Mean, std, min, max, 25%,50%,75%.
	•	Supposons, pour chaque entreprise, que les effectifs commencent à zéro le 23/01/2011. Quelle est l’estimation des effectifs, pour chaque entreprise, chaque jour, du 24/01/2011 au 13/12/2015. (company_id, join_date, count_employee)
	•	Obtenir le nombre de nouveaux employés chaque jour pour chaque entreprise (company_id, join_date, count_new_hire)
	•	Obtenir le nombre d’employés ayant quitté chaque entreprise chaque jour (company_id, join_date, count_churn)
	•	Tracer en boxplot la distribution churn / salary
	•	Classification 
	•	Créer un arbre de décision pour classifier les contributeurs selon churn (Yes ou No) avec comme attributs d’entrés seniority, salary
NB : suivre les étapes de la classification à l’aide d’un arbre de décision (Training/test, classification, évaluation, et performance [« Accuracy score » et « Confusion Matrix »]) 
	•	Classifier les employés selon churn (Yes ou No) utilisant KNN à l’aide de la cross validation 
	•	Reporter la performance du KNN  
	•	Prédiction 
	•	Réaliser une régression linéaire pour prédire la duration en jours en fonction des attributs d’entrés seniority, salary
	•	Prédire la duration en jour pour l’employé x salary=9800 et seniority=25
