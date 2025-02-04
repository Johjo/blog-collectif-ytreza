+++
date = '2025-02-10T00:00:00+01:00'
draft = false
title = 'Recrutez des developpeurs, pas des techniciens'
author = ["Benjamin Sureau"]
+++

**TLDR**: dans le monde du recrutement tech, les entreprises recherchent des experts d’un outil ou framework spécifique (Symfony, Nest, React, Angular...), au lieu de rechercher des développeurs capables de résoudre des problèmes métier. Cet article explore pourquoi cette approche purement technique est limitée et comment des principes issus du TDD (Test-Driven Development) et de la clean architecture permettent de concevoir des applications solides, en se concentrant sur ce qui génère réellement de la valeur ajoutée pour une entreprise : son coeur de métier.

## Comprendre le vrai rôle d’un développeur

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/p4khtwp6vxn3s4dyt53w.png)

C'est le genre d'annonce qui est malheureusement devenu monnaie courante dans un monde de la tech en pleine crise. Elle reflète une fâcheuse tendance à privilégier des compétences techniques spécifiques, souvent au détriment d’une véritable compréhension des besoins métiers ou d’une évaluation des capacités générales d'un développeur à résoudre des problèmes, s’adapter et collaborer efficacement avec des équipes pluridisciplinaires.

Cette focalisation excessive sur le nombre d'années d'expérience passées sur des frameworks ou des outils en particulier pose un réel problème car elle peut fortement limiter l’accès à des (jeunes) talents capables d’apporter une perspective plus large et innovante, et exclut potentiellement des profils tout aussi compétents, mais moins spécialisés sur des outils précis.

#### Le développeur comme résolveur de problèmes

Le rôle principal d’un développeur n’est pas de maîtriser un framework en particulier, mais de comprendre et résoudre des problèmes métier. Les frameworks et technologies sont des outils, mais leur importance devient secondaire lorsque les principes fondamentaux de la conception logicielle sont respectés. Un bon développeur est un résolveur de problèmes, pas seulement un exécutant de tâches techniques.

#### Technicien vs Développeur

Dans de nombreux cas, les entreprises ne recherchent pas des développeurs mais des techniciens, c’est-à-dire des personnes hautement spécialisées dans un outil donné. Cependant, un technicien excelle dans un cadre restreint mais devient obsolète dès que ce cadre change (nouveau framework, nouvelles technologies).
À contrario, un développeur qui maîtrise les concepts abstraits et les bonnes pratiques de développement s’adapte à tout contexte et peut résoudre des problèmes complexes en gardant le métier au centre de ses préoccupations.

## Le piège des frameworks

Beaucoup confondent encore à tort l’outil avec la valeur qu’il doit réellement servir.
Les frameworks sont sans aucun doute des instruments puissants pour accélérer le développement d'un produit, mais ils ne devraient jamais dicter l’architecture ou limiter la capacité d’une équipe à répondre aux besoins spécifiques de l’entreprise.

#### Les frameworks évoluent rapidement

Les technologies évoluent à un rythme effréné. Le framework populaire d’aujourd’hui pourrait devenir obsolète demain. En focalisant vos recrutements sur des spécialistes d'un framework spécifique, vous risquez de limiter vos perspectives si votre projet change d’orientation ou nécessite des évolutions importantes, voire une migration.

#### Une architecture bien pensée transcende les technologies

Les frameworks ne devraient rester que des détails d’implémentation. Une application robuste et maintenable repose tout d'abord sur une architecture claire et des concepts universels tels que :
• La séparation des préoccupations : Les règles métier et l’infrastructure doivent être isolées les unes des autres.
• La flexibilité : Une application bien conçue peut facilement changer de framework ou encore de source de données sans impacter son cœur logique.

## Les principes pour une approche centrée sur le métier

Une approche centrée sur le métier repose sur des principes d'architectures qui favorisent la clarté, la maintenabilité et l’indépendance par rapport aux outils techniques. Elle permet de développer des solutions alignées sur les besoins réels tout en restant adaptables face aux évolutions technologiques.

Des principes comme le TDD, l'architecture hexagonale... permettent justement de de bâtir des systèmes pérennes, où la technique sert le métier et non l’inverse.

#### TDD : Test-Driven Development

Le TDD consiste à conduire la résolution d'un problème par des tests qui vont servir de tremplin. Chaque nouveau test va permettre de franchir une nouvelle étape vers la résolution du problème, en se concentrant sur les comportements attendus plutôt que les détails d'implémentation. Les tests garantissent que le système fonctionne comme prévu, même après des évolutions importantes, rendant le travail de refactoring beaucoup plus agréable et sans risque de régression.

#### L'architecture hexagonale

Introduite par Alistair Cockburn et popularisée par Robert C. Martin (dit l'oncle Bob), elle repose sur une organisation du code en couches :
• Le core domain : qui contient les règles métier, ordonne les cas d'utilisation... et toute la valeur ajoutée d'un produit. Il est exposé par des ports/interfaces et reste complètement hermétique aux détails d'implémentation.
• L'infrastructure : qui gère les interactions avec le monde extérieur (frameworks, bases de données, etc.), en se connectant aux ports exposés par le domaine via des adaptateurs.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rc0tt1hiudy4b8ccx7s0.png)

## Un exemple concret : l'enregistrement d'un utilisateur

Imaginez une API qui permet d'enregistrer un nouvel utilisateur, avec les règles suivantes :

1. L'adresse email doit être valide et ne doit pas déjà être enregistrée
2. Le mot de passe doit contenir au moins 8 caractères, dont au moins une lettre minuscule, une lettre majuscule et un chiffre.

Commençons par écrire un premier test qui vérifie que, dans un cas nominal (email valide, non déjà enregistré, mot de passe conforme), le cas d’utilisation d’enregistrement d’utilisateur renvoie une réponse attendue :

```javascript
it('Given valid inputs, when user registers, then account is created successfully', () => {
  const registerUser = new RegisterUserUseCase();
  expect(registerUser.execute('melanie@zetofrais.fr', '@ValidP4ssw0rd')).toBe(
    'ok'
  );
});
```

Pour faire passer le test le plus rapidement possible, nous développerons une version minimale du use case qui fait le strict nécessaire. Soit ici, créer une classe `RegisterUserUseCase` avec une méthode `execute(email: string, password: string)` qui renvoie (pour l'instant) `ok` :

```javascript
export class RegisterUserUseCase {
  execute(email: string, password: string): string {
    return 'ok';
  }
}
```

Prenons ensuite le cas où l'email passé en paramètre est invalide :

```javascript
it('Given invalid email, when user registers, then account is not created', () => {
  const registerUser = new RegisterUserUseCase();
  expect(() =>
    registerUser.execute('invalid_email.com', '@ValidP4ssw0rd')
  ).toThrow('Invalid email');
});
```

Le raccourci le plus rapide pour faire passer ce nouveau test sans casser le premier serait alors :

```javascript
export class RegisterUserUseCase {
  execute(email: string, password: string): string {
    if (email === 'invalid_email.com') throw new Error('Invalid email');

    return 'ok';
  }
}
```

Une fois le test vert, on peut ensuite refactoriser la condition pour avoir une solution plus générique :

```javascript
import { z } from 'zod';

const emailSchema = z.string().email();

export class RegisterUserUseCase {
  execute(email: string, password: string): string {
    if (!emailSchema.safeParse(email).success) throw new Error('Invalid email');

    return 'ok';
  }
}
```

Vérifions maintenant que l'adresse email n'est pas déjà enregistrée. Auquel cas on s'attend alors naturellement à une erreur :

```javascript
it('Given valid inputs, when email address is already in use, then account is not created', async () => {
  const registerUser = new RegisterUserUseCase();
  await expect(
    registerUser.execute('melanie@zetofrais.com', '@ValidP4ssw0rd')
  ).rejects.toThrow('Email address already in use');
});
```

Encore une fois, le chemin le plus court pour faire passer le test serait :

```javascript
import { z } from 'zod';

const emailSchema = z.string().email();

export class RegisterUserUseCase {
    constructor(public readonly userRepisotory: UserRepository) {}

    async execute(email: string, password: string): Promise<string> {
        if (!emailSchema.safeParse(email).success)
            throw new Error('Invalid email');

        if (email === 'melanie@zetofrais.com')
            throw new Error('Email address already in use');

        return 'ok';
    }
}
```

Essayons maintenant de refactoriser la condition par quelque chose de plus générique.

On pourrait imaginer une interface qui expose un contrat, défini par une méthode en charge de récupérer un utilisateur à partir d'une adresse email, sans se soucier pour l'instant de la source de données à partir de laquelle cet utilisateur sera récupéré. Si la méthode trouve un utilisateur, elle renvoie l'utilisateur, sinon `null` :

```javascript
import { z } from 'zod';

const emailSchema = z.string().email();

interface UserRepository {
    findByEmail(email: string): Promise<string | null>;
}

export class RegisterUserUseCase {
    constructor(public readonly userRepisotory: UserRepository) {}

    async execute(email: string, password: string): Promise<string> {
        if (!emailSchema.safeParse(email).success)
            throw new Error('Invalid email');

        const emailAddressAlreadyInUse =
            await this.userRepisotory.findByEmail(email);

        if (emailAddressAlreadyInUse)
            throw new Error('Email address already in use');

        return 'ok';
    }
}
```

On peut ensuite développer une implémentation de cette interface pour tester le comportement du use case refactorisé :

```javascript
export class FakeUserRepository implements UserRepository {
    public users: string[];

    constructor() {
        this.users = [];
    }

    async findByEmail(email: string): Promise<string | null> {
        return this.users.find(user => user === email) || null;
    }
}
```

Notre test devient alors :

```javascript
describe('RegisterUserUseCase', () => {
  let userRepository: FakeUserRepository;
  let registerUser: RegisterUserUseCase;

  beforeEach(() => {
    userRepository = new FakeUserRepository();
    registerUser = new RegisterUserUseCase(userRepository);
  });
  it('Given valid inputs, when email address is already in use, then account is not created', async () => {
    userRepository.users.push('melanie@zetofrais.com');
    await expect(
      registerUser.execute('melanie@zetofrais.com', '@ValidP4ssw0rd')
    ).rejects.toThrow('Email address already in use');
  });
});
```

Cette démarche permet rapidement de constater plusieurs choses :

- Le TDD permet par tremplins successifs, comme un guide, de se diriger vers la solution finale, en testant non pas des classes de façon unitaire, mais le comportement global de notre use case.
- Une fois les tests posés, on peut refactorer sans prendre le risque de générer des régressions ou de dévier du comportement attendu de notre use case. Le refactoring n'est plus une source de stress pour le développeur et devient même un plaisir. Il fait partie intégrante du TDD.
- Le TDD amène naturellement aux concepts de clean architecture/architecture hexagonale.
- En adoptant ces principes, on peut continuer de développer tout notre use case sans se préoccuper des détails techniques d'implémentation. En restant concentré sur le domaine logique de notre application :

```javascript
import EmailAddressAlreadyInUseError from '@core-logic/auth/exceptions/emailAddressAlreadyInUseError';
import { UserRepository } from '@core-logic/auth/repositories/userRepository';
import { PasswordHasher } from '@core-logic/auth/services/passwordHasher';
import { DateProvider } from '@core-logic/shared/services/dateProvider';
import { ErrorCodes } from '@core-logic/shared/models/errors';
import { Email } from '@core-logic/auth/models/email';
import { Password } from '@core-logic/auth/models/password';
import { InvalidDataException } from '@core-logic/auth/exceptions/invalidDataException';
import { Logger } from '@core-logic/shared/services/logger';
import { User } from '@core-logic/auth/models/user';
import { v4 as uuidv4 } from 'uuid';
import { Uuid } from '@core-logic/shared/models/uuid';

export class RegisterUserUseCase {
  constructor(
    private userRepository: UserRepository,
    private passwordHasher: PasswordHasher,
    private dateProvider: DateProvider,
    private logger: Logger
  ) {}

  async execute(registerUserRequest) {
      const { email, password, agreedToTerms, subscribedToNewsletter } =
        registerUserRequest;

      this.logger.info('New register user request...', {
        email: email,
      });

      const userEmail = Email.create(email);
      await this.checkIfEmailAddressIsAlreadyInUse(userEmail);

      await this.registerUser(
        userEmail,
        password,
        agreedToTerms,
        subscribedToNewsletter
      );

      this.logger.info('User registered!');
  }

  private async checkIfEmailAddressIsAlreadyInUse(email: Email) {
    const emailAddressAlreadyInUse = await this.userRepository.hasUser(email);

    if (emailAddressAlreadyInUse) {
      throw new EmailAddressAlreadyInUseError('Email address already in use');
    }
  }

  private async registerUser(
    userEmail: Email,
    password: string,
    agreedToTerms: boolean,
    subscribedToNewsletter: boolean
  ): Promise<User> {
    const userPassword = Password.create(password);
    const passwordHash = this.passwordHasher.hash(userPassword);

    if (!agreedToTerms) {
      throw new InvalidDataException('Terms and conditions must be accepted');
    }

    const user = User.create(
      Uuid.create(uuidv4()),
      userEmail,
      passwordHash,
      this.dateProvider.now(),
      this.dateProvider.now(),
      subscribedToNewsletter
    );
    await this.userRepository.register(user);

    return user;
  }
```

Les implémentations (frameworks, ORM...) ne relèvent finalement que de l'ordre du détail technique. Ils viendront se greffer par la suite à notre coeur logique par le biais d'adapters, offrant une grande flexibilité et modularité du code. Par exemple, on pourrait tout à fait garder notre classe `FakeUserRepository` pour simuler une base de données dans le cadre d'une démo client, sans même avoir à y connecter un ORM !

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rggc5txisyt1g8glk81m.png)

Par ailleurs, on voit également que le framework Nest utilisé ici, pourrait être remplacé par n'importe quel autre framework en un rien de temps. Il n'est plus qu'un sous dossier du projet, et ce sont désormais les implémentations qui dépendent des abstractions, non plus l'inverse.

**Retrouver le repo complet de la démo** 👉 [https://github.com/bsureau/tdd-ddd-cleanarchi-example-api](https://github.com/bsureau/tdd-ddd-cleanarchi-example-api)

## Conclusion

Recruter en misant exclusivement sur des compétences techniques spécifiques est une stratégie risquée dans un environnement technologique en constante évolution. Plutôt que de chercher des experts d’un framework ou outil particulier, privilégiez des développeurs qui maîtrisent les concepts fondamentaux de la programmation, sont capables de résoudre des problèmes métier, et s’adaptent rapidement à de nouveaux contextes.

En adoptant des pratiques comme le TDD et la clean architecture, vous posez les bases d’un système solide, maintenable et évolutif. Ces principes permettent de garder le métier au cœur des préoccupations, tout en offrant une flexibilité technologique qui transcende les outils du moment.

Au final, ce qui compte pour une entreprise, ce n’est pas d’avoir des techniciens enfermés dans des boîtes à outils. Apprendre à utiliser un nouveau framework est une histoire de quelques jours. Mais des développeurs capables de comprendre, modéliser et résoudre les problèmes qui génèrent de la valeur ajoutée. Ce sont eux qui, en s’appuyant sur des méthodologies robustes et bien pensées, feront la différence dans un marché compétitif et en constante mutation.

Alors, lors de vos prochains recrutements, demandez-vous : cherchez-vous un technicien d’aujourd’hui ou un développeur de demain ?

## Lectures recommandées

- [Test Driven Developement: By Example, Kent Beck](https://www.amazon.fr/Test-Driven-Development-Kent-Beck/dp/0321146530)
- [Refactoring, Marin Fowler](https://www.amazon.fr/Refactoring-Improving-Design-Existing-Code/dp/0134757599/ref=pd_bxgy_thbs_d_sccl_1/261-5906817-9239643?pd_rd_w=OwRvm&content-id=amzn1.sym.3dbb4249-7cc8-4963-a362-854c36cc0919&pf_rd_p=3dbb4249-7cc8-4963-a362-854c36cc0919&pf_rd_r=FXJ5DHJYH5A5WRGHTC2Q&pd_rd_wg=3BqMC&pd_rd_r=bda8ed22-0c58-4d4c-a6fc-37f2282ea9c7&pd_rd_i=0134757599&psc=1)
- [Clean Architecture: A Craftsman's Guide to Software Structure and Design, Robert C. Martin](https://www.amazon.com/Clean-Architecture-Craftsmans-Software-Structure/dp/0134494164)
- [Domain-Driven Design Distilled, Vaughn Vernon](https://www.amazon.fr/Domain-Driven-Design-Distilled-Vaughn-Vernon/dp/0134434420/ref=sr_1_1?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1TI28KUZUF6SQ&dib=eyJ2IjoiMSJ9.V38g5Do5w5nrE6OQbkJUMAIMZ5R0jvlcHZNXNSwxAsPGjHj071QN20LucGBJIEps.x1BPKyfHyIw7awxF1u9Wc4MDRj19-zhkY9ZRB4_mDHE&dib_tag=se&keywords=domain+driven+design+distilled&nsdOptOutParam=true&qid=1734969160&sprefix=domain+driven+design+distilled%2Caps%2C97&sr=8-1), ou pour les plus valeureux [Implementing Domain Driven Design, Vaughn Vernon](https://www.amazon.com/Implementing-Domain-Driven-Design-Vaughn-Vernon/dp/0321834577)

## Formations

- Formation Wealcome [_TDD, Clean Architecture et DDD_](https://wealcomecompany.com/formations/) dispensée par Michaël AZERHAD
