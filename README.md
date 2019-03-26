<p align="center"><img src="https://image.flaticon.com/icons/svg/977/977504.svg" width="150"><p>
<h1 align="center">Awesome Laravel Bash Aliases</h1>


<p align="center">
<a href="https://github.com/sindresorhus/awesome">
    <img align="center" src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg">
</a>

<a href="https://travis-ci.org/ahinkle/awesome-laravel-bash-aliases">
    <img align="center" src="https://img.shields.io/travis/ahinkle/awesome-laravel-bash-aliases/master.svg?style=flat">
</a>

🚀 Curated list of useful Laravel bash aliases that will make your work easier.

## Inspiration

Working with bash in daily life, it is very irritating writing the same command multiple times.
To avoid that we write aliases/snippets for bashrc and make our life easier.

.. and let's get real - Watching Taylor Otwell and Jeffrey Way run "`nah`" is magical ✨.

Read [Contribution Guidelines](CONTRIBUTING.md) before contributing.

## Contents

- [Contents](#contents)
    - [How To Use Aliases](#how-to-use-aliases)
    - [Laravel Framework](#laravel-framework)
        - [Artisan Console](#artisan-console)
        - [Controllers](#controllers)
        - [Database](#database)
        - [Installation](#installation)
        - [Logging](#logging)
        - [Testing](#testing)
    - [Composer](#composer)
    - [Docker](#docker)
    - [Git](#git)
    - [Other](#other)
- [License](#license)

<a id="how-to-use-aliases"></a>
### How To Use Aliases
First, open up the `~/.bashrc` file in a text editor that is found in your home directory. Uncomment or add the following lines:

    if [ -f ~/.bash_aliases ]; then
        . ~/.bash_aliases
    fi

This tells it to load a .bash_aliases file, if it exists, so you can put all your aliases in it and make them easier to share and keep up with. Finally, create the `~/.bash_aliases` file and add the following as your first alias:

    alias art="php artisan"

Save the file and type the following in the terminal:

    source ~/.bashrc

From here on you should be able to type art and it’ll auto expand into php artisan. Just remember that every time you modify the `bash_aliases` file you’ll need to either run that source command or restart Terminal so the changes are picked up.


<a id="laravel-framework"></a>
### Laravel Framework

<a id="artisan-console"></a>
#### Artisan Console
##### [php artisan](https://laravel.com/docs/artisan)
    alias art="php artisan"

    # also commonly alased to `artisan`, `p`, `pa`, and others.

##### [php artisan tinker](https://laravel.com/docs/artisan#tinker)
    alias t="php artisan tinker"

    # also commonly alased to `pat`, `tink`, `artt`, and others.

<a id="controllers"></a>
#### Controllers
##### [php artisan make:controller](https://laravel.com/docs/controllers)
    alias mc="php artisan make:controller"
    alias mrc="php artisan make:controller --resource "

<a id="database"></a>
#### Database
##### [php artisan make:migration](https://laravel.com/docs/migrations#generating-migrations)
    alias mm="php artisan make:migration"
    alias mmm="php artisan make:migration -m "

##### [php artisan migrate](https://laravel.com/docs/migrations#running-migrations)
    alias migrate="php artisan migrate"
    alias mfs="php artisan migrate:fresh --seed"

<a id="installation"></a>
#### Installation
##### [composer create-project --prefer-dist laravel/laravel](https://laravel.com/docs/5.8/installation)
    alias laravel-installer="composer create-project --prefer-dist laravel/laravel "

##### [php artisan key:generate](https://laravel.com/docs/5.8/installation)
    alias key="php artisan key:generate"

##### [php artisan serve](https://laravel.com/docs/5.8/installation)
    alias serve="php artisan serve"

<a id="logging"></a>
#### Logging
#### [View Log](https://laravel.com/docs/5.8/logging)
    # Tail all Laravel Logs and filter out the stack traces:
    alias viewlog='tail -f -n 450 storage/logs/laravel*.log \
                    | grep -i -E \
                        "^\[\d{4}\-\d{2}\-\d{2} \d{2}:\d{2}:\d{2}\]|Next [\w\W]+?\:" \
                        --color'

#### [Remove Logs](https://laravel.com/docs/5.8/logging)
    alias rmlogs="rm storage/logs/laravel-*.log"

<a id="testing"></a>
#### Testing
##### [phpunit](https://laravel.com/docs/testing#creating-and-running-tests)
    alias t="phpunit"
    alias pf="phpunit --filter "
    alias pg="phpunit --group "

##### [php artisan dusk](https://laravel.com/docs/testing#creating-and-running-tests)
    alias du="php artisan dusk"

##### [php artisan make:test](https://laravel.com/docs/testing#creating-and-running-tests)
    alias mt="php artisan make:test"
    alias mtu="php artisan make:test --unit "

<a id="composer"></a>
### Composer
    alias cdo="composer dump-autoload -o"
    alias ci="composer install"
    alias co="composer outdated"
    alias cu="composer update"

<a id="docker"></a>
### Docker
    alias d='docker'
    alias dc='docker-compose'
    alias dm='docker-machine'

<a id="git"></a>
### Git
    alias g="git"
    alias gl="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
    alias gs="git status"
    alias nah="git reset --hard;git clean -df"
    alias wip="git add . && git commit -m 'wip'"

<a id="other"></a>
### Other
    alias _='sudo'
    alias copyssh="pbcopy < $HOME/.ssh/id_rsa.pub"

---
<a id="license"></a>
## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)