Selectik
========
Selectik is jQuery select plugin, easy use, cross-browser alternative to the standard select form element which can be customised with CSS.
All features of custom select and help you can find on <a href="http://brankub.github.com/selectik">demo page</a>.

Features:
---------
* TAB key control
* original select key control
* mouse wheel control
* search by first letter
* custom/default scroll
* smart positioning
* auto/cutsom width

Support browsers:
-----------------
IE7+, Chrome, Safari, Firefox.

Usage
-----
First include in html head tag stylesheet for custom selects (you can customize demo CSS file), jQuery, jQuery mousewheel plugin (included in project), and Selectik .js file:

`<head>
...
<link rel="stylesheet" type="text/css" href="css/selectik.css" /> // CSS for Selectik
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script> // jQuery library
<script type="text/javascript" src="js/jquery.mousewheel.js"></script> // mousewhell plugin
<script type="text/javascript" src="js/jquery.selectik.js"></script> // Selectik plugin
...
</head>`

You can choose what select should be custom by class, id or use for all selects on page by tag:

For all selects on page:
`$(document).ready(function(){
$('select').selectik();
});`

Only with some class/id:
`$(document).ready(function(){
$('.someclass').selectik();
});`

Plugin parametrs
----------------

+ **Container class (containerClass)** - for customizing class of main div around custom and original select. Default value - 'custom-select'.

+ **Width of custom select (width)** - if you willn't use this parametr custom select will be with width of bigger option. Default value - '0'.

+ **Maximum items (maxItems)** - you can put max quantity of options that should be visible. If quantity of options will be bigger plugin will put scroll. If value of this paramentr will be '0', all options will be visible. Default value - '0'.

+ **Type of scroll (customScroll)** - choose type of scroll (custom or original). 1 - custom, 0 - original. Default value - '1'.

+ Speed of animation (speedAnimation)** - speed of show/hide animation in milliseconds. Default value - '200'.
                                                                                                      - 
Example of using parametrs:
`$('select').selectik({
width: 300,
maxItems: 5,
customScroll: 0,
speedAnimation: 100
});`

Plugin API
----------

API of plugin are utils which used when necessary to reload, show/hide, enable/disable, change selected option or set dynamicly width of select.

In Selectik jQuery store a reference to the plugin of object by 'data'. In this case you should use 'data' and know what select to control.
Reload custom select when original was changed:
`$('.first select').data('selectik').refreshCS();`

Show/hide list:
`$('.second select').data('selectik').showCS();` // show list
`$('.second select').data('selectik').hideCS();` // hide list

Change selected option:
`$('.first select').data('selectik').changeCS({index: 1});` // set first option 'selected'
`$('.first select').data('selectik').changeCS({value: 'New'});` // set selected options with value 'New'

Set width:
`$('.third select').data('selectik').setWidthCS(200);` // set width 200px

Enable/disable select:
`$('.first select').data('selectik').disableCS();` // disable select
`$('.first select').data('selectik').enableCS();` // enable select

        
        