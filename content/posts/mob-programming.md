+++
date = '2024-11-19T09:55:56+01:00'
draft = false
title = 'Mob Programming'
+++

# Genesis

At the very beginning, each developer was behind his own computer in his garage or whatever room they liked to be in. There were very few of them because affording a computer was far from how easy it is today.

Years passed, and companies started to show needs for software development. Developers were hired to work on projects in the same place. Development became a team activity. Hurray!

These developers had to organize their work in a way that would be efficient.

-- share file with hard disk

-- Git appeared, PR (mainly for OSS projects)

-- mob programming appears

Tous ces concepts étaient complexes pour partager le travail d'équipe. Un jour, quelqu'un a eu l'idée de simplifier ce process en faisant travailler les développeurs ensemble, sur le même clavier et le même écran. Le mob programming était né.

Et enfin, avec Internet, le remote mob programming a vu le jour.

But did it really ?

# Why mob programming over anything else ?

Instead of coming up with a list of all the reasons why we chose mob programming, let's dig into few common situations you might also have encountered in the past.

## 🌈🦄 Unicorns 🦄🌈

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

## "We just need a quick tech review before deployment"

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

## A quick update ⌚

> **Alexandre**: Am I the only one bored AF during daily meetings?
>
> **Mickael**: Careful, slippery terrain ahead 🚧
>
> **Alexandre**. What was once a 5 minute meeting turns out to be 🥁🥁🥁 45. Nearly one hour per day. I didn't even get half of what has been said. Why? Because I only worked on a single topic. Let's even say two.
>
> **Mickael**: I hope everyone does not feel the same 😅
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
> **Alexandre**: We are three and everyone is working on something different to speed up progress.
>
> **Mickael**: Let me guess, 9 women = 1 baby in 1 month?
>
> **Alexandre**: Pretty much yeah...

While there is no unicorn, sadly, these kinds of problems still need to be addressed.
Because software development is also a highly collaborative activity built around adjustments, compromises, mistakes, and successes, collaboration has to be flawless.

We want everyone to:
- Have a deep understanding of the problems we aim to solve
- Learn at the same time, leveraging other members strong expertise
- Be involved during design decisions
- Own the product being built
- Take pride in what we are doing and enjoy teamwork

For all these things to exist, synchronous collaboration is key. Once a group of individuals is seen as one single entity, flawless collaboration is achieved. 
What better tool than mob programming to shape this team effort?

# For which activities

We currently pratice mob programming for many tasks, the most obvious one being development. After all we are devs, right?

## During a mission

Because the coding part in a project is never the starting point, nor the ending one, we also have to consider other tasks to attend to.

Before a partnership even begins between a client and us, we need to understand the problem we aim to solve. Having the team available for a first meeting helps a lot to ask the right questions. 
Remember, we need as much information as possible to make sure we have the required skills to come up with the right solution. We might have to onboard newcomers in our collective to fulfill these requirements.

About partnership, it might have to begin with a quote, and this is something we tackle collectively. We decide together to share a degree of risk. We succeed as a team or fail as a team.

Priorities are always discussed and defined with the customer. We aim for the most value as fast as possible while seeking active user feedback. 
Because the most urgent feature could break into multiple subtasks, prioritization is dealt internally. There is always someone in the mob programming who puts on the focus maintainer role. 

## Outside of a mission

One of the primary activities outside of missions is the organization and structuring of the collective. This involves regular meetings where team members come together to discuss ongoing projects, share insights, and strategize on future endeavors. By establishing a clear framework for collaboration, the team ensures that everyone is aligned and that their collective efforts are directed towards common goals.

A fundamental principle of our collective decision-making process is that no single individual speaks for the group. Instead, decisions are made collectively, requiring the presence of at least three members to ensure diverse perspectives are considered. This approach not only empowers each team member but also prevents stagnation; we do not wait for absent individuals to weigh in, as this could halt our progress

In addition to decision-making, we take the time to enhance our professional profiles on platforms like LinkedIn and Malt. By collaboratively refining our online presence, we can better showcase our skills and experiences, ultimately benefiting both individual team members and the collective as a whole.
Organisation / structuration du collectif. Guess what, this article is no exception.

Scheduling events is another critical activity that we undertake outside of missions. Whether it’s organizing workshops, meetups, or team-building activities, we prioritize creating opportunities for connection and learning. These events not only strengthen our team dynamics but also allow us to engage with the wider community, sharing our passion for mob programming and learning from others in the field.

# How

## Tools 🛠️

The general rule: KISS. Keep your tools "simple, stupid". Sounds familiar? It sure is! Here it's applied as a GENERAL but a DESIGN principle.

- Conversations:
  - With out clients: Google Meet or Teams because it's usually easier for them
  - Internally: Discord -> if you need to schedule a meeting switch from a textual conversation to a vocal one, get another tool a try.
- Screensharing: Discord. Nice we are reusing a tool ♻️
- Coding:
  - Sharing the codebase: Git obviously
  - Working on the codebase: We tried LiveShared and CodeWithMe but struggled to make these tools fit with how we work.
    - Instead, we are now using mob.sh which is by far the best tool for frequent role switching and is based on Git. Another tool being reused ♻️
- Taking notes:
  - TODO.md. Yup, it can't be closer to the codebase. We are reusing yet another tool (the codebase) ♻️
  - Framapad otherwise
- Priorization:
  - Code related: Final Version Perfected (FVP) approach in our TODO.md. You know the drill -> ♻️
  - Elsewhere: Discord threads/posts per topic. We are currently playing with closing a topic when no activity is seen after x days

## Methods 📏

A key aspect of mob programming is a frequent role switch. We target a controlled state (red or green) before the switch occurs. If a controlled state can't be reached within minutes, we roll back.
When should we switch? It depends on the mood and current team pace 🤷‍♂️. Some great moments for this rotation to happen:
- When mob.sh integrated timer (♻️) tells us to do so. In fact, we decide in advance how long rotation should be ⌛
- When we complete a baby step or a TDD cycle 🚦
- Arbitrarily at a specific moment (e.g., at 2:45 PM) 🕑
- When the driver ends their line of code and the navigator completes their flow of thought. We're not monsters! 👹
- It depends on the mood 🤷‍♂️

When at least 3 persons are participating in a mob session, things get interesting. You can have someone endorse the timekeeper and focuskeeper roles. Another team member can even remind the others to take a break.

There are so many [roles](https://github.com/willemlarsen/mobprogrammingrpg/blob/master/rpg_roles_plain_text.md) one could have.

## Humans 🙆

Did we forget to tell about how much software engineering is a collaborative environment? There is no collaboration without human beings.

Well, for a great mob programming experience, trust needs to be built. You can't start your very first rotation all-in with strong challenges, arguments, and all that good stuff.

Practicing kata is a lovely way to step into it and to learn about how you and your partners react to different situations. As always, it's important to remember that it's the job that's being criticized and not the person.

# Who talks about it

Is it possible to mention Mob Programming without mentioning [Woody ZUILL](https://www.linkedin.com/in/woodyzuill/)? Let's give credit where credit is due. He and his team are the originators of Mob Programming.

He, along with [Kevin MEADOWS](https://www.linkedin.com/in/jkmeadows/), pushed this approach even further with ["Software Teaming"](https://softwareteaming.com/). The main idea being to involve the whole team, not just developers, which is truly incredible! 🤯

In France, you can follow:
- [Manon CARBONNEL](https://www.linkedin.com/in/manon-carbonnel/) and [Marjorie AUBERT](https://www.linkedin.com/in/marjorie-aubert-full-stack-developer/) who both share their experience with Mob Programming during talks.
- [Hadrien MENS-PELLEN](https://www.linkedin.com/in/hadrien-mens-pellen-39071231/). I'm still looking for his "Mob Programming: Is it worth it?" talk replay 


## How pair/mob programming helps YOU ? 

// Use Airtable answers


# Where to start

Probably the best way to start would be with your team as long as you get along quite well. You can try a simple refactoring Kata with 10 minute (max!) rotation. If the experience was pleasing to everywhere, do it again. And again! Practice as a team 💪
If you struggle to implement this activity, you can get in touch with a coach who will be glad to help you out in this wonderful journey.

You're not ready to start with your current team? Let's try it together using our [Discord server](https://discord.gg/XDNbYaBp)

You can also look for meetups near you which organize meetups with coding dojo. Chances are, when there is a coding dojo, there is Mob Programming not that far.

# Dig deeper

Ok you are quite used to Mob Programming, right? Try including these [roles](https://github.com/willemlarsen/mobprogrammingrpg/blob/master/rpg_roles_plain_text.md) in your rotations.
