+++
date = '2024-12-23T00:00:00+01:00'
draft = false
title = 'Mob Programming'
author = ["Jonathan LAURENT", "Dimitri KOCH"]
+++

# Disclaimer

This article is currently in progress. We recently asked for your feedback using a simple [Airtable form](https://airtable.com/app87w9xfbVXGGcUT/pagBY6xXvJ4T9h9Sy/form). You can of course share yours while this form is open whether you choose to stick with the Airtable form or to get in touch with us using contact@ytreza.dev 🙏

**We made a [dashboard](https://airtable.com/app87w9xfbVXGGcUT/pagY0gQcUJGXhcTTb) but still have to integrate everyone feedback into this article**.

# Quick reminder

Software development, from the very beginning, has been about working together on a single computer. Remember, early computers were pretty expensive, and you could have fit an entire room with just a single one.
Many engineers were required to operate such a machine at the same time.

We lost this type of collaboration with the beginning of the domestic computer era and our beloved internet 🌐. Nowadays, everyone has their own laptop and could work remotely, which is great; don't get us wrong.

Are we doomed? Yes. End of this article. We hope you like it.

Naaaah, let's get into the meat of this great topic.

# What the heck is Mob Programming anyway?

It's a team activity where everyone is viewing the same screen and only one can use the keyboard, role switching frequently. This activity is fueled by someone's idea jumping onto someone else's brain and so on. That's the general idea, "nothing more, nothing less" some might say.

Nothing less, yes. Nothing more, well... Let's just say there is a lot to it. After all, many books are entirely dedicated to it.
Kind of like how TDD could sometimes be referred to as just baby steps 😅

# Why Mob Programming over anything else?

Instead of coming up with a list of all the reasons why we chose Mob Programming, let's dig into few common situations you might also have encountered in the past.

<details>
<summary><b>🌈🦄 Unicorns 🦄🌈</b></summary>

> **Jonathan**: Seriously, this is nuts.
>
> **Dimitri**: ?
>
> **Jonathan**: I recently came across a few job offers... Every time, developers are asked to be able to work on the backend, frontend, CI/CD, infrastructure, security, and so on.
>
> **Dimitri**: I get it. They don't want, and might not even have the budget, to hire 5 persons. Depending on the project, infrastructure might just be a thing they need to address at the very beginning but won't see a lot of work afterward. Same about the CI, which only sees a few optimizations here and there.
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
</details>

<details>
<summary><b>About the tech review 🔍</b></summary>

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
> **Dimitri**: Of course, but I spent hours on that, and now I need to undo mostly everything.
>
> **Mickael**: You could have just pair programmed with this person. Just sayin' 🤷‍♂️
>
> **Dimitri**: The thing is I worked on this feature with another team member.
>
> **Mickael**: Why didn't you work with this person then?
>
> **Dimitri**: Same problem. I would have worked with this person, but we would still have need review from someone else.
>
> **Mickael**: Why didn't you ALSO* work with this person then?
>
> **Jonathan**: He has a point.
>
> **Dimitri**: Fair enough. I think I understand where this is going...
</details>

<details>
<summary><b>A quick update ⌚</b></summary>

> **Alexandre**: Am I the only one bored AF during daily meetings?
>
> **Mickael**: Careful, slippery terrain ahead 🚧
>
> **Alexandre**. What was once a 5-minute meeting turns out to be 🥁🥁🥁 45. Nearly one hour per day. I didn't even get half of what has been said. Why? Because I only worked on a single topic. Let's even say two.
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
</details>

While there are no unicorns, sadly, these kinds of problems still need to be addressed.
Because software development is also a highly collaborative activity built around adjustments, compromises, mistakes, and successes, collaboration has to be flawless.

Still, don't expect your customers to wait for your collaboration to reach such level. They are waiting for value to be delivered as fast as possible and as regularly as possible. Proper lead time. If the whole team is focused - synchronously working - on the this value, any unclear aspect will be addressed in a matter of minutes, not hours!

We want everyone to:

- Have a deep understanding of the problems we aim to solve
- Learn at the same time, leveraging other members strong expertise
- Be involved during design decisions
- Own the product being built
- Take pride in what we are doing and enjoy teamwork

For all these things to exist, synchronous collaboration is key. Once a group of individuals can be seen as one single entity, flawless collaboration is achieved. What better tool than Mob Programming to shape this team effort?

# For which of our activities?

We currently practice Mob Programming for many tasks, the most obvious one being development. After all we are devs, right?

## During a mission

Because the coding part in a project is never the starting point, nor the ending one, we also have to consider other tasks to attend to.

Before a partnership even begins between a client and us, we need to understand the problem we aim to solve. Having the team available for a first meeting helps a lot to ask the right questions. Remember, we need as much information as possible to make sure we have the required skills to come up with the right solution. We might have to onboard newcomers in our collective to fulfill these requirements.

About partnership, it might have to begin with a quote, and this is something we tackle collectively. We decide together to share a degree of risk. We succeed as a team or fail as a team.

Priorities are always discussed and defined with the customer. We aim for the most value as fast as possible while seeking active user feedback. Because the most urgent feature could break into multiple subtasks, prioritization is dealt internally. There is always someone in the Mob Programming who puts on the focus maintainer role.

## Outside a mission

One of the primary activities outside of missions is the organization and structuring of the collective. This involves regular meetings where team members come together to discuss ongoing projects, share insights, and come up with strategies on future endeavors. By establishing a clear framework for collaboration, the team ensures that everyone is aligned and that their collective efforts are directed towards common goals.

A fundamental principle of our collective decision-making process is that no single individual speaks for the group.
Instead, decisions are made collectively, requiring the presence of at least three members to ensure diverse perspectives are considered. This approach not only empowers each team member but also prevents stagnation; we do not wait for absent individuals to weigh in, as this could halt our progress

In addition to decision-making, we take the time to enhance our professional profiles on platforms like LinkedIn and
Malt. By collaboratively refining our online presence, we can better showcase our skills and experiences, ultimately
benefiting both individual team members and the collective as a whole. Guess what, this article is no exception.

Scheduling events is another critical activity that we undertake outside of missions. Whether it’s organizing workshops, meetups, or team-building activities, we prioritize creating opportunities for connection and learning. These events not only strengthen our team dynamics but also allow us to engage with the wider community, sharing our passion for Mob
Programming and learning from others in the field.

# How do we apply it?

## Tools 🛠️

The general rule: KISS. Keep your tools "simple, stupid". Sounds familiar? It sure is! Here it's applied as a GENERAL
and not a DESIGN principle.

- Conversations:
    - With ou clients: Google Meet or Teams because it's usually easier for them
    - Internally: Discord -> Text, voice and video in a single tool
- Screensharing: Discord. Nice we are reusing a tool ♻️
- Coding:
    - Sharing the codebase: Git obviously
    - Working on the codebase: We tried CodeWithMe but struggled to make this tools fit with how we work.
        - Instead, we are now using mob.sh which is great for frequent role switching. Based on Git so... ♻️
- Taking notes:
    - TODO.md. Yup, it can't be closer to the codebase. Yet another tool (the codebase) reused ♻️
    - Framapad otherwise
- Prioritization:
    - Code related: Final Version Perfected (FVP) approach in our TODO.md. You know the drill -> ♻️
    - Elsewhere: One Discord threads/posts per topic which is closed when no activity is seen after x days

## Methods 📏

A key aspect of Mob Programming is a frequent role switch. We target a controlled state (red or green) before the switch occurs. If a controlled state can't be reached within minutes, we roll back.
When should we switch? It depends on the mood and current team pace 🤷‍♂️. Some great moments for this rotation to happen:

- When mob.sh integrated timer (♻️) tells us to do so. In fact, we decide in advance how long rotation should be ⌛
- When we complete a baby step or a TDD cycle 🚦
- Arbitrarily at a specific moment (e.g., at 2:45 PM) 🕑
- When the driver/navigator ends their line of code/flow of thought. We're not monsters! 👹
- It depends on the mood 🤷‍♂️

When at least 3 persons are participating in a mob session, things get interesting. You can have someone endorse the timekeeper and focus-keeper roles. Another team member can even remind the others to take a break.

There are so many [roles](https://github.com/willemlarsen/mobprogrammingrpg/blob/master/rpg_roles_plain_text.md) one could have.

## Humans 🙆

Did we forget to tell about how much software engineering is a collaborative environment? There is no collaboration without human beings.

Well, for a great Mob Programming experience, trust needs to be built. You can't start your very first rotation all-in with strong challenges, arguments, and all that good stuff. It's crucial to establish a framework so that everyone enjoy a sense of belonging.

Practicing kata is a lovely way to step into it and to learn about how you and your partners react to different situations. As always, it's important to remember that it's the job that's being criticized and not the person.

# Who talks about it?

Is it possible to mention Mob Programming without mentioning [Woody ZUILL](https://www.linkedin.com/in/woodyzuill/)?
Let's give credit where credit is due. He and his team are the originators of Mob Programming.

He, along with [Kevin MEADOWS](https://www.linkedin.com/in/jkmeadows/), pushed this approach even further with ["Software Teaming"](https://softwareteaming.com/). The main idea being to involve the whole team, not just developers, which is truly incredible! 🤯

In France, you can follow:

- [Manon CARBONNEL](https://www.linkedin.com/in/manon-carbonnel/) and [Marjorie AUBERT](https://www.linkedin.com/in/marjorie-aubert-full-stack-developer/) who both share their experience with Mob Programming during talks.
- [Hadrien MENS-PELLEN](https://www.linkedin.com/in/hadrien-mens-pellen-39071231/) -> We are still looking for your "Mob Programming: Is it worth it?" talk replay 😏

## How Mob Programming helps YOU?

**In progress. This is where YOUR feedback will greatly help**

# Where to start?

Probably the best way to start would be with your team as long as you get along quite well. You can try a simple refactoring Kata with 10 minute (max!) rotation. If the experience was pleasing to everywhere, do it again. And again! Practice as a team 💪

If you struggle to implement this activity, you can get in touch with a coach who will be glad to help you out in this wonderful journey.

You're not ready to start with your current team? Let's try it together using our [Discord server](https://discord.gg/A6ZrT3cf)

You can also look for meetups near you which organize meetups with coding dojo. Chances are, when there is a coding dojo, there is Mob Programming not that far.

# We need to go deeper 🕳️

Ok, you are quite used to Mob Programming, right? Try including these [roles](https://github.com/willemlarsen/mobprogrammingrpg/blob/master/rpg_roles_plain_text.md) in your rotations then.
