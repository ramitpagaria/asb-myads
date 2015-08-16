# Assigning Banners #

You should create a banner in the right panel and then drag it to a paddock of an ad place. As a result a new banner identical to the original one is created. The binding between the original and the newly created banner still exists. The banner is identified by:
<ul>
<li>banner name</li>
<li>banner file</li>
</ul>
That means if you change banner name or banner file of the original banner it will be automatically changed in all child banners.
All other banners settings are independent for each banner.

## Example 1 ##
You have a banner that you want to display on 3 ad places and you want to limit total number of views for this banner to 100,000.

## Solution ##
Create a banner and drag and drop it to 3 ad places. In banner settings (Targeting->Capping) set 'maximum number of views for the whole display period' to 33,333 for each cloned/dropped banner.

## Example 2 ##
Suppose you want to assign banners to "top left" of all pages.

## Solution ##
Depending on whether you need to generate separate reports for each top-left of your pages and target ads by something else than page position (eg. site section) you can create either one ad place (aggregate report) or multiple ad places (separate reports).
Most likely you are using a CMS such as Joomla or WordPress. Content management systems use templates to display content. We recommend creating one ad place for each page position and inserting its invocation code (ad tag) into the corresponding place in the template.