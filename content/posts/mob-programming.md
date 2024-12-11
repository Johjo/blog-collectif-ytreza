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

Instead of coming up with a list of all the reasons why we choose mob programming, let's dig into few common situations you might also have encountered in the past.

### 🌈🦄 Unicorns 🦄🌈
> **Jonathan**: Seriously, this is nuts.
>
> **Dimitri**: ?
>
> **Jonathan**: I recently came across a few job offers... Every time, developers are asked to be able to work on the backend, frontend, CI/CD, infrastructure, security, and so on.
>
> **Dimitri**: I get it. They don't want, and might not even have the budget, to hire 5 persons. Depending on the project, infrastructure might just be a thing they need to address at the very beginning but won't see a lot of work afterwards. Same about the CI, which only sees a few optimizations here and there.
>
> **Jonathan**: But how could one normal person truly master all these skills? 🤷‍♂️ I can master a few but only scratch the surface of the other ones. I'm no unicorn 🦄
>
> **Alexandre**: I can easily deal with the frontend 🖼️ but could get some help on the backend ⚙️
>
> **Jonathan**: Exact opposite on my end...
> 
> **Dimitri**: I'm quite familiar with CI/CD and cloud provisioning.
>
> **Alexandre**: We're onto something here 🤔


### "We just need a quick tech review before deployment"
> **Dimitri**: I found my nemesis. The one thing that could end our modern world. Asynchronous blocking code reviews 🤬
>
> **Jonathan**: "Slightly" dramatic but I could relate to that. What happened?
> 
> **Dimitri**: I am working on a feature for which I now need any team member review approval. Until then, I can't deploy anything 🤦
>
> **Jonathan**: So far so good IMHO. Code reviews help in sharing what has been done to the rest of the team.
>
> **Dimitri**: Yup. That's the issue.
>
> **Jonathan**: I don't get it 🤔
>
> **Dimitri**: "What has been done". I already went through the problem multiple times to find, to my knowledge, the best solution and design.
>
> **Jonathan**: Yes but you might have missed something.
>
> **Dimitri**: Of course but I spent hours on that and now I need to undo mostly everything.
>
> **Mickael**: You could have just pair programmed with this person. Just sayin' 🤷‍♂️
>
> **Dimitri**: The thing is I worked on this feature with another team member.
>
> **Mickael**: Why did not you worked with this person then?
>
> **Dimitri**: Same problem. I would have worked with this person but we would still have need review from someone else.
>
> **Mickael**: Why did not you ALSO* worked with this person then?
> 
> **Jonathan**: He has a point.
>
> **Dimitri**: Fair enough. I think I understand where this is going...

### A quick update ⌚
> **Alexandre**: Am I the only one bored AF during daily meetings?
>
> **Mickael**: Careful, slippery terrain ahead 🚧
>
> **Alexandre**. What was once a 5 minute meeting turns out to be 🥁🥁🥁 45. Nearly one hour per day. I didn't even get half of what has been said. Why? Because I only worked on a single topic. Let's even say two.
>
> **Mickael**: I hope everyone in your meeting does not feel the same.
>
> **Alexandre**. Right? It's MENTAL 🤯. Do you have daily meetings in yours?
>
> **Mickael**: Well, we keep it short, mostly because we only talk about previous day feature deployments or bottlenecks. Just a quick update for the product team, one might say.
>
> **Alexandre**: How do you keep your other team members up-to-date with recent design changes?
>
> **Mickael**: We don't. At least not during this meeting. Anything tech-related is often dealt with as soon as it arises.
>
> **Mickael**: Disclaimer: We are two devs and mostly work together synchronously.
>
> **Alexandre**: We are three and is everyone working on something different to speed up progress.
>
> **Mickael**: Let me guess, 9 women = 1 baby in 1 month?
>
> **Alexandre**: Pretty much yeah...

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
