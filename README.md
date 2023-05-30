## Provides the [Heroku CLI](https://devcenter.heroku.com/categories/command-line) environment as a Lando app

### Getting started

* Clone the repository
* Run `lando start`

### Logging in to Heroku

Use command: `lando heroku -i`

Enter the API key for your Heroku user account as the password, available at [https://dashboard.heroku.com/account](https://dashboard.heroku.com/account)

### Choosing a different Node.js version.

In the `.lando.yml` file, you can change `node:18` to some other version number.

Better: override the setting using a `.lando.local.yml` file as described [here](https://docs.lando.dev/core/v3/#override-file).

    services:
      appserver:
        # --- override node service version ---
        type: 'node:20'

In either case, run `lando rebuild` to effect the change.
