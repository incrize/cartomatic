![alt text](https://raw.githubusercontent.com/gongled/cartomatic/master/cartomatic.png "Cartomatic Logo")

## About

Cartomatic helps you setup server for CS-Cart or Multi-Vendor 4.0+.

## Quick install

Log in to your server as superuser (root) via SSH and execute this command:

    curl -sL http://cartoma.tk/installer | bash -s -- yourdomain.ltd

If you don't have cURL:

    wget -qO - http://cartoma.tk/installer | bash -s -- yourdomain.ltd

Done. It works.

## Manual install

Log in to your server as superuser (root) via SSH and execute this command:

    curl -sL http://cartoma.tk/preconf | bash

Put custom settings in the JSON file:

    cd /srv/cartomatic/<version>
    vim config/simple.json

You can also specify extra variables in files in 'group_vars' folder.

Run:

    ansible-playbook lamp.yml -c local -e @config/simple.json

Passwords will be saved in the 'credentials' folder.

## Supported platforms

* Ubuntu 14.04 x86_64
* Ubuntu 14.10 x86_64
* Ubuntu 15.04 x86_64
* Debian 6 Squeeze x86_64
* Debian 7 Wheezy x86_64
* Debian 8 Jessie x86_64
* CentOS 6 x86_64
* CentOS 7 x86_64

## Restrictions

* Works well only for clean installations.
* Not compatible with ISPManager, cPanel, Plesk etc.

## Credits

* [@jsjant](https://github.com/jsjant), project's name.
* Andrew Voronin for logo design.
* Tatiana Durnova for the help with translation.

## License

GNU Public Licence 3 (GPL v3)