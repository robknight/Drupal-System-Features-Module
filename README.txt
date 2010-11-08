System Features Module
----------------------

Created by Rob Knight <http://drupal.org/user/36475>

Introduction
------------

The System Features module provides basic integration between Features and
Drupal "system" objects - modules and themes (the current version supports only
modules).  This means that module enablement and weight can be exported to a
feature.  When this feature is installed and/or reverted, the modules in
question will be enabled and their weights will be set according to the feature
configuration.

Usage
-----

The primary intended usage of system features is for deployment scenarios.  For
example, where you might run a script to enable certain modules and adjust the
weights, it is now only necessary to enable and revert the feature which does
this work for you, and this can be achieved via Drush.

System Features can be used to do some of the work commonly done by install
profiles, but is more flexible because install profiles are only run once and
cannot be updated and run again on the same installation.  System Features can
run on existing sites (e.g. cloned sites) as part of a scripted or manual update
process.

To create a System Feature, go to the Features admin page and create a feature
in the normal way.  To add modules, choose "Module Status" from the "Add
Components" drop-down menu, and select the modules that you want to export the
status of.  Once you have selected the modules, you can download the feature and
being using it.

Upon reverting the feature, modules will be either enabled or disabled according
to their status in the feature, and their weights will also be adjusted.

Feedback
--------

The information about usage above is based on my own needs.  I'd really like to
hear about what other people are using this module for, or ways in which they
think it could be improved.  Feel free to contact me at mail@robknight.org.uk .