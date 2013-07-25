# PHP Composer Deploy

If you want to use Capistrano to deploy php apps using Composer, this is it.

## Installation

    # gem install php-composer-deploy

## Usage

Open your application's `Capfile` and make it begins like this:

    require 'rubygems'
    require 'php-composer-deploy'
    load    'config/deploy'

Remove `require 'deploy'` since we are overriding that

Full list of tasks:

    $ cap -T

## What do you get?

If you want to try before you buy, here's the list of tasks included with this version of the deploy recipe:

    cap deploy                # Deploys your project.
    cap deploy:check          # Test deployment dependencies.
    cap deploy:cleanup        # Clean up old releases.
    cap deploy:cold           # Deploys and starts a `cold' application.
    cap deploy:pending        # Displays the commits since your last deploy.
    cap deploy:pending:diff   # Displays the `diff' since your last deploy.
    cap deploy:rollback       # Rolls back to a previous version and restarts.
    cap deploy:rollback:code  # Rolls back to the previously deployed version.
    cap deploy:setup          # Prepares one or more servers for deployment.
    cap deploy:create_symlink # Updates the symlink to the most recently deployed ...
    cap deploy:update         # Copies your project and updates the symlink.
    cap deploy:update_code    # Copies your project to the remote servers.
    cap deploy:upload         # Copy files to the currently deployed version.
    cap composer:install      # Run composer install in the currently symlinked directory
    cap composer:copy_vendors # Copy the vendors folder from the previously deployed version
    cap invoke                # Invoke a single command on the remote servers.
    cap shell                 # Begin an interactive Capistrano session.


## Want to help improve this?

Fork me on GitHub:

    http://github.com/lombardoja/php-composer-deploy
