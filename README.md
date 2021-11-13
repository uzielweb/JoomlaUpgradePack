# JoomlaUpgradePack


## How to fix Jupgrade Migrating undefined error when upgrading to Joomla 2.5
*2012-11-05 by Alessandro Pasotti filed under Joomla.*
Recently I had an error message while migrating and old Joomla! 1.5 site to the new Joomla! 2.5, jupgrade failed with “Migrating undefined” error. 
After digging in the code I found a solution: You have to edit two files: 
jupgrade/installation/models/configuration.php 
jupgrade/installation/models/database.php 
and insert the following line near the top of the script: 
require_once JPATH_ROOT.'/jupgrade/libraries/cms/model/legacy.php'; 
When done (after the failed upgrade), you can retry the migration checking the following options in Jupgrade configuration:ex

*Original article: https://www.itopen.it/fixing-jupgrade-migrating-undefined-error-when-upgrading-joomla/*


# JUPGRADE PRO Packages

Install it in a Joomla 2.5 or 3.5 website and than get data from old 1.0, 1.5 and 2.5 websites.
