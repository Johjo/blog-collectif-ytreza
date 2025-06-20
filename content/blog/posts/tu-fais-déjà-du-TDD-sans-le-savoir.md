+++
date = '2025-06-20T06:28:49+01:00'
draft = false
title = 'Tu fais (déjà) du TDD sans le savoir'
author = ["Jonathan LAURENT"]
+++

# Tu fais (déjà) du TDD sans le savoir

## ✍️ Introduction

Tu penses que le TDD, c’est une histoire de puristes ?  
Que c’est un truc rigide où il faut absolument écrire un test avant chaque ligne de code ?  
Tu n’es pas seul·e.

Mais laisse-moi te poser une question :  
Quand tu codes un bout de logique, que tu l’exécutes pour voir ce que ça donne, puis que tu ajustes… tu fais quoi, exactement ?  
Tu observes, tu testes, tu corriges. Tu fais un cycle.  
Un cycle guidé par le feedback.

Et ce cycle-là, c’est le cœur même du TDD.

Alors non, tu ne respectes peut-être pas les dogmes. Tu ne rédiges peut-être pas un test JUnit avec un nom de méthode en snake_case.  
Mais tu as probablement déjà intégré — sans le formaliser — **le vrai moteur du Test-Driven Development** :  
> un processus itératif, guidé par des résultats concrets, qui t’aide à aller droit au but.

Dans cet article, on va regarder d’un peu plus près ce que tu fais déjà — sans l’étiqueter — et pourquoi ça mérite d’être reconnu… et peut-être renforcé.

---

## 🧠 Le cœur du TDD, ce n’est pas le test, c’est le feedback

Quand on entend “TDD”, on pense tout de suite à des tests. Unitaires. Écrits avant le code. Automatisés.  
Mais ça, c’est la surface. L’outil.

Ce qui donne vie au TDD, ce n’est pas le test en lui-même, c’est **le cycle de feedback** qu’il permet.

TDD, c’est avant tout une manière d’**avancer pas à pas**, en s’appuyant sur une boucle :

1. **Red** : je définis une intention. J’exprime ce que j’attends du système. Et ça échoue (normal, le comportement n’existe pas encore).  
2. **Green** : j’écris juste assez de code pour satisfaire cette intention.  
3. **Refactor** : je nettoie, je clarifie, je structure, sans changer le comportement.

Ce cycle est court, simple, puissant.  
Il met en place un rythme naturel : **je fais une hypothèse, je la vérifie, j’ajuste**.

Et ce rythme-là, tu le pratiques probablement déjà, même si tu n’écris pas de tests automatisés.

Dès que tu fais une modif, que tu relances ton code, que tu regardes si le résultat colle à ce que tu voulais, tu fais exactement ça :  
> un cycle de feedback rapide.

Le test, dans ce cadre, n’est qu’un **outil pour rendre ce feedback tangible, reproductible et vérifiable**.

---

## 🔍 Des exemples de TDD… sans tests

Tu ne l’as peut-être jamais appelé “TDD”.  
Mais si tu as déjà fait ça, alors tu en pratiques les principes :

### 👩‍💻 Exemple 1 : Le REPL / console.log-style

Tu écris une fonction dans un fichier.  
Tu l’appelles avec quelques valeurs dans la console.  
Tu observes ce que ça donne.  
Tu ajustes le code.  
Tu recommences.

➡️ Tu as une **intention** (le comportement attendu)  
➡️ un **feedback immédiat** (ce que la console affiche)  
➡️ une **réaction rapide** (tu modifies et retestes)  

C’est *exactement* le cycle Red – Green – Refactor.  
Juste... en version manuelle.

---

### 🎨 Exemple 2 : Travailler sur une interface graphique

Tu ajustes une marge, un comportement de hover, ou l’apparition d’un modal.  
Tu enregistres. Tu regardes le résultat dans le navigateur.  
Tu changes à nouveau. Tu compares. Tu nettoies le code.

Encore une fois : tu observes un écart entre ce que tu veux et ce que tu as.  
Tu ajustes. Tu raffines.  
C’est une forme de **test guidé par l’expérience utilisateur**, sans script automatisé — mais avec **le même cycle d’apprentissage**.

---

### 🔁 Exemple 3 : Tu fais un PoC rapide avant de structurer ton code

Tu veux tester une idée. Tu bricoles une solution. Tu vois si ça fonctionne.  
Puis tu factorises, tu découpes, tu ajoutes des conditions réelles, tu ranges dans des fonctions.

Tu as posé un **test vivant** : est-ce que cette idée vaut la peine d’être industrialisée ?  
Et quand c’est validé, tu passes à la **refacto**.

---

### 🧩 Ce qu’ils ont en commun

Tous ces cas ont un point commun fondamental :  
> ils sont **guidés par le feedback**.

Pas de plan détaillé sur 200 lignes. Pas de “je code tout et on verra après”.  
Juste une avancée progressive, rythmée par la réalité du système.

Et c’est exactement ça que TDD cherche à systématiser.

---

## 🧭 Pourquoi c’est du TDD dans l’esprit

Si tu reconnais les exemples précédents, alors tu pratiques déjà une chose essentielle :  
> **tu n’écris pas du code dans le vide.**  
> Tu avances guidé·e par le comportement attendu.

Ce qui fait la différence entre un code jeté au hasard et une démarche intentionnelle, c’est cette boucle :

- 🎯 **Une intention claire** : tu sais ce que tu veux obtenir  
- 🧪 **Une vérification rapide** : tu regardes si ça fonctionne  
- 🛠️ **Un ajustement ciblé** : tu modifies ce qu’il faut, ni plus ni moins  
- 🔁 **Une itération** : tu recommences jusqu’à avoir quelque chose de satisfaisant

Ce n’est peut-être pas du “TDD académique” — avec un test unitaire, un framework, une CI verte —  
Mais c’est **TDD dans l’intention**.

> Le test n’est qu’un **moyen** d’instaurer un feedback clair, rapide et stable.

Tu pourrais le remplacer par une trace console, un rendu graphique, ou même un collègue qui te dit “non, ça ne marche pas”.  
Le point commun, c’est que tu **valide un comportement** avant d'aller plus loin.

Et quand tu prends le réflexe d’**attendre une preuve avant de continuer**, tu es déjà dans une posture TDD.

---

## 🚀 Ce que le TDD apporte en plus

Si tu suis déjà un cycle d’itération guidé par le feedback, tu es sur la bonne voie.  
Mais pourquoi formaliser tout ça avec de “vrais” tests automatisés ?  
Qu’est-ce que TDD apporte de plus, au-delà de l’intuition ?

### ✅ 1. Le feedback devient **automatisé et reproductible**

Plus besoin d’y penser : le test tourne à chaque fois.  
Un test cassé ne te laisse pas oublier une régression.

### 👥 2. Le feedback devient **partageable**

Les tests montrent ton intention à la personne qui lit ton code demain.  
C’est un support de communication technique.

### 🧱 3. Le feedback devient **structurel**

Tu découpes ton code pour qu’il soit testable.  
Et donc souvent plus clair, plus simple, mieux organisé.

### 🧘 4. Le feedback devient **apaisant**

Tu avances avec moins de peur, plus de confiance.  
Tu peux refactorer sereinement.

> TDD, c’est un filet de sécurité qui te permet d’avancer librement.

---

## ✅ Conclusion — Tu fais du TDD… il ne te manque que le nom

Tu n’as peut-être jamais lancé `npm test` ou écrit une méthode `test_should_return_true_when_input_is_valid`.  
Mais si tu avances par petits pas, en observant le comportement du code, en ajustant, en réessayant...  
Alors tu fais déjà ce qui compte :  
> **tu codes guidé·e par le feedback.**

Et ce feedback, c’est le cœur du TDD.  
Le reste, c’est de l’outillage, du confort, des bonnes pratiques — utiles, mais secondaires.

Ce que tu fais **instinctivement**, TDD t’invite à le **rendre visible, reproductible et partageable**.

---

### 🌱 Et maintenant ?

Tu n’as pas besoin de tout changer d’un coup.  
Mais la prochaine fois que tu fais un `console.log`, ou que tu testes une idée vite fait...  
Demande-toi :  
> “Et si j’écrivais un test pour ça ?”

Petit à petit, tu verras que **formaliser ton feedback** t’aide à mieux réfléchir, mieux structurer… et avancer plus sereinement.

Tu fais (déjà) du TDD.  
Il ne te reste qu’à l’assumer. 😌
