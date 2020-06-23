---
title: Commitizen | Automating release cycles
theme: black
revealOptions:
  transition: "convex"
---

# Commitizen

Automating release cycles

[![github logo](./assets/github.png)](https://github.com/commitizen-tools/commitizen)

---

## About me

Santiago

origin: Argentina 🇦🇷 <!-- .element: class="fragment" data-fragment-index="0" -->

current: Amsterdam 🇳🇱 @ KPN <!-- .element: class="fragment" data-fragment-index="0" -->

🐍 python, web, js, stuff <!-- .element: class="fragment" data-fragment-index="0" -->

---

## Agenda

1. History
2. Commands <!-- .element: class="fragment" data-fragment-index="2" -->
3. Automating release cycle <!-- .element: class="fragment" data-fragment-index="3" -->
4. Customization <!-- .element: class="fragment" data-fragment-index="4" -->

---

## History 📜

Born as a prompt to avoid remembering commit conventions

Based on the js cz-cli

<small>
conventional commits, work conventions, etc <!-- .element: class="fragment" data-fragment-index="1" -->
</small>

---

## In the Beginning

- Extendable: build your own rules
- Automatic version inference planned <!-- .element: class="fragment" data-fragment-index="1" -->
- Wait, I can also generate the changelog 🤔 <!-- .element: class="fragment" data-fragment-index="2" -->

---

## Evolution

Built prompt

Built auto bump version <!-- .element: class="fragment" data-fragment-index="1" -->

@Lee-W starting contributing more and more <!-- .element: class="fragment" data-fragment-index="2" -->

@Lee-W created first autochangelog MVP <!-- .element: class="fragment" data-fragment-index="3" -->

I found motivation again and finished the auto-changelog feature <!-- .element: class="fragment" data-fragment-index="4" -->

---

## Commands

> Aim for intuitiveness and sane defaults

----

`cz init`

Assists in the creation of the `toml` file, with some automatic detections.

----

`cz commit` or `cz c`

🐕‍🦺 Assist in the creation of a commit with matching the defined rules.

Defaults: <!-- .element: class="fragment" data-fragment-index="0" -->
[conventional commitis](https://www.conventionalcommits.org/en/v1.0.0/) <!-- .element: class="fragment" data-fragment-index="0" -->

----

`cz changelog`

Creates changelog file 📂, can target a different file name

----

`cz bump --changelog`

Bumps version ⬆️ including the changelog generation 📂

----

### And more

`cz ls` ➡️ list installed commit rules

`cz check` ➡️ validate the commit (useful for git hooks)

`cz schema` ➡️ show the schema of the commit rule

`cz example` ➡️ show an example

`cz info` ➡️ explain rationale behind the commit rule

---

## Release workflow

🧑 Merge PR

⬇️ <!-- .element: class="fragment" data-fragment-index="0" -->

🤖 Create changelog and new tag <!-- .element: class="fragment" data-fragment-index="0" -->

⬇️ <!-- .element: class="fragment" data-fragment-index="1" -->

🤖 Push back to your branch <!-- .element: class="fragment" data-fragment-index="1" -->

⬇️ <!-- .element: class="fragment" data-fragment-index="2" -->

🤖 Trigger deploy/release for new tag <!-- .element: class="fragment" data-fragment-index="2" -->

---

## Version bump

- Follows SEMVER
- Calculates new tag based on the commit rules and last tag <!-- .element: class="fragment" data-fragment-index="0" -->
- Has the ability to create the changelog <!-- .element: class="fragment" data-fragment-index="1" -->


---

## Fear SEMVER no more

#### MAJOR.MINOR.PATCH 

- Let commitizen handle it for you <!-- .element: class="fragment" data-fragment-index="0" -->
- Contains information <!-- .element: class="fragment" data-fragment-index="1" -->


----

## MAJOR

⬇️ <!-- .element: class="fragment" data-fragment-index="0" -->

BREAKING CHANGES ⚠️ <!-- .element: class="fragment" data-fragment-index="0" -->

----

### MINOR

⬇️ <!-- .element: class="fragment" data-fragment-index="0" -->

New stuff 🎉 <!-- .element: class="fragment" data-fragment-index="0" -->

----

#### PATCH

⬇️ <!-- .element: class="fragment" data-fragment-index="0" -->

Secuuurity 🔒 and bug fixes 🐛 <!-- .element: class="fragment" data-fragment-index="0" -->


---

## Customization

- We have a <!-- .element: class="fragment" data-fragment-index="0" -->
[template for custom rules](https://github.com/commitizen-tools/commitizen_cz_template) <!-- .element: class="fragment" data-fragment-index="0" -->
- Bunch of regex for bump <!-- .element: class="fragment" data-fragment-index="1" -->
- Changelog should work by default, best if a regex is provided <!-- .element: class="fragment" data-fragment-index="2" -->

Read the 
[documentation](https://commitizen-tools.github.io/commitizen/)


---

## Future

- Support for other config format files: `json`
- Github action
- Sprint on next europython

---

## Recap

```bash
# on an initialized git repo
cz init
git add <file>
cz c
cz bump --changelog
```

---

## Demo

---

## Questions 🙋🙋‍♀️

---

![thanks](./assets/thanks.gif)

twitter: [@santiwilly](twitter.com/santiwilly)

github: [woile](github.com/Woile)