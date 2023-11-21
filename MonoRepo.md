
# What is a monorepo?
~~~
A monorepo is a version-controlled code repository that holds many projects. 
While these projects may be related, they are often logically independent and run by different teams.

Some companies host all their code in a single repository, shared among everyone. Monorepos can reach colossal sizes. 
Google, for example, is theorized to have the largest code repository ever, which has tens of hundreds of commits per day and is over 80 TBs large. 
Other companies known to run large monorepos are Microsoft, Facebook, and Twitter.
~~~
# Monorepos vs. multirepos

~~~
The opposite of the monorepo is multirepo, where each project is held on an entirely separate, 
version-controlled repository. Multirepos come naturally — it’s what most of us do when starting a new project. 
After all, who doesn’t like starting fresh?

Going from multi to monorepo is a matter of moving all your projects into a single repository.
~~~

![43242](https://github.com/Sri-Labs2023/Git-branching-strategy/assets/141903669/a0108df5-4172-4b9c-802c-bf8bb7593c65)


# benefits of monorepos

At first glance, the choice between monorepos and multirepos may not seem like a big deal, but it’s a decision that will deeply influence your company’s development workflow. 
As for their benefits, we can list a few:

**Visibility:**
~~~
everyone can see everyone else’s code.This property leads to better collaboration and cross-team contributions —
a developer in a different team can fix a bug in your code you didn’t even know existed.
~~~

**Simpler dependency management:**

~~~
sharing dependencies is trivial. There’s little need for a package manager as all modules are hosted in the same repository.
~~~
**Single source of truth:**
~~~
one version of every dependency means there are not versioning conflicts and no dependency hell.
~~~

**Consistency:**
~~~
enforcing code quality standards and a unified style is easier when you have all your codebase in one place.
~~~

**Shared timeline:**
~~~
 breaking changes in APIs or shared libraries are exposed immediately,
forcing different teams to communicate ahead and join forces. Everyone is invested in keeping up with changes.
~~~

**Atomic commits:**
~~~
atomic commits make large-scale refactoring easier. A developer can update several packages or projects in a single commit.
~~~

**Implicit CI:**

~~~
 continuous integration is guaranteed as all the code is already unified in one place.
~~~

**Unified CI/CD:**
~~~
 you can use the same CI/CD deployment process for every project in the repo.
~~~

**Unified build process:**
~~~
we can use a shared build process for every application in the repo.
~~~

# Hating monorepos

As monorepos grow, we reach design limits in version control tools, build systems, and continuous integration pipelines. 

These problems can make a company go the multirepo route:

**Bad performance:**
~~~
monorepos are difficult to scale up. Commands like git blame may take unreasonably long times,
IDEs begin to lag and productivity suffers, and testing the whole repo on every commit becomes infeasible.
~~~

**Broken main/master:**
~~~
a broken master affects everyone working in the monorepo.
This can be seen as either disastrous or as a good motivation to keep tests clean and up to date.
~~~
**Learning curve:**
~~~
the learning curve for new developers is steeper if the repository spans many tightly-coupled projects.
~~~
**Large volumes of data:**
~~~
monorepos can reach unwieldy volumes of data and commits per day.
~~~
**Ownership:**
~~~
maintaining ownership of files is more challenging, as systems like Git or Mercurial don’t feature built-in directory permissions.
~~~

**Code reviews:**
~~~
notifications can get very noisy. For instance,
GitHub has limited notifications settings that are not best suited for a snow slide of pull requests and code reviews.
~~~
**Investing in tooling**
https://semaphoreci.com/blog/what-is-monorepo#investing-in-tooling

