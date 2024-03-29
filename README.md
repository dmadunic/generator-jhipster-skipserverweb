# generator-jhipster-skipserverweb
[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]
> JHipster blueprint, Blueprint that allows for a Java web layer to be skiped during code generation.

# Introduction

This is a [JHipster](https://www.jhipster.tech/) blueprint, that is meant to be used in a JHipster application.

This blueprint is intended for applications/projects that would like to take benefit from JHippster generator capabilities in creating Java JPA model, DTO's, JPA Repositories and Service layer, but **do not need** Controllers, Mappers and other components specific for Web applications.

Examples of this kind of applications would be: Spring Shell CLI apps, or Java FX based Desktop applications.

In short once installed this bluprint will skip the generation of all web components.

**What this blueprint does not do at the moment.**

Current version of the bluprint does not change build files: gradle.build or pom.xml. 

You still need to manually remove web dependencies you do not need from these!

# Supported JHipster version
Current version of the JHipster generator this bluprint is adjusted for, is JHipster version 6.10.5.

# Prerequisites

As this is a [JHipster](https://www.jhipster.tech/) blueprint, we expect you have JHipster and its related tools already installed:

- [Installing JHipster](https://www.jhipster.tech/installation/)

# Installation

## With NPM

To install this blueprint:

```bash
npm install -g generator-jhipster-skipserverweb
```

To update this blueprint:

```bash
npm update -g generator-jhipster-skipserverweb
```

## With Yarn

To install this blueprint:

```bash
yarn global add generator-jhipster-skipserverweb
```

To update this blueprint:

```bash
yarn global upgrade generator-jhipster-skipserverweb
```

# Usage

To use this blueprint in your Jhipster project run the command bellow:

```bash
jhipster --blueprint skipserverweb
```

## Running local Blueprint version for development

During development of blueprint, please note the below steps. They are very important.

1. Link your blueprint globally 

Note: If you do not want to link the blueprint(step 3) to each project being created, use NPM instead of Yarn as yeoman doesn't seem to fetch globally linked Yarn modules. On the other hand, this means you have to use NPM in all the below steps as well.

```bash
cd generator-jhipster-skipserverweb
npm link
```

2. Link a development version of JHipster to your blueprint (optional: required only if you want to use a non-released JHipster version, like the master branch or your own custom fork)

You could also use Yarn for this if you prefer

```bash
cd generator-jhipster
npm link

cd skipserverweb
npm link generator-jhipster
```

3. Create a new folder for the app to be generated and link JHipster and your blueprint there

```bash
mkdir my-app && cd my-app

npm link generator-jhipster-skipserverweb
npm link generator-jhipster (Optional: Needed only if you are using a non-released JHipster version)

jhipster -d --blueprint skipserverweb

```

# License

Apache-2.0 © [Domagoj Madunić]()


[npm-image]: https://img.shields.io/npm/v/generator-jhipster-skipserverweb.svg
[npm-url]: https://npmjs.org/package/generator-jhipster-skipserverweb
[travis-image]: https://travis-ci.org/dmadunic/generator-jhipster-skipserverweb.svg?branch=master
[travis-url]: https://travis-ci.org/dmadunic/generator-jhipster-skipserverweb
[daviddm-image]: https://david-dm.org/dmadunic/generator-jhipster-skipserverweb.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/dmadunic/generator-jhipster-skipserverweb
