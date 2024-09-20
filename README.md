# 420-SF1-RE-A24-TP1
Travail pratique 1 du cours 420-SF1-RE A24

# Travail pratique 1

# Sommaire
Le travail pratique 1 est divisé en 4 parties. Chaque partie est un exercice à part entière et doit être complétée dans un fichier séparé. Les parties sont les suivantes:
1. Validateur d'adresses courriel
2. Mot à deviner
3. Déchiffrer la combinaison
4. Calibrer la machine à danser

Ce travail pratique compte pour 15% de la note finale. Voir le barême de correction plus bas.

# Constitution des équipes et mise en place du TP
Ce travail s'effectue en équipe de 2 personnes.
Un lien pour Github classroom vous sera envoyé par MIO. Il vous permettra de créer une nouvelle équipe ou joindre une équipe existante.

Une fois l'équipe créée, Github classroom va créer un dépôt que vous pourrez accéder à partir de votre compte Github. Le lien du dépôt apparaît aussi dans github classroom.

- chaque coéquipier peut cloner le dépôt pour travailler sur le TP.
- Écrivez votre code dans les fichiers appropriés
- N'oubliez pas d'inscrire vos noms et utilisateurs Github dans l'entête des fichiers.
- Faire un "commit" va créer une révision locale sur votre ordinateur.
- Le "push" permet d'envoyer les commits sur le serveur distant
  - Ceci veut dire que vous pouvez faire la remise au fur et à mesure.
    - Chaque "push" fait la remise de vos commits locaux
  - La correction se fera sur la version du code présente dans le dépôt au moment de l'échéance de la remise.
  - Pas de remise par LÉA


# Exercices

## Exercice 1 - Validateur d'adresses courriel
**Objectifs: manipulation de chaînes de caractères, structures conditionnelles, entrées et sorties**

Vous devez demander à un utilisateur de saisir son nom, son prénom et son adresse courriel. Puis vous dites si l’adresse courriel est valide ou pas.

Une adresse courriel est valide si :
- elle contient un seul @
- elle se termine par .com ou par .ca
- elle ne contient qu’un seul .com ou .ca

Vous devez par la suite dire à l’utilisateur si son adresse courriel est valide ou pas. Si l’adresse est valide, vous devez générer un mot de passe pour cette adresse. Le mot de passe est formé de :
- Les deux premières lettres du nom en majuscule
- Les 3 dernières lettres du prénom en minuscule
- Le tout suivi de _2024

Voici un exemple (vous devez présenter les mêmes messages **en gras** à l'utilisateur)


*exécution 1 :*
>**Donner votre nom :** Boushaba  
>**Donner votre prénom :** Mustapha  
>**Donner votre adresse courriel :** mustapha@boushaba.ca 

Après saisie des informations, voici ce qu’on doit recevoir : 
>**Mustapha Boushaba, votre adresse mustapha@boushaba.ca est valide. Votre mot de passe est : BOpha_2024**


*exécution 2 :*
>**Donner votre nom :** Barre  
>**Donner votre prénom :** Alain  
>**Donner votre adresse courriel :** barre@alain.bm 

Après saisie des informations, voici ce dont on doit recevoir le message:

>**Alain Barre, votre adresse barre@alain.bm n’est valide**


## Exercice 2 - Mot à deviner
**Objectifs: manipulation de chaînes de caractères, structures conditionnelles, entrées et sorties, structures répétitives**

Soit une liste de mot que vous allez définir préalablement dans votre programme. Exemple :
>mots = ["banane", "fleur", "chat", "ordinateur", "python"]

Vous allez choisir un mot aléatoirement et demander à l’utilisateur de deviner les caractères formant le mot. Vous devez avant tout donner la taille du mot à deviner à l’utilisateur et il a le droit au maximum à 3 erreurs.

*Exemple : supposant que la machine choisie le mot fleur
Voici ce qu’on affiche à l’utilisateur :*

>Le mot est formé de 5 lettres.
>Choisissez votre lettre : e
>Choisissez la position : 0

Pour l’utilisateur, il va saisir la lettre et la position où elle se trouve. Comme le mot fleur commence par un *f* à la position *0*, l’utilisateur a commis donc une première erreur.
Puis, on continue à demander à l’utilisateur de deviner la lettre et la position de la lettre (je vous rappelle que la position 0 est la première position du mot).
Le jeu s’arrête quand l’utilisateur trouve tous les caractères du mot et on lui affiche dans ce cas:  
**bravo : vous avez deviné le mot.**   
Sinon, quand le joueur atteint le maximum d’erreurs et on lui dit:  
**Bonne chance pour la prochaine fois.**

## Exercice 3 - Déchiffrer la/les combinaison(s) du coffre
**Objectifs: manipulation de chaînes de caractères, structures conditionnelles, entrées et sorties, structures répétitives, utilisation de la bibliothèque math, utilisation des nombres**

Un coffre est fermé sur un trésor. On vous demande de trouver la ou les bonnes combinaisons pouvant ouvrir le coffre en respectant les conditions suivantes :
- Je suis un nombre de 4 chiffres entre 1000 et 9999
- Le premier chiffre est le double du deuxième
- Le troisième chiffre est la moitié du premier
- La somme des quatre chiffres est 12

Écrire un code en python vous permettant de trouver et d’afficher la/les bonne(s) combinaison(s).


## Exercice 4 - Calibrer la machine à danser
**Objectifs: manipulation de chaînes de caractères, structures conditionnelles, structures répétitives, utilisation de la bibliothèque math, utilisation des nombres**

La machine à danser est une machine qui permet de générer de la musique pour un party mémorable. Malheureusement, elle doit
être calibrée pour réaligner les mécanismes qui se sont déplacés durant le transport. Les calibrations pour les 5 mécanismes sont
fournies dans une liste de spécifications. Cette liste est constituée de 5 chaînes de caractères contenant des chiffres et des lettres.

Pour trouver tous les paramètres de calibration, vous devez:
- déchiffrer chaque spécification
  - Vous devez extraire le premier chiffre à partir du début de la chaîne de caractères et le premier chiffre à partir de la fin de la chaîne de caractères.
    - Par exemple, si on a la liste de spécifications suivantes:
> specifcations = [ "3dlamuze49", "danser5souqu3r", "r0ckmo1ca7", "m3tal666", "beat8beat"]  
Les spécifications correspondantes seront: 39, 53, 07, 36, 88

- calculer la moyenne des spécifications
- calculer l'écart type des spécifications
  - Petit rappel sur l'écart type: [Écart typer sur alloprof](https://alloprof.qc.ca/fr/eleves/bv/mathematiques/l-ecart-type-m1508)

- Vous devez afficher les nombres des spécifications sur la première ligne en les séparant d'un espace
- Vous devez afficher la moyenne sur la deuxième ligne
- Vous devez afficher l'écart type sur la troisième ligne

# Barême de correction
- Chaque exercice compte pour 25% du TP
- Pour chaque exercice, la correction se décline comme suit:
  - 50% Fonctionnement du code
    - Votre code va être testé avec plusieurs valeurs d'entrée. Si certaines réponses ne sont pas valides, vous allez perdre des points. En revanche, si votre code fonctionne à merveille, vous allez avoir tous vos points! Je vous conseille de bien tester votre programme
  - 10% Commentaires
    - Avez-vous mis suffisamment de commentaires ? Vous devez en mettre quelques-uns à des endroits clés, de façon à expliquer le fonctionnement global du programme. Attention : si vous mettez trop de commentaires, vous n'allez pas avoir tous vos points dans cette section.
  - 10% pour le respect des affichages demandés
  - 40% Beauté du code
    - Plus votre code est simple et facile à lire, plus vous allez avoir de points ! Voici des éléments qui contribuent à la beauté d'un code :
      - Est-ce que vos noms de variable sont descriptifs de leur utilisation ?
      - Est-ce que vous aérez vos expressions ?
        - Utilisez-vous des variables inutiles ? Évitez-vous la répétition de code ?
      - Est-ce que votre code est concis ?
      - Respectez-vous les [PEP-008](https://peps.python.org/pep-0008/)
        - PyCharm vous affiche des lignes jaunes brisées si les PEP-0008 ne sont pas respectés
          - ex: 
            - trop de lignes vides ou pas assez lignes vides entre les blocs de code
            - respecter la convention de nommage des fonctions (snake_case)
            - la position des imports dans le fichier
          - PyCharm vous propose de les corriger pour vous si vous survoler la ligne jaune brisée 
      - Votre code est-il facilement adaptable à d'autres situations ?

