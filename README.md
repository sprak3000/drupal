Drupal Installer
================
This is a simple Composer package that will install Drupal at the root of your Composer project.

Drupal is not directly contained in this project. It is downloaded from the drupal.org website.

**NOTE:** This project was forked from [thecodingmachine/drupal](https://github.com/thecodingmachine/drupal); my need was to have Drupal extracted into a particular directory in the project root.


Installing Drupal using this Composer package:
----------------------------------------------
Not used to Composer? The first step is installing Composer. 
This is essentially a one line process:

```bash
curl -s https://getcomposer.org/installer | php
```

Windows users can download the phar file here: [install composer](http://getcomposer.org/download/).
Then create a *composer.json* file at the root of your project:

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/sprak3000/drupal"
        }
    ],
    "require": {
        "sprak3000/drupal": "7.28.x-dev"
    }
}
```

and finally, run

```bash
php composer.phar install
```

This will download and unpack the Drupal archive in a `public` folder at the root of your project. In this example, the version downloaded is 7.28.

Further Reading:
----------------
Want to learn more about this package? Check out [the original blog post](http://blog.thecodingmachine.com/content/installing-drupal-using-composer).
