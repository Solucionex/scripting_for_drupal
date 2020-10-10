# Scripting for Drupal
Welcome to the scripting repository of Solucionex // SLX, a space for diverse scripting tools for everyday-life.  

## Installers
In this folder you will find some resources in order to launch a new Drupal site / local installation.   
* **Buckaroo:** Bash script, download a Drupal codebase using Docker, Docker-Compose and DDEV. Also installs some JavaScript resources.
  > Features:
    * Checks if an Internet connection is available.  
    * Installs updated packages for [Docker](https://docs.docker.com/get-started/overview/), [Docker-Compose](https://docs.docker.com/compose/). 
    * Installs or updates [DDEV-Local](https://ddev.readthedocs.io/en/stable/).
    * Runs Docker and stop Apache local server, in order to leave the port 80 free.
    * Builds a new Drupal-based project using DDEV-Local.
    * Download a custom docker-composer file in order to add a one more [container with Portainer to the DDEV-Local Network](https://github.com/davidjguru/ddev-contrib/tree/master/docker-compose-services/portainer). 
    * Creates, configures and Deploys a new Drupal site in the current location.
    * Installs and enable some Basic Drupal Modules ready for work: [devel](https://www.drupal.org/project/devel), [masquerade](https://www.drupal.org/project/masquerade), [admin_toolbar](https://www.drupal.org/project/admin_toolbar) and [webprofiler -merged in Devel module-](https://www.drupal.org/project/webprofiler).
    * Builds subtheming for the project: Creates the custom subtheme, libraries declaration, an initial JavaScript file and an initial empty file for CSS styling.
    * Puts the Drupal instalation in dev mode turning off the cache system and enabling TWIG debug.
    * Installs and enable subtheme.
    * Installs node, npm and Angular.
    * Shows a whole report with info about the installation.
    * Launches the new Drupal Site in Browser and connect to the container's prompt.

* **PHP74_basic_setup:** Bash script, installs the basic package set for PHP in a Debian / Ubuntu distro.  
  > Features:
    * Install the next packages:   php7.4, php7.4-bcmath, php7.4-bz2, php7.4-curl, php7.4-dev, php7.4-gd, php7.4-dom, php7.4-imap, php7.4-imagick, php7.4-intl, php7.4-json, php7.4-ldap, php7.4-mbstring, php7.4-mysql, php7.4-oauth, php7.4-odbc, php7.4-uploadprogress, php7.4-ssh2, php7.4-xml, php7.4-yaml, php7.4-zip, php7.4-solr, php7.4-apcu, php7.4-opcache, php7.4-redis, php7.4-memcache, php7.4-memcached, php7.4-xdebug, php7.4-sqlite3.      

* **Installing_Acquia_Lightning_DDEV-Local:** Bash script, installs a Acquia Lightning Drupal Distro using DDEV-Local.
  > Features:
    * Installs the Acquia Lightning Distro for Drupal 9: [drupal.org/lightning](https://www.drupal.org/project/lightning).
    * Installs other Drupal basic resources like: drush, admin_toolbar, drupal_console, devel.  
    * Installs a pair of interesting Drupal contrib modules: [domain for Domain Access](https://www.drupal.org/project/domain) , and [tmgmt for Translation Management Tool](https://www.drupal.org/project/tmgmt).