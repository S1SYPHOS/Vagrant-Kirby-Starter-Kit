# Vagrant/Kirby StarterKit
[![Release](https://img.shields.io/github/release/S1SYPHOS/Vagrant-Kirby-Starter-Kit.svg)](https://github.com/S1SYPHOS/Vagrant-Kirby-Starter-Kit/releases) [![License](https://img.shields.io/github/license/S1SYPHOS/Vagrant-Kirby-Starter-Kit.svg)](https://github.com/S1SYPHOS/Vagrant-Kirby-Starter-Kit/blob/master/LICENSE) [![Issues](https://img.shields.io/github/issues/S1SYPHOS/Vagrant-Kirby-Starter-Kit.svg)](https://github.com/S1SYPHOS/Vagrant-Kirby-Starter-Kit/issues)

**You heard about Kirby CMS and want to use it on your next project? You want to harness the power of Vagrant? Then THIS is for you!**

Here's my personal (thus opinionated) Vagrant+Kirby boilerplate, starring:
- [Kirby CMS v3](https://getkirby.com) - a file‑based CMS that's 'easy to setup, easy to use & flexible as hell'
- [Vagrant](https://www.vagrantup.com) - a tool for building and maintaining portable virtual software development environments

**Table of Contents**
- [1. Requirements](#requirements)
- [2. Getting started](#getting-started)
- [3. Configuration](#configuration)
- [4. Credits](#credits)

## Requirements
- Installing [Vagrant](https://www.vagrantup.com/docs/installation)
- Working [VirtualBox setup](https://www.virtualbox.org/wiki/Downloads) (also works with [other providers](https://www.vagrantup.com/docs/providers))
- [Composer](https://getcomposer.org)

## Getting started
Download or clone this repository, then install the [Gulp/Kirby StarterKit](https://github.com/S1SYPHOS/Gulp-Kirby-Starter-Kit) (or any other Kirby project):

```text
# Composer
composer create-project s1syphos/gulp-kirby-starter-kit htdocs --no-dev --prefer-dist

# Git
git clone https://github.com/S1SYPHOS/Gulp-Kirby-Starter-Kit.git htdocs
```

Now just type `vagrant up` and code away!

## Configuration
This boilerplate assumes that `index.php` is stored inside `htdocs`:

```text
htdocs/
├── assets
├── content
├── kirby
├── site
└── index.php
```

However, for a [more secure setup](https://getkirby.com/docs/guide/configuration#custom-folder-setup) (and some extra straightforwardness), the following structure is recommended:

```text
htdocs/
├── content
├── kirby
├── public
│   ├── assets
│   ├── .htaccess
│   └── index.php
├── site
└── storage
    ├── accounts
    ├── cache
    └── sessions
```

The webserver only exposes the `public` directory, which contains `assets`, `index.php` and `.htaccess`. For this to work, simply move some files around, update your `index.php` (Gulp/Kirby StarterKit [got your back](https://github.com/S1SYPHOS/Gulp-Kirby-Starter-Kit/blob/master/index.php)) and `lib/config/vars.yml` (just comment/uncomment some lines).

## Credits
@dirkaholic's [vagrant-php-dev-box](https://github.com/dirkaholic/vagrant-php-dev-box) inspired this boilerplate - he deserves all the credit.

## Special Thanks
I'd like to thank everybody that's making great software - you people are awesome. Also I'm always thankful for feedback and bug reports :)
