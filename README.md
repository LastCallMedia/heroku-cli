## Provides the [Heroku CLI](https://devcenter.heroku.com/categories/command-line) environment as a Lando app
Heroku CLI is brought to you by your friends at [Last Call Media](https://www.lastcallmedia.com).

### Getting started

* Install [Lando](https://lando.dev/) if you don't already have it: https://lando.dev/download/
* Clone the repository
* Run `lando start`

### Logging in to Heroku

* For browser-based login, use command: `lando heroku login` and open the URL given in your browser.
* For intereactive login, use command: `lando heroku:login` or `lando heroku login -i`.
    * Enter the API key as the login password.
    * Get your API key at [https://dashboard.heroku.com/account](https://dashboard.heroku.com/account)

### Running Heroku CLI commands

Method #1: just prefix the command with `lando`.
Examples:
* `lando heroku help`
* `lando heroku apps`

Method #2: drop into a shell and from there run the Heroku CLI commands directly.

Run `lando ssh`  
then:
  `heroku help` or `heroku apps`, etc.

### Choosing a different Node.js version.

In the `.lando.yml` file, you can change `node:18` to some other version number.

Better: override the setting using a `.lando.local.yml` file as described [here](https://docs.lando.dev/core/v3/#override-file).

    services:
      appserver:
        # --- override node service version ---
        type: 'node:20'

In either case, run `lando rebuild` to effect the change.
