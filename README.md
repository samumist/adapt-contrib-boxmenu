# adapt-elfboxmenu

This is a modification of the
[adapt-contrib-boxmenu](http://github.com/adaptlearning/adapt-contrib-boxmenu),
for installation and other infomation, please visit the original repo's
[wiki](http://github.com/adaptlearning/adapt-contrib-boxmenu/wiki).

## Settings Overview

The attributes listed below are used in *contentObjects.json* to configure **the
elfboxmenu**, and are properly formatted as JSON in
[*example.json*](https://github.com/samumist/adapt-elfboxmenu/blob/master/example.json).

### Attributes

**_id** (string): This is a unique identifier that establishes relationships with other content structures. It is referenced in *articles.json* as the `_parentid` of an article model.   

**_parentId** (string): This value is sourced from the parent element's `_id` found within *course.json*. It must match. 

**_type** (string): This value determines what the learner will access by clicking the provided link/button. Acceptable values are `"page"` and `"menu"`. `"page"` will direct the learner to a page structured with articles, blocks, and components. `"menu"` will direct the learner to a page with more menus. 

**_classes** (string): CSS class name to be applied to menu item's `page`
element (*src/core/js/views/pageView.js*). The class must be predefined in one of the Less files. Separate multiple classes with a space.

**title** (string): This text is a reference title for the content object.

**displayTitle** (string):  This text is displayed on the menu item.

**body** (string):  Optional text that appears on the menu item. Often used to inform the learner about the menu choice. If no **pageBody** is supplied, this text will also appear as the body text of the page header.

**pageBody** (string): Optional text that appears as the body text of the page header. If this text is not provided, the **body** text will be used (if it is supplied). Reference [*adapt-contrib-vanilla/templates/page.hbs*](https://github.com/adaptlearning/adapt-contrib-vanilla/blob/master/templates/page.hbs).

**_graphic** (object): The image that appears on the menu item. It contains
values for **alt**, **locked** locked and **src**.

>**alt** (string): This text becomes the image’s `alt` attribute.

>**src** (string): File name (including path) of the image. Path should be relative to the *src* folder (e.g., *"course/en/images/t05.jpg"*).  

>**locked** (string): File name (including path) of the image for the locked. Path should be relative to the *src* folder (e.g., *"course/en/images/t05.jpg"*).  
       
**linkText** (string): This text is displayed on the menu item's link/button.  

**linkLockedText** (string): This text is displayed on the locked menu item's link/button.  

**linkVisitedText** (string): This text is displayed on the visited menu item's link/button.  

**duration** (string): Optional text which follows **durationLabel** (e.g., `"2 mins"`).  
       
<div float align=right><a href="#top">Back to Top</a></div>  

### Accessibility
Several menu-related elements are assigned a label using the
[aria-label](https://github.com/adaptlearning/adapt_framework/wiki/Aria-Labels)
attribute: **ariaRegion**, **menuItem**, and **menuEnd**. These labels are not
visible elements. They are utilized by assistive technology such as screen
readers. Should the label texts need to be customised, they can be found within
the **globals** object in
[*properties.schema*](https://github.com/samumist/adapt-elfboxmenu/blob/master/properties.schema).   
<div float align=right><a href="#top">Back to Top</a></div>

## Limitations
 
No known limitations.  

----------------------------
**Version number:**  2.0.0   <a href="https://community.adaptlearning.org/" target="_blank"><img src="https://github.com/adaptlearning/documentation/blob/master/04_wiki_assets/plug-ins/images/adapt-logo-mrgn-lft.jpg" alt="adapt learning logo" align="right"></a> 
**Framework versions:**  2.0     
**Author / maintainer:** Adapt Core Team with [contributors](https://github.com/adaptlearning/adapt-contrib-boxmenu/graphs/contributors)  
**Accessibility support:** WAI AA   
**RTL support:** yes  
**Cross-platform coverage:** Chrome, Chrome for Android, Firefox (ESR + latest version), Edge 12, IE 11, IE10, IE9, IE8, IE Mobile 11, Safari for iPhone (iOS 8+9), Safari for iPad (iOS 8+9), Safari 8, Opera 
