Algolia Search for Magento
==================

[Algolia Search](http://www.algolia.com) is a hosted full-text, numerical, and faceted search engine capable of delivering realtime results from the first keystroke.

This extension replaces the default search of Magento with a typo-tolerant, fast & relevant search experience backed by Algolia. It's based on [algoliasearch-client-php](https://github.com/algolia/algoliasearch-client-php) and [algoliasearch-client-js](https://github.com/algolia/algoliasearch-client-js).


See features and benefits of [Algolia Search Extension for Magento](https://www.algolia.com/with/magento).

![Latest version](https://img.shields.io/badge/latest-1.1.0-green.svg)
![Magento 1.6.2](https://img.shields.io/badge/magento-1.6.2-blue.svg)
![Magento 1.7.1](https://img.shields.io/badge/magento-1.7.1-blue.svg)
![Magento 1.8.1](https://img.shields.io/badge/magento-1.8.1-blue.svg)
![Magento 1.9](https://img.shields.io/badge/magento-1.9-blue.svg)
![PHP >= 5.3](https://img.shields.io/badge/php-%3E=5.3-green.svg)

Installation
--------------

### Using the packaged Community Extension

To setup this module using the packaged Community Extension, download the last version from our [releases](https://github.com/algolia/algoliasearch-magento/tree/master/releases) directory and upload it on your Magento instance.

### Using Modman

To setup this module using [modman](https://github.com/colinmollenhour/modman) (a module manager for Magento) run the following commands:

```sh
$ cd /path/to/your/magento/directory
$ modman init
$ modman clone https://github.com/algolia/algoliasearch-magento.git
```

### Using Composer

To setup this module using [Composer](https://getcomposer.org/) (a dependency manager for PHP), just add ```"algolia/algoliasearch-magento": "*"``` to your ```composer.json``` file.

Features
--------

### Search bar with auto-complete

This extension adds an auto-completion menu to your search bar displaying products and categories "as-you-type".

![Auto-completion](doc/auto-completion.gif)

### Typo-tolerant full-text search

This extension replaces the default full-text search feature of your Magento instance providing you a typo-tolerant & relevant search experience.

![Full-text search](doc/fts.png)


Configuration
--------------

To setup this module, you'll need an Algolia account. Just sign up [here](http://www.algolia.com/users/sign_up) to create an account and retrieve your credentials.

### Credentials & Activation

Once the extension is installed, a new **Algolia Search** menu will appear in your **System > Configuration** menu.

![Configuration menu](doc/configuration-menu.png)

In the first block of the configuration panel, you'll be able to setup your credentials and to enable to search features.

To replace Magento's default Full-Text search algorithm by Algolia, set **Enable Catalog Search** to `Yes`. To add an auto-completion menu to your search bar, set **Enable Auto-completion Menu** to `Yes`.

![Configuration panel](doc/configuration-credentials.png)

Once done, go to **System > Catalog > Catalog Search > Search Engine** and select **Algolia** as the Search Engine used to search your catalog.

![Catalog search](doc/catalog-search.png)


### Products Configuration

This section of the configuration allows you to configure how your **Product** records will look like in Algolia. List here all the attributes you need to search, rank and display your products. The order of this setting matters as those at the top of the list are considered more important.

Use the **Ranking** configuration to specify the numerical attribute used to reflect the popularity of your products. By default, we recommend using the number of ordered quantity as popularity criteria.

![Configuration panel](doc/configuration-product.png)

### Categories Configuration (auto-completion menu only)

This section of the configuration allows you to configure how your **Category** records will look like in Algolia. List here all the attributes you need to search, rank and display your categories. The order of this setting matters as those at the top of the list are considered more important.

Use the **Ranking** configuration to specify the numerical attribute used to reflect the popularity of your categories. By default, we recommend using the number of products in the category as popularity criteria.

![Configuration panel](doc/configuration-category.png)

Initial import
-----------------

Once configured, do not forget to trigger the re-indexing in **System > Index Management**:

![Index management](doc/index-management.png)


Instant-search
---------------

If you want to build an instant-search based result page refreshing the whole page (results, pagination & navigation filters) “as you type” you can follow this [tutorial](http://www.algolia.com/doc/tutorials/instant-search).

![Instant search](doc/instant-search.gif)

