# Scripting for Drupal
Welcome to the scripting repository of Solucionex // SLX, a space for diverse scripting tools for everyday-life. Here, we're storing diverse tooling in order to work with Drupal in the daily life. We have some folders named by functions. Follow our README guide.  

## Installers
In this folder (/installers), you will find some resources in order to launch a new Drupal site / local installation.   
* **installing_complete_environment** Bash script, downloads a Drupal codebase using Docker, Docker-Compose and DDEV. Also installs some JavaScript resources.
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

* **installing_PHP74_basic_setup** Bash script, installs the basic package set for PHP in a Debian / Ubuntu distro.  
  > Features:
    * Install the next packages:   php7.4, php7.4-bcmath, php7.4-bz2, php7.4-curl, php7.4-dev, php7.4-gd, php7.4-dom, php7.4-imap, php7.4-imagick, php7.4-intl, php7.4-json, php7.4-ldap, php7.4-mbstring, php7.4-mysql, php7.4-oauth, php7.4-odbc, php7.4-uploadprogress, php7.4-ssh2, php7.4-xml, php7.4-yaml, php7.4-zip, php7.4-solr, php7.4-apcu, php7.4-opcache, php7.4-redis, php7.4-memcache, php7.4-memcached, php7.4-xdebug, php7.4-sqlite3.      
    
* **installing_docker_dockercompose_ddev** Bash script, installs the Docker Engine and the DDEV tool in a local environment.
  > Features: 
    * Updates your local package system.  
    * Installs some resources as: build-essential apt-transport-https ca-certificates jq curl software-properties-common file git  
    * Installs containerd docker.io docker-compose
    * Enables Docker and add the current user to the Docker group.
    * Checks if Docker is running or not.
    * Gets output from the Docker installed version.
    * Checks if DDEV was installed by brew or not, updating brew and previous versions of DDEV.
    * Downloads and executes the DDEV basic installation script.
    * Checks if DDEV is available now in your system.

* **installing_custom_subtheming** Bash script, creates and enables a new custom Drupal subtheme from Bartik inside your Drupal installation.    
  Works with DDEV, just for a DDEV local deployment, executes the script within the main project folder.  
  > Features:
    * Creates all the new folders structure.
    * Creates a new custom subtheme: info.yml, libraries.yml, .js initial file and CSS initial file.
    * Puts the Drupal installation in dev mode, turning off the cache system and enabling TWIG debug.
    * Installs and enables new subtheme using Drush.
    * Launch the Drupal installation through the default browser.
    
 * **/installers/drupal_versions_using_ddev/** Main folder with a family of installation scripts for deploy local Drupal installations with different versions (Drupal 7, Drupal 8, Drupal 9 and Drupal 9 using Acquia Lightning version). This scripts covers all the steps when you already are in a Debian / Ubuntu System and have Docker, Docker-Compose and DDEV working locally. Use the scripts just in these scenarios.  
 * **installing_drupal9_ddev** This is our main script (right now), is a processing bash script to deploy a whole Drupal 9 site ready to Work. Just download, move to your workspace directory, giving permissions to the file with ```chmod +x installing_drupal9_ddev``` and launching it with a new project name as parameter, just do:  
 
 ```bash
 $ cd workspace
 $ chmod + x installing_drupal9_ddev
 $ ./installing_drupal9_ddev projectname
 ```
 See the actions contained in the script:  
   > Features:
     * Gets initial name for new project and makes folder.
     * Builds initial basic structure for DDEV deploy.
     * Gets the Docker Compose file for Portainer in DDEV network (from https://github.com/davidjguru/ddev-contrib/tree/master/docker-compose-services/portainer). 
     * Inits the DDEV local deploy using ```ddev composer create```.
     * Creates auxiliary folders: /scripts, /docs, /backups, /config/sync.
     * Downloads and prepares JavaScript libraries for Web Profile (d3, highlight).
     * Changes the location of the config/sync folder using a new custom settings.local.php
     * Writes a new README file for project in root.
     * Builds the new Drupal Site and clears cache.
     * Installs some Drupal contrib modules and resources.
     * Creates a new custom subtheme derivative from Bartik (with basic files, CSS and JavaScript) and enables it in the Drupal installation.
     * Puts the Drupal installation in dev mode turning off the cache system and enabling TWIG debug.
     * Exports an initial dump of the database file and the config files.
     * Restarts, launchs in browser and connects the new deploy.
 * **installing_drupal9_acquia_lightning_ddev** Same as former but using Acquia Lightning as base. 
 * **installing_drupal8_ddev** Same as the first script but for a Drupal 8 core version. 
 * **installing_drupal7_ddev** Just a very, very basic script for Drupal 7 installation. 
