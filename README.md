# JoomlaUpgradePack

## How to fix Jupgrade Migrating undefined error when upgrading to Joomla 2.5
*2012-11-05 by Alessandro Pasotti filed under Joomla.*

Recently I had an error message while migrating an old Joomla! 1.5 site to the new Joomla! 2.5, jupgrade failed with “Migrating undefined” error.  
After digging in the code I found a solution: You have to edit two files:  
`jupgrade/installation/models/configuration.php`  
`jupgrade/installation/models/database.php`  
and insert the following line near the top of the script:  
`require_once JPATH_ROOT.'/jupgrade/libraries/cms/model/legacy.php';`  
When done (after the failed upgrade), you can retry the migration checking the following options in Jupgrade configuration:ex

*Original article: [https://www.itopen.it/fixing-jupgrade-migrating-undefined-error-when-upgrading-joomla/](https://www.itopen.it/fixing-jupgrade-migrating-undefined-error-when-upgrading-joomla/){:target="_blank"}*

# JUPGRADE PRO Packages

Install it in a Joomla 2.5 or Joomla 3.x website and retrieve data from old 1.0, 1.5, and 2.5 websites. It is better to use the database method.

# Upgrading Versions
[https://docs.joomla.org/Portal:Upgrading_Versions](https://docs.joomla.org/Portal:Upgrading_Versions){:target="_blank"}

## Migration

The documentation below is a funnel starting with Why Migrate. Simply follow the buttons at the bottom of each page that are applicable to you. The Self Assessment will help you determine if doing the migration is within your skill set. Please don't skip the Planning pages as they include important information for your migration.

- [Why Migrate](https://docs.joomla.org/Special:MyLanguage/Why_Migrate){:target="_blank"}
- [Migration Step by Step Self Assessment](https://docs.joomla.org/Special:MyLanguage/Migration_Step_by_Step_Self_Assessment){:target="_blank"}
- [Planning for Migration](https://docs.joomla.org/Special:MyLanguage/Planning_for_Migration){:target="_blank"}

- [Updating a Joomla CMS 3.x.x Installation](https://docs.joomla.org/Special:MyLanguage/J3.1:Updating_from_an_existing_version "Special:MyLanguage/J3.1:Updating from an existing version"){:target="_blank"}
    - [Updating Joomla CMS 3.x.x (Update Method)](https://docs.joomla.org/Special:MyLanguage/J3.x:Updating_Joomla_(Update_Method) "Special:MyLanguage/J3.x:Updating Joomla (Update Method)"){:target="_blank"} **_recommended method_**
    - [Updating Joomla CMS 3.x.x (Install Method)](https://docs.joomla.org/Special:MyLanguage/J3.x:Updating_Joomla_(Install_Method) "Special:MyLanguage/J3.x:Updating Joomla (Install Method)"){:target="_blank"}
- [Updating a Joomla CMS 2.5.x Installation](https://docs.joomla.org/Special:MyLanguage/J2.5:Updating_from_an_existing_version "Special:MyLanguage/J2.5:Updating from an existing version"){:target="_blank"} **EOS**
    - [Updating Joomla CMS 2.5.x (Update Method)](https://docs.joomla.org/Special:MyLanguage/J2.5:Updating_Joomla_(Update_Method) "Special:MyLanguage/J2.5:Updating Joomla (Update Method)"){:target="_blank"} **_recommended method_**
    - [Updating Joomla CMS 2.5.x (Install Method)](https://docs.joomla.org/Special:MyLanguage/J2.5:Updating_Joomla_(Install_Method) "Special:MyLanguage/J2.5:Updating Joomla (Install Method)"){:target="_blank"}

## [Migration](#Migration)

The documentation below is a funnel starting with Why Migrate. Simply follow the buttons at the bottom of each page that are applicable to you. The Self Assessment will help you determine if doing the migration is within your skill set. Please don't skip the Planning pages as they include important information for your migration.

- [Why Migrate](https://docs.joomla.org/Special:MyLanguage/Why_Migrate "Special:MyLanguage/Why Migrate"){:target="_blank"}
- [Migration Step by Step Self Assessment](https://docs.joomla.org/Special:MyLanguage/Migration_Step_by_Step_Self_Assessment "Special:MyLanguage/Migration Step by Step Self Assessment"){:target="_blank"}
- [Planning for Migration](https://docs.joomla.org/Special:MyLanguage/Planning_for_Migration "Special:MyLanguage/Planning for Migration"){:target="_blank"}

### [Migration 1.5 to 3.x](#Migration_1.5_to_3.x)

- [Planning Migration - Joomla 1.5 to 3](https://docs.joomla.org/Special:MyLanguage/Planning_Migration_-_Joomla_1.5_to_3 "Special:MyLanguage/Planning Migration - Joomla 1.5 to 3"){:target="_blank"}
- [Joomla 1.5 to 3.x Step by Step Migration](https://docs.joomla.org/Special:MyLanguage/Joomla_1.5_to_3.x_Step_by_Step_Migration "Special:MyLanguage/Joomla 1.5 to 3.x Step by Step Migration"){:target="_blank"}
- [Migrating a Template from Joomla 1.5 to 3.x](https://docs.joomla.org/Special:MyLanguage/Migrating_a_Template_from_Joomla_1.5_to_3.x "Special:MyLanguage/Migrating a Template from Joomla 1.5 to 3.x"){:target="_blank"}

### [Migration 2.5 to 3.x](#Migration_2.5_to_3.x)

- [Planning for Mini-Migration - Joomla 2.5 to 3.x](https://docs.joomla.org/Special:MyLanguage/Planning_for_Mini-Migration_-_Joomla_2.5_to_3.x "Special:MyLanguage/Planning for Mini-Migration - Joomla 2.5 to 3.x"){:target="_blank"}
- [Joomla 2.5 to 3.x Step by Step Migration](https://docs.joomla.org/Special:MyLanguage/Joomla_2.5_to_3.x_Step_by_Step_Migration "Special:MyLanguage/Joomla 2.5 to 3.x Step by Step Migration"){:target="_blank"}
- [Joomla 2.5 to 3.x Common Migration Errors](https://docs.joomla.org/Special:MyLanguage/Joomla_2.5_to_3.x_Common_Migration_Errors "Special:MyLanguage/Joomla 2.5 to 3.x Common Migration Errors"){:target="_blank"}

### [Migration 3.10 to 4.x](#Migration_3.10_to_4.x)

- [Planning for Mini-Migration - Joomla 3.10 to 4.x](https://docs.joomla.org/Special:MyLanguage/Planning_for_Mini-Migration_-_Joomla_3.10.x_to_4.x "Special:MyLanguage/Planning for Mini-Migration - Joomla 3.10 to 4.x"){:target="_blank"}
- [Joomla 3.10 to 4.x Step by Step Migration](https://docs.joomla.org/Special:MyLanguage/Joomla_3.x_to_4.x_Step_by_Step_Migration "Special:MyLanguage/Joomla 3.x to 4.x Step by Step Migration"){:target="_blank"}
- [Joomla 3.10 to 4.x Common Migration Errors](https://docs.joomla.org/Special:MyLanguage/Joomla_3.10_to_4.x_Common_Migration_Errors "Special:MyLanguage/Joomla 3.10 to 4.x Common Migration Errors"){:target="_blank"}

### [Update 4.4 to 5.x (new)](#Update_4.4_to_5.x_.28new.29)

- [Pre-Update Check](https://docs.joomla.org/Special:MyLanguage/J4.x:Pre-Update_Check "Special:MyLanguage/J4.x:Pre-Update Check"){:target="_blank"}
- [Planning for Update - Joomla 4.4.x to 5.x](https://docs.joomla.org/Special:MyLanguage/Joomla_4.4.x_to_5.x_Planning_and_Upgrade_Step_by_Step "Special:MyLanguage/Joomla 4.4.x to 5.x Planning and Upgrade Step by Step"){:target="_blank"}
- [Pre-Update Check](https://docs.joomla.org/Special:MyLanguage/J4.x:Pre-Update_Check){:target="_blank"}
- [Planning for Update - Joomla 4.4.x to 5.x](https://docs.joomla.org/Special:MyLanguage/Joomla_4.4.x_to_5.x_Planning_and_Upgrade_Step_by_Step){:target="_blank"}
****
