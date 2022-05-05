# Readme ecrit par MOSBAH Yasmin

- Projet réalisé lors du cours d'Agent conversationnel, dirigé par **Madame Célia Pereira**. 


# Agents Aspirateurs :

> Les détails sur les agents aspirateurs sont décrits sur le code. J'ai choisit le format jupyter pour pouvoir commenter chaque detail important.

##### Liste des fonctionnalités générales : 

- Fonction qui génère le taux de poussière dans chaque  piece et qui déclanche le changement de sac a poussière de l'aspirateur(**randompouss(init)**). 
Une fonction appliqué a tout mes agents

## Agents aspirateur simple.
Cet aspirateur va nettoyer la piece si elle est sale, ou changer de piece si elle est propre. Il va changer son sac a poussière si il est pleins. 

- Fonction qui génère l'état de manière random dans chaque piece ici il y en a seulement 2 (**randomrooms()**).


![EXEMPLE1](./IMAGES/agent_simple.png)

## Agents aspirateur avec etat interne.

Cet aspirateur va nettoyer la piece si elle est sale, mais si elle est propre il change de pièce. Il agit exactement comme le précédent aspirateur mais cette fois il va se souvenir qu'il a nettoyer une salle. Il aura une mémoire ! Il change également son sac a poussière. 

![EXEMPLE2](./IMAGES/agent_simple_memoire.png)

## Agents aspirateur reflexe. 

Cet aspirateur va attérire dans une salle de manière aléatoire, et il aura pour but d'aller dans la dernière piece du chemin en nettoyant tout sur son passage. Il change également son sac a poussière. 

- Fonction qui permet de générer la liste des chemins (**chemin_generator(salles,nb)**)

- Fonction qui génère l'état de manière random dans chaque piece mais cette fois on a le choix du nombre de pieces (**randomroomsnb(nbsalles)**).

![EXEMPLE3](./IMAGES/agent_reflexe.png)



## Agents aspirateur réflexes avec une fonction d'utilité
Il a comme but d'arriver a la dernière piece en nettoyant toutes les pieces sur son passage. Mais cette fois-ci en choisissant le chemin le plus court. Ici il choissira le chemin ou il y a le moins de piece sale. Il change également son sac a poussière. 

- Fonction qui va choisir le chemin le plus optimale en fonction du nombre de pièce sales(**choix__chemin(salles,chemins)**). 

![EXEMPLE4](./IMAGES/agent_but.png)


## Eliza

> Eliza est un chatbot qui simule le travail d'un psychotérapeute qui reformule les phrases de ses patients.

> Ma Eliza part initialement du tutoriel Datacamp. Son code initial ne mes pas propres car c'est ce tutoriel qui m'a guidé. Par la suite, il nous a été demandé de la personnalisé. 

> Alors voilà la liste des fonctionnalités que je lui ai ajouté :  

  - Le premier ajout a été celui de sa mémoire. Lors de l'échange, ma Eliza va enregistrer dans une liste toutes les informations dites par le patient. Ainsi, elle pourra lui demander plus de détail par la suite. 
  
  - Etant donnée que c'est une Eliza personnalisé et que je suis de la génération qui utilise des smileys pour tout et rien.. Je lui ai donné l'option d'ajouter des smiley a la fin de ses phrases. Les smileys sont choisit de manière aléatoire car elle n'a pas la capacité d'analiser les sentiements de son patient.
  
  - Ma Eliza est réellement désireurse de mieux connaitre son interloccuteurs, donc avant de commencer toute discussion elle lui demande son prenom et elle se présente ensuite. 
  
  - Lorsque son prénom est récupéré, elle change le template "user" avec le prenom du patient. 
  
  - Enfin, je lui ai ajouté une plus grand dictionnaire. 


### Exemple d'échange avec Eliza : 
![EXEMPLEELIZA](./IMAGES/eliza.png)

## Parry
> Parry est une ELiza mais avec une personnalité propre. On se rapproche donc d'un chat bot avec plus "d'humanité". 

> Ma parry est une evolution logique de ma Eliza décrite juste au dessus mais avec encore une fois des fonctionnalités bien différentes. 

> Voilà la liste :

- Tout d'abord ma Parry a la capacité de detecter l'intention de la personne qui lui parle. L'intention sera idéntifié en fonction de mots clés, de ponctuations, etc..

- En fonction de l'intention de l'interlocuteur, Parry agira différement. Pour cela elle un dictionnaire pour chaque humeur, une liste de smiley egalement pour chaque humeur. 

- Si parry est trop enervé, elle va se mettre a raconter sa propre vie en ignorant son interlocuteur.

- Parry est une adolecente, elle est fan d'un chanteur (Kai) et elle deteste ses concurrents (BTS). Si on lui parle de son chanteur elle devient surexcitée et joyeuse, par contre si on parle de ses concurrents elle s'enerve. 

- Parry a la phobie de l'eau. Elle pense qu'un requin peut surgir de n'importe où si y a de l'eau..

- Parry donne des surnoms mignons si elle est heureuse. 

- Parry a tellement peur de la mafia, que quand on lui parle de ça elle se met a parler Italien (sa langue natale) car elle veut éviter le sujet.

- Parry sait si on lui parle anglais ou non. Grace a la librairie NLTK, Parry a la capacité de savoir en quelle langue on lui parle.


### Exemple d'échange avec Parry : 

#### Parry neutre :
Lorsque Parry ets neutre, elle est plutot normal.. Elle a un grand dictionnaire pour pouvoir parler de tout et rien, elle pose des qestions un peu comme ELiza. On voit tout de même sa réaction etrange lorsqu'on lui parle de la mafia, ou son excitement pour Kai.. ET la manière dont elle ne veut pas parler de BTS.

![EXEMPLEJOHNNY1](./IMAGES/parryneutre.png)

#### Parry heureuse :
Ici elle est heureuse, elle donne des surnom, ses smileys sont plutot joyeux et elle met des petites vagues a la fin de ses phrases comme si elle "chantait". 

![EXEMPLEJOHNNY1](./IMAGES/parryhappy.png)

#### Parry énervé:
Ici Parry est énérvée, elle n'ecoute plus son interlocuteur. Elle est désagreable et elle finit même par se venter en rabaissant la personne en face. Ses smileys sont plutot mauvais. 

![EXEMPLEJOHNNY1](./IMAGES/parryangry.png)

####  Test Parry : 
Ici je commence une conversation avec Perry qui est plutot neutre, et je la rends joyeuse en lui parlant de Kai, de choses joyeuses, je lui fais des compliments. Suite a cela, on voit qu'elle met des smileys plus joyeux, des surnoms (comme montré précédement).

Ensuite je décide de l'énerver en lui parlant de mafia, d'hommes, du corona, de trump, de bts et elle s'enerve et commence a devenir désagreable. Ses smileys sont méchants et elle parle même en masjusculte pour me hurler dessus. 

![EXEMPLEJOHNNY1](./IMAGES/testparry.png)

## Agent achat de billet d'avion (Johnny)

> Mon agent s'appelle Johnny, il n'est pas un agent conversationnel a base de régles. Il fonctionne par étapes, on son but est de collecter les informations nécessaire pour acheter un billet d'avion pour l'interlocuteur. 
> Il va commencer par demander le prenom de son interlocuteur, il va poser les questions dans l'ordre et demander si tout est bon. Si ce n'est pas le cas il va recommencer. 


Johnny n'est pas si bête que ça, il a la capacité de reconnaitre n'importe quelle date et ça peut importe dans quelle forme elle est écrite.
Il a aussi la capacité de savoir si on lui fournit une vraie localisation. 

### Exemple d'échange avec Johnny : 

![EXEMPLEJOHNNY1](./IMAGES/johnny1.png)
![EXEMPLEJOHNNY1](./IMAGES/johnny2.png)