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

Instead of coming up with a list of all reasons for why we choose mob programming, let's dig into a common situation you might have encountered in the past.

> **Jonathan**: Hey, I recently went through job offers here and there and the only thing I saw is that everyone one is looking for unicorns 🦄. They all want us to be able to work on the backend, frontend, CI/CD, build and host the infrastructure, security, GPDR, and so on. How could one normal person truly master all these skills? I can master few but only scratch the surface of the other ones. It's quite a journey. 
>
> **Dimitri**: I get it. They don't want, or don't have the budget, to hire 5 persons. Depending on the project, infrastructure might just be a thing they need to address at the very beginning but won't see a lot of work afterwards. Look, when the CI is in place, it mostly don't change. Few optimizations here and there but that's basically it, right?
>
>  when De mon côté, je cherche à avoir de l'homogénéité au sein de l'équipe. Je suis fatigué de devoir répété des choix de design qui ont été pris avec une partie des membres de l'équipe mais pas tout le monde. J'aime comprendre aussi pourquoi certains choix ont été fait donc je vais à mon tour demander ce qui a motivé tel ou tel choix. - Dimitri
>
> **Dimitri**: Pratiques !=. Comment se synchro / se mettre d'accord
>
> **Jonathan**: Besoin de trop d'interactions entre les différentes personnes. On adresse trop de sujet en même temps. On avance pas tous au même rythme 
>
> **Dimitri**: Je suis pas bon en front -> Je laisse à quelque d'autre le travail vs je bosse avec cette autre personne qui me mentore et partage son savoir de manière synchrone
>
> **Jonathan**: QUand la personne avec la connaissance n'est pas présente, le projet stagne / je suis dans la galère / pas efficace
>
> **Jonathan**: Daily sans réellement s'écouter car on s'adresse à des personnes pas concernées. Je bosse sur la fonctionnalité F, si Bernand ne la connait, il va m'écouter un peu sans comprendre exactement ce dont je parle. Au final, il a perdu du temps et moi aussi
>
> **Dimitri**: Point de synchro sur "je viens de faire ça pour info, ça ressembler à ça". Quand un dév bosse sur une fonctionnalité et pas moi, je n'ai pas la maîtrise du sujet donc suis dans l'incapacité de gérer la prod de cette feat 
>
> **Jonathan**: Lorsqu'il y a un soucis, on passe plus de temps à trouver le responsable qu'à résoudre le problème
>
> **Dimitri**: Lorsqu'il y a un soucis et que toute l'équipe ne participe pas à la résolution, certains choix / compromis aurient pu être [meilleur].

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


## For which activities?

We currently pratice mob programming for various types of activities, the most obvious one being development. After all we are devs, right?

### During a mission
Because the coding part in a project is never the starting point, nor the ending one, we also have to consider other tasks to attend to.

Before partnership even begins between a client and us, we need to understand the problem we aim to solve. Having the team available for a first meeting helps a lot to ask the right questions.  
Remember, we need as much information as possible to make sure we have the required skills to come up with the right solution. We might have to onboard newcomers in our collective to fulfill these requirements.

About partnership, it might have to begin with a quote and this is something we tackle collectively. We decide together to share a degree of risk. We succeed as a team or fail as team.

Priorities are always discussed and defined with the customer. We aim for the most value as fast as possible while seeking for active user feedbacks.  
Because the most urgent feature could break into multiple subtasks, priorisation is dealt internally. There is always someone in the mob programming who put on the focus maintener role. 

### Outside of a mission

One of the primary activities outside of missions is the organization and structuring of the collective. This involves regular meetings where team members come together to discuss ongoing projects, share insights, and strategize on future endeavors. By establishing a clear framework for collaboration, the team ensures that everyone is aligned and that their collective efforts are directed towards common goals.

A fundamental principle of our collective decision-making process is that no single individual speaks for the group. Instead, decisions are made collectively, requiring the presence of at least three members to ensure diverse perspectives are considered. This approach not only empowers each team member but also prevents stagnation; we do not wait for absent individuals to weigh in, as this could halt our progress

In addition to decision-making, we take the time to enhance our professional profiles on platforms like LinkedIn and Malt. By collaboratively refining our online presence, we can better showcase our skills and experiences, ultimately benefiting both individual team members and the collective as a whole.
Organisation / structuration du collectif. Guess what, this article is no exception.

Scheduling events is another critical activity that we undertake outside of missions. Whether it’s organizing workshops, meetups, or team-building activities, we prioritize creating opportunities for connection and learning. These events not only strengthen our team dynamics but also allow us to engage with the wider community, sharing our passion for mob programming and learning from others in the field.

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

## How pair/mob programming helps YOU ? 

// Use Airtable answers


## How to start

Vous pouvez aussi trouver des meetup qui organisent des coding dojo. Il y en a dans chaque grande ville. Lors de ces coding dojo, il est courant de le faire en mob programming.

Enfin, le meilleur endroit, c'est au sein de votre équipe. Vous pouvez commencer dès maintenant et si la mise en place est trop compliquée, il y a plusieurs coach techniques qui pourraient vous accompagner.

Pas encore chaud de faire ça dans votre équipe ? Venez sur le collectif (lien discord ou pas ?) et on se fait une session ensemble.

## Aller plus loin
Nous rejoindre sur le discord : https://discord.gg/Z7GeFzpZBT
https://github.com/willemlarsen/mobprogrammingrpg/blob/master/rpg_roles_plain_text.md
