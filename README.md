# Must See Movies Auth

In this project, we'll practice using the Devise gem to add authentication and authorization.

## Windows bcrypt error

Note: Windows users, at some point you may run into an error with the bcrypt gem when you try to rails db:seed or sign in with the admin user. In order to resolve,

 1. Shut down your `rails server` if you have one running, and/or
 1. Launch Command Prompt with Ruby on Rails, and navigate to your project  folder.
 1. At the command line, run:

    ```ruby
    gem uninstall bcrypt
    ```

    If you're asked "Continue with Uninstall?", answer "y".

 1. At the command line, run:

    ```ruby
    gem uninstall bcrypt-ruby
    ```

    If you're asked "Continue with Uninstall?", answer "y".

 1. At the command line, run:

    ```ruby
    gem install bcrypt --platform=ruby
    ```

    If you're asked "Continue with Uninstall?", answer "y".

 1. In Atom, add the following to the `/Gemfile`:

    ```ruby
    gem 'bcrypt', platforms: :ruby
    ```

 1. At the command line, run: `bundle install`
 1. (Re)start your `rails server`, and you should be good to go!

## Setup

 1. Fork, clone, and open the code.
 1. `bundle install`
 1. Start the server and navigate to [http://localhost:3000](http://localhost:3000)
 1. Quickly pre-populate some data:

    ```
    rake db:seed:characters
    ```

## Devise Guide

Have the [Devise Guide](https://guides.firstdraft.com/authentication-and-authorization-with-devise.html) open in a tab to refer to as we work together.
