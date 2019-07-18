# wmcp-laravel

Vagrant Laravel PHP Development Box

See [Vagrant Laravel Homestead Documentation](https://laravel.com/docs/5.8/homestead) for more information on the Laravel PHP framework.

## Quick Start

Add the following to `/etc/hosts`:

```
192.168.10.10   wmcp-laravel.local
```

Start the vagrant box:

```
vagrant up
```

## Detailed information

This repo is a minimalized version of the Laravel Homestead Vagrant repo with only the `Vagrantfile` and `scripts/` directories copied for initializtaion and NGnix configuration through the `Homestead.yaml` file.

The `homestead-master.zip` file is a .zip download of the Homestead project as of this writing.

To set up the project, unzip `homestead-master.zip`, copy the `Vagrantfile` and `scripts/` directory to the project directory, then use PHP Composer (```brew install composer``` if needed for MacOS) to generate the `Homestead.yaml` sample file:

```
unzip homestead-master.zip
cp homestead-master/Vagrantfile .
cp -iRn homestead-master/scripts .
brew install composer
composer require laravel/homestead --dev
vagrant up
```

Once the build process completes, test the site by navigating to:

```
http://wmcp-laravel.local/phpinfo/
```
