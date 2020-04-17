# WordPress Site

Easily create a new Composer-based WordPress site.

## Requirements

- PHP 5.6+
- [Composer](https://getcomposer.org/doc/00-intro.md)

## Installation

Run this command in the terminal:
```
composer create-project wp-forge/wp-site
``` 

Optionally append a directory name to the end of the command to customize the folder name that your project will be installed into.

## Usage

### With Laravel Valet

- Install [Homebrew](https://brew.sh/)
- Install [Laravel Valet](https://laravel.com/docs/7.x/valet#installation)
- Install MySQL using Homebrew: `brew install mysql`
- Start MySQL using Homebrew: `brew services start mysql`
- Set password to be `root` for the root user: `$(brew --prefix mysql)/bin/mysqladmin -u root password root`
- Run `composer create-project wp-forge/wp-site local`
- Run `valet link local` (unless you've already run `valet park` and are in your Valet root directory)
- Run `valet secure local`
- Run `cd local`
- Run `composer run wp db create` - You may need to rename the database in your `.env` file first if you don't want your database to be named `local`.
- Visit `https://local.test` (unless you set a different top level domain) in the browser to finish the WordPress installation.

If you want your site's domain to be something different, just replace all instances of the word `local` above with your desired name.

### With Local

- Install [Local](https://localwp.com/)
- Create a new WordPress site using the UI
- Navigate to the site's `app` directory in the terminal. 
- Run `rm -rf public` to delete the `public` directory.
- Run `composer create-project wp-forge/wp-site public`
- Click the link in Local to visit the site in the browser.

## Configuration

Open up the `.env` file to edit database credentials or other WordPress constants.

## Reminders

Don't forget to:

- Update the project's meta data in the composer.json file.
- Customize the readme.md file for your project.
