+++
date = '2024-11-19T09:55:56+01:00'
draft = false
title = 'Mob Programming'
+++

## Genesis
At the very beginning, each developer was behind his own computer in his garage or whatever room they liked to be in. There were very few of them because affording a computer was far from how easy it is today.

Years passed and companies started to show needs for software development. Developers were hired to work on projects in the same place. Development became a team activity. Hurray !

These developers had to organize their work in a way the would be efficient. 

-- share file with hard disk

-- Git appeared, PR (mainly for OSS projects)

-- mob programming appears

Tous ces concepts étaient complexes pour partager le travail d'équipe. Un jour, quelqu'un a eu l'idée de simplifier ce process en faisant travailler les développeurs ensemble, sur le même clavier et le même écran. Le mob programming était né.

Et enfin, avec Internet, le remote mob programming a vu le jour.

But did it really ?

## Why do we choose mob programming ?

Manque de compétence
Panel d'expertise bien plus large.
  > Jonathan: Personnellement, j'étais dans l'incapacité de réaliser un projet de A à Z (back, front, CI/CD, déploiement/hébergement, sécurité, etc.). En voyant les offres d'emploi pour du dév, c'est souvent le mouton à 5 pattes qui est attendu 🐑. Il y a trop de compétences attendues dans une fiche de poste. On peut avoir survolé mais sans maîtriser les compétences demandées. Maîtriser ces compétences est impossible pour une personne [normale] - Jonathan

  > Dimitri: De mon côté, je cherche à avoir de l'homogénéité au sein de l'équipe. Je suis fatigué de devoir répété des choix de design qui ont été pris avec une partie des membres de l'équipe mais pas tout le monde. J'aime comprendre aussi pourquoi certains choix ont été fait donc je vais à mon tour demander ce qui a motivé tel ou tel choix. - Dimitri

D'autres citation pour évoquer d'autres problèmes ?
  > D : Pratiques !=. Comment se synchro / se mettre d'accord
  > J : Besoin de trop d'interactions entre les différentes personnes. On adresse trop de sujet en même temps. On avance pas tous au même rythme 

  > D : Je suis pas bon en front -> Je laisse à quelque d'autre le travail vs je bosse avec cette autre personne qui me mentore et partage son savoir de manière synchrone
  > J : QUand la personne avec la connaissance n'est pas présente, le projet stagne / je suis dans la galère / pas efficace

  > JLA : Daily sans réellement s'écouter car on s'adresse à des personnes pas concernées. Je bosse sur la fonctionnalité F, si Bernand ne la connait, il va m'écouter un peu sans comprendre exactement ce dont je parle. Au final, il a perdu du temps et moi aussi
  > DKO : Point de synchro sur "je viens de faire ça pour info, ça ressembler à ça". Quand un dév bosse sur une fonctionnalité et pas moi, je n'ai pas la maîtrise du sujet donc suis dans l'incapacité de gérer la prod de cette feat 

  > JLA : Lorsqu'il y a un soucis, on passe plus de temps à trouver le responsable qu'à résoudre le problème
  > DKO : Lorsqu'il y a un soucis et que toute l'équipe ne participe pas à la résolution, certains choix / compromis aurient pu être [meilleur].

--- Idée : switch les quotes en fausse conversation
Le mob programming répond à cette problématique d'optenir "un" dév qui sache adresser un scope plus large
Tout le monde connait le projet.
On apprend tous en même temps.
Les décisions sont prises au fil de l'eau
L'ownership est à l'équipe.

On commence et termine une seule chose à la fois.
L'équipe entière est responsable du focus de l'équipe (toujours quelqu'un pour faire timekeeper / focus keeper)

Il y a toujours au moins une personne pour soutenir le rythme de l'équipe.
Plus rigoureux.
Pas de démotivation / d'épuisement.

On sait tous où on en est.
Pas besoin de faire de réunion / point d'étape asynchrone
Onboarding très rapide.
Chacun peut aller et venir en fonction de prios et de agendas de chacun
Problématique: Pas de dispo à 100% prévu


## For which activity

Dev (évidemment)
Priorisation des tâches au sein d'une mission
Construction d'un devis / répondre à un prospect
Organisation / structuration du collectif.
Ce n'est pas une personne qui pour tout le monde et on prend une décision qu'à partir de 3 personnes présentes. Pour autant, on attend pas les absents (sinon ça ralentirait la construction)
S'essayer à l'écriture d'article (au hasard :D)
Optimiser nos profiles LinkedIn et autres
Organisation d'événements
Post LinkedIn ? Ca reste un branding individuel même si une partie du branding collectif peut être derrière :)


## How
### Les moyens techniques

partage de code : LiveShare, CodeWithMe
partage d'écran : Discord / RustDesk
Vocal: Discord / meet ponctuel avec les prospects / clients
Note: Framapad / TODO.md
Code: Git, mob.sh, timer (navigator / pilot)

### La méthode
Timeboxing avec souplesse (laisse le pilote termienr l'écriture de sa ligne de cas de test par ex et le navigateur finir son flow de pensée)
Switch régulier navigator / pilot.
On switche toujours dans un état maîtrisé (rouge ou vert)
Assigner des rôles à chacun (timekeeper, ). 
S'assurer que chacun participe activement : la loi des deux pieds 


## Who talks about Software Teaming
Woody Zuill (son bouquin) & Kevin Meadows
Chris Pipito (regular free event brite session). [[[Next is scheduled on 12/5 -> Move this on in LI post and outside article]]]
Manon Carbonnel : https://www.linkedin.com/in/manon-carbonnel/ Elle intervient souvent dans les con
Marjorie Aubert : https://www.linkedin.com/in/marjorie-aubert-full-stack-developer/ Elle a commencé le développement directement dans une équipe pratiquant le mob et elle partage son expérience durant les conférences. 

Emily Bache (méthode samman)



## How to start

Vous pouvez aussi trouver des meetup qui organisent des coding dojo. Il y en a dans chaque grande ville. Lors de ces coding dojo, il est courant de le faire en mob programming.

Enfin, le meilleur endroit, c'est au sein de votre équipe. Vous pouvez commencer dès maintenant et si la mise en place est trop compliquée, il y a plusieurs coach techniques qui pourraient vous accompagner.

Pas encore chaud de faire ça dans votre équipe ? Venez sur le collectif (lien discord ou pas ?) et on se fait une session ensemble.

## Aller plus loin
Nous rejoindre sur le discord : https://discord.gg/Z7GeFzpZBT
https://github.com/willemlarsen/mobprogrammingrpg/blob/master/rpg_roles_plain_text.md
