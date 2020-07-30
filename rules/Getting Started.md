## Download the Zutilo plugin
First we need to install the Zutilo plugin for Zotero to get easy access to our document URIs and tags. To do so, follow the installation guide provided by [Zutilo](https://github.com/willsALMANJ/Zutilo/). 

Next we need to explicitly enable the URI feature. Therefore go to Zotero `Preferences` and then to the `Advanced` tab and hit the `Config Editor` button.

![[Zutilo_URI_1.png]]

Next, searrch for `zutilo.itemmenu` and change the value under `extensions.zutilo.itemmenu.copyZoteroItemURI` and `extensions.zutilo.itemmenu.copyZoteroSelectLink` from `Hide` to `Zutilo`.

![[Zutilo_URI_2.png]]

That's it, now you are good to go and can start adding your first papers to Zotero and Obsidian.

## Adding a new paper

To add a new paper to this repository, first add it to Zotero. You can follow our guide [in the wiki](https://isgroup.atlassian.net/wiki/spaces/ISG/pages/1650163800/Reference+Manager+Zotero) to get started. A convenient way to add documents to Zotero is adding them by DOI, arXiv id, or through the [Zotero connector plugin](https://www.zotero.org/download/connectors) for Google Chrome, Safari, or Firefox. 

> Don't forget to put your tags when adding a paper!

Once you added your literature with proper tags, you can add notes to Obsidian by duplicating the `_template` file and sorting it in the `research` folder. Please follow our naming conventions to keep things consistent and easy to find.

![[Naming Conventions]]

To link back from obsidian to Zotero, `right-click` your added paper in Zotero and click `Zutilo => Copy select item links`. Next, go back to Obsidian and paste the URI to your newly created page under `Zotero Select Link` on top. Do the same with `Copy Zotero URIs` and `Copy tags to clipboard`. 

![[Zutilo_URI_3.png]]

