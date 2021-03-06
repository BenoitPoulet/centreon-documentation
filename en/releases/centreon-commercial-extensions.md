---
id: centreon-commercial-extensions
title: Commercial Extensions
---

## Introduction

You can find in this chapter all changelogs concerning **Centreon Commercial
Extension**.

> It is very important when you update your system to refer to this section in
> order to learn about behavior changes or major changes that have been made on
> this version. This will let you know the impact of the installation of these
> versions on the features you use or the specific developments that you have
> built on your platform (modules, widgets, plugins).

If you have feature requests or want to report a bug, please contact support.

## Centreon MAP

### 20.04.0

* Simplify packaging: The packaging has been simplified so we don't require Tomcat. Logs are now
accessible in `/var/log/centreon-map/` and the service is now `centreon-map`
(*systemctl restart centreon-map*). [Follow the upgrade procedure](../graph-views/upgrade.html)
* Silent installation: It's now possible to install Centreon Map using a silent mode instead of the
only interactive mode.
* License on Central server: The licensing system has been simplified. The MAP license resides now on the Centreon **central** server, as any other
commercial extension. No worry, the compatibility with the previous licensing mecanism (license on the map server) is maintained.
* [API] Add metaservice endpoint
* [API] Simplify authentication
* [API] Use the reeal resource ID instead of internal resource ID
* It's now possible to manage how value are rounded on links

## Centreon BAM

### 20.04.1

* The default calculation method is now "Worst" when you create a business activity
* Business activities configuration: You're now able to save only warning thresholds
* Reporting: manage timeperiods different from 24x7 in charts & tables
* Improve "null" threshold displays
* Widget: manage worst/best/ratio status calculation methods

### 20.04.0

* New calculation methods available: Worst, Best & Ratio
* New planned downtime inheritance management: you can now ignore the indicator in the calculation
* Update all real time & configuration page to manage new calculation methods

## Centreon MBI

### 20.04.1

* Logo preview has been fixed
* Immediate rescheduling a job was setting the execution date in the future
* fix some translations in reports

### 20.04.0

* Manage compatibility with Centreon 20.04

## Centreon Auto Discovery

### 20.04.2

#### Enhancements

- Better handle forms testing in Host Discovery wizard
- Enhance error render for jobs

#### Bugfixes

- Unable to run Service Discovery since 20.04.1
- Some words are not translated in french
- Use $rg API directive to search in providers listing
- Remove bad characters in the JSON result in Host Discovery
- Mapper Monitoring - "From job" setting does not take job monitoring server

### 20.04.1

#### Enhancements

- Job with 0 discovered items redirects to empty job details

#### Bugfixes

- Overlapping text when configuring job with default proxy
- Use direct connection to Poller when having Remote Server is ignored by
  Service Discovery

### 20.04.0

Redesign hosts discovery with a new wizard to add discovery job:

  - Better credentials management
  - Possibility to define from where the discovery will be made
  - New *mappers* system and preview of result

The *mappers* system is a feature to map discovered items value with a
configuration value:

  - **association**: allows you to map the value of an attribute of a discovered
    resource with a property in the Centreon configuration (on a condition or
    not)
  - **macro**: allows you to map the value of an attribute of a discovered
    resource with a custom macro (on a condition or not)
  - **template**: allows to selected the template to apply (on a condition or
    not)
  - **monitoring**: allows to select the monitoring server which will monitor
    the discovered resource (on a condition or not)

## Centreon Plugin Packs Manager

### 20.04.1

  - Drop legacy table not used since PPM version 2.1.0 (PR #100)

### 20.04.0

  - Improve management of errors during Plugin Packs installation process
  - The procedures for installing Plugin Packs are now hosted on the official
    Centreon documentation

## Centreon License Manager

### 20.04.1

- Manage unlink platform from previous IMP trial to access to IT-100 free edition.

### 20.04.0

Remove `Administration > Extensions > Subscription` menu to manage IT Edition
subscription from `Administration > Extensions > Manager` menu:

  - Add a button to add a Centreon IT Edition subscription
  - Add a button to view a Centreon IT Edition subscription

Licenses for products linked to Centreon IT and Business Editions online
subscriptions are now automatically downloaded.
