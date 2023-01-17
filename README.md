## Java Spring Boot | template coding
Dans ce repo, je vous présente mon template coding pendant mes développments dans un projet.

### Contexte
---
Un code propre est un code facile à comprendre, facile à modifier et facile à entretenir. Le travail d'un développeur n'est pas terminé lorsque l'application fonctionne comme prévu mais lorsque le code est si simple et propre que n'importe qui peut l'utiliser, le modifier et le maintenir sans lire la moindre documentation.

### Approches
---
*NB : Cette liste n'est pas forcement en ordre, c'est juste une checklist globale.*
- **Partie fonctionnelle**
	- Identifier et comprendre les besoins ou les exigences
	- Quelles sont les règles de gestion
	- Poser des questions pour savoir la logique métier de l'exigence : pourquoi, comment, si....
- **Partie technique***
	- Conception diagramme de classe
	- Validation d'approche pour la réalisation des exigences
	- Créer un diagramme de séquence ou activité ou un document qui explique les étapes de réalisation si besoins
	- Dans code métier :
		- Utilisez des conventions de dénomination appropriées et cohérentes (classe, méthode, variable, etc)
			- Pour les variables et les méthodes, la convention est d'écrire en minuscule camelCase ex : private String movieTitle(), String anotherString
			- Pour les variables constantes, utilisez le cas du serpent hurlant (en majuscule), par exemple : PI_VALUE
			- Pour les classes, les interfaces, les énumérations, les enregistrements, les annotations, utilisez PascalCase, par exemple : public class CodeEncryptor
			- Pour les packages et les fichiers de propriétés, utilisez la casse minuscule, par exemple : java.net.http, com.company.splitter, application.properties
		- Utilisez les modificateurs d'accès et l'encapsulation appropriés
		- Faire toujours le plus simple
		- Penser toujours des codes optimals pour avoir une rapidité
		- Respecter les concepts SOLID
		- Decouper en plusieurs fonctions/méthodes si le code métier est complexe
		- Encapsuler les paramètres de la méthode : les méthodes ne doivent pas avoir trop de paramètres, généralement pas plus de 3 ou 4
		- Vérifier toujours un objet avant de l'utiliser pour éviter l'erreur NPE
		- Si une liste est vide, retourne `Collection.isEmpty()` au lieu de renvoyer des éléments nuls. C'est une meilleure façon de décider si un type de collection est vide.
		- Eviter au maximum le boucle pour avoir une performance et rapidité sur l'API
		- Il est recommandé de réaliser le besoins/exigence dans la requête de la base de données pour éviter le boucle dans le code métier
		- Utiliser l'injection de dependance par constructeur
		- Ne retourne que les données demandés
		- Identifier les types d'attribut optimal (boolean, int, enum, timestamp, etc) pour certains champs
		- Utiliser le bloc try/catch avec log @Slf4j. Ne laissez pas les blocs catch vides sans raison, ce qui rendra le débogage plus difficile et chronophage sans raison.
		- Utiliser Lombok
		- Indexer les champs nécessaires
		- Avec MongoDB respecter toujours l'ordre de la requête ESR (Equality, Sort, Range)
		- Avec MongoDB éviter l'utilisation lookup/jointure sur des gros volumes de données. Faire un process 2 temps si besoins
		- Ne remplacez pas les bibliothèques existantes par vos propres outils
		- Rédigez des commentaires et donnez-leur du sens
		- Gardez un œil sur les avertissements IDE
		- Tester tous les scénarios possibles d'un API
