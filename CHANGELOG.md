# Capistrano::Magento2 Change Log

0.2.2
==========

* Revert "Add workaround for M2.0.4 bug noted in magento/magento2#4070"

0.2.1
==========

* Fixed issue with initial deploy failing before 'current' link has been created on target

0.2.0
==========

* Added "smart" magento:setup:di:compile task which uses multi-tenant if available (for compatibility with 2.0 release)
* Added a command_map for the bin/magento tool to simplify rake files
* Added indexer:info, indexer:status, indexer:show-mode, indexer:set-mode
* Added maintenance:status and maintenance:allow-ips, exposes maintenance:disable
* Fixed broken error detection logic on setup:static-content:deploy
* Fixed bug where magento:setup:upgrade was not using the --keep-generated flag
* Fixed log bloat caused by chatty static-content:deploy
* Fixed missing dependency include in deploy.rb
* Fixed output of magento:cache:varnish:ban command
* Fixed potential issue where if a botched release was in production, one could not roll back
* Fixed technical dependency bug preventing projects from overriding the deploy.rake with a custom one
* Renamed capistrano/magento2/deploy/notify to capistrano/magento2/notifier
* Renamed magento:reset_permissions to magento:setup:permissions
* Renamed magento:setup:static_content:deploy to magento:setup:static-content:deploy
* Updated composer calls to explicitly set  --prefer-dist and --no-interaction
* Updated README to reflect current setup instructions

0.1.3
==========

* Changed magento:cache:varnish:ban to use `:varnish_cache_hosts` array in deploy config vs hardcoding 127.0.0.1:6081

0.1.2
==========

* Added information to README file regarding use of terminal-notifier functionality

0.1.1
==========

* Initial functional release, tested with Magento 2.0.4 / PHP 7.0.5
