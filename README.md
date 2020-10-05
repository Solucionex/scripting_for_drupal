# Scripting for Drupal
Welcome to the scripting repository of Solucionex // SLX, a space for diverse scripting tools for everyday-life.  

## Installers
In this folder you will find some resources in order to launch a new Drupal site / local installation.   
* **Buckaroo:** Bash script, download a Drupal codebase using Docker, Docker-Compose and DDEV. Also installs some JavaScript resources.
  > Features:
    * Installs updates packages for Docker, Docker-Compose. 
    * Installs or update DDEV.
    * Runs Docker.
    * Builds a new Drupal-based project using DDEV.
    * Creates, configures and Deploys a new Drupal site in the current location.
    * Installs and enable some Basic Drupal Modules ready for work: devel, masquerade, admin_toolbar and webprofiler.
    * Builds subtheming for the project: Creates the custom subtheme, libraries declaration, a initial JavaScript file and an initial empty file for CSS styling.
    * Puts the Drupal instalation in dev mode turning off the cache system and enabling TWIG debug.
    * Installs and enable subtheme.
    * Installs node, npm and Angular.
    * Shows a whole report with info about the installation.
    * Launches the new Drupal Site in Browser and connect to the container's prompt.
