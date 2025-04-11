+++
date = '2025-04-06T08:07:52+02:00'
draft = false
title = 'Feedback rules (the world) - Partie 2 - TDD versus Feedback Rules'
+++

# Introduction

Dans [l'article précédent](../feedback_rules_the_world_part_1), nous avons découvert le schéma suivant : 

![Théorie du feedback - action constater déséquilibre qui donne état déséquilibré puis action équilibrer qui donne état équilibré ](feedback-rules.svg)

# Le cycle ok -> RED -> ko -> GREEN

L'étape RED correspond à l'action de mettre en évidence qu'il y a un déséquilibre.

L'étape GREEN est l'action de rééquilibrer.

ok et ko représentent l'état du système. Respectivement quand tout est OK et quand quelque chose ne va pas.

ok -> RED -> ko -> GREEN est le cycle lié à Feedback Rules.

# Test Driven Development

Ce cycle RED - GREEN ressemble énormément au cyle RED - GREEN - REFACTORING

Faisons un petit passage dans le monde du Test Driven Development (TDD). C'est cette méthode qui m'a inspiré cette série d'articles. 

TDD repose sur un cycle que l'on appelle Red - Green - Refactoring, le voici : 
![TDD - cycle red green refactoring](tdd-red-green-refactoring.svg)

- Red : on met en place un test qui échoue
- Green : on fait passer le test
- Refactoring : on arrange le code

Reprenons maintenant ce schéma en se basant sur le concept **Feedback Rules** et découvrons ce que cela donne : 

![TDD - Cycle Red Green Refactoring selon feedback rules](tdd-frtw.svg).

Contrairement au schéma traditionnel de TDD, le feedback est mis en avant dans les cadres et les activités sont des flèches. 

En décrivant TDD à l'aide Feedback rules (the world), nous constatons plusieurs choses : 
- TDD est un process composé de 2 process (Implémentation et refactoring) qui s'exécutent séquentiellement
- Il y a plusieurs sources de feedback : 
	- Les tests automatiques qui échouent ou passent
	- Le constat que le code me convient ou ne me convient pas

Cela met en évidence qu'il y a des choses qui sont faîtes inconsciemment. **Feedback Rules (the world)** est un outil qui permet de les mettre en évidence.


# Double loop TDD

Enrichissons notre vision avec un autre process : la double loop TDD.

Voici le schéma traditionnel : 

![TDD - Cycle Red Green Refactoring selon feedback rules](double-loop-tdd-traditionnelle.svg).

La double loop permet de travailler avec un test d'acceptation qui nous indique quand on a fini le travail. 

Utilisons **Feedback Rules (the world)** pour la schématiser : 

![TDD - Cycle Red Green Refactoring selon feedback rules](double-loop-tdd-frtw.svg).

Nous voyons ici que le cycle TDD est imbriqué dans le cycle Double loop TDD.

# Les conclusions

Cette étude nous a permis de mettre en évidence plusieurs choses : 

- Nous utilisons inconsciemment certains process
- Les process peuvent être : 
	- imbriqués
	- séquentiels
- Il existe plus d'une source de feedback, dont certaines inconscientes

Nous verrons tout cela en détail dans [l'article suivant](../feedback_rules_the_world_part_3).



