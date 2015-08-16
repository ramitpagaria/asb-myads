# Setting Up Image/Flash/HTML Banners #

[ASB MyAds](http://www.adserverbeans.com/asb_myads.html) currently supports 3 banner types:
  * image (jpeg, png, bmp, gif, etc.)
  * Flash (swf)
  * HTML (html)

All these types are recognized automatically by file extension on file upload.

For Flash and HTML banners you should use special syntax (clickTAG) when defining click-through URL. Our system will inject target URL automatically and count the click.

Example of ActionScript code within a Flash banner:
```
on (release) {
  if (_root.clickTAG.substr(0,5) == "http:") {
    getURL(_root.clickTAG, "_blank");
  }
}
```
Example of an HTML banner:
```
<a href="${clickTAG}" target="_blank">Website Design</a>
```