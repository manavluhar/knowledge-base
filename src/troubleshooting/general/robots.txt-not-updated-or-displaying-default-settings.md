---
title: robots.txt not updated or displaying default settings
labels: 2.3.x,2.4.x,Magento Commerce,Magento Commerce Cloud,configuration,default,robots.txt,settings,troubleshooting
---

The article provides a solution for when you have configured `robots.txt` correctly, for example per [Best practices for Magento robots.txt](https://support.magento.com/hc/en-us/articles/360048754931) but the `robots.txt` is not getting updated or is displaying the default settings.

## Affected products and versions

* Magento Commerce (Cloud) 2.3.x, 2.4.x

## Issue

Cannot change the default `robots.txt` setting.

 <span class="wysiwyg-underline">Steps to reproduce:</span> 

1. Access the Magento Admin panel.
1. Add content to **Content** > Design > **Configuration** > **Edit Custom instruction of `robots.txt` ** file such as the text "hello" and save the changes.

Visit the `robots.txt` url.

 <span class="wysiwyg-underline">Expected result:</span>  `robots.txt` has the saved text. <span class="wysiwyg-underline">Actual result:</span> 

 `robots.txt` file does not change.

## Cause

Indexing by search engines is turned off.

## Solution

Enable indexing by search engines. See [Configure indexing by search engine](https://devdocs.magento.com/cloud/trouble/robots-sitemap.html#configure-indexing-by-search-engine) in Magento Developer Documentation.

## Related reading

* [DevDocs Add site map and search engine robots](https://devdocs.magento.com/cloud/trouble/robots-sitemap.html)

