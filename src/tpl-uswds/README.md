## Additional Information/Notes

The current state of this template is to provide the CSS, Header, and Footer for rapid prototyping of Service Portals.  **This template should not be used to produce 'Production Ready' portals.** However; it can give you a good jump start. 

You can read more about this standard from [their site](https://designsystem.digital.gov/).

The template package contains:

USWDS Service Portal
  * Configured to use the USWDS Theme and supporting Service Portal (Demo) menus
  
USWDS Theme Record contains -
  * CSS Includes (2) - Font(s) import and the USWDS CSS
  * JS Include - USWDS Javascript API
  * Bootstrap overrides with SASS variable as part of the CSS variables block

Service Portal Menus - Three (3) menus are provided in order to demonstrate the power of the template.  Configuration of the menus is explained below.
  * USWDS Primary - Demonstrate the 'basic' menu 
  * USWDS Secondary - Demonstrate the 'extended' menu capabilities
  * USWDS Footer - Menu for demonstrating the footer menu capabilities

Five (5) Widgets – 
  * USWDS Header (uswds-header)
  * USWDS Header Menu (uswds-header-menu)
  * USWDS Header Secondary Menu (uswds-header-secondary-menu)
  * USWDS Footer (uswds-footer)
  * USWDS Typeahead Search (uswds-typeahead-search)


## Installation

Download and install the Zipped Images for the site **[uswds_images_base.zip](https://raw.githubusercontent.com/platform-experience/portal-template-library/master/src/tpl-uswds/uswds_images_base.zip)**

* SN Product Documentation - ['Upload one or more images'](https://docs.servicenow.com/bundle/madrid-platform-user-interface/page/administer/navigation-and-ui/task/t_UploadingMultipleImages.html)

Download and install update set **[tpl-uswds.u-update-set.xml](https://raw.githubusercontent.com/platform-experience/portal-template-library/master/src/tpl-uswds/tpl-uswds.u-update-set.xml)**

_**NOTE:**_ You will get import errors during the update set preview process because of the menu records.  Just **'Accept remote update'** on all the error records from the **Update Set Preview Problems** tab.

* SN Product Documentation - ['Load a customization from a single XML file'](https://docs.servicenow.com/bundle/kingston-application-development/page/build/system-update-sets/task/t_SaveAnUpdateSetAsAnXMLFile.html)

## Configuration

The USWDS standard accounts for multiple presentation formats of [Header](https://designsystem.digital.gov/components/headers/) and [Footer](https://designsystem.digital.gov/components/footers/).  We have built the Header and Footer widgets to __dynamically__ adjust based on the amount of menu choices setup in the respective menus (included).

The Service Portal record's **Quick start config** is used to identify when different elements of the Header and Footer are to be used.

```
[{
  "auto_menu": false,
  "secondaryMenu": {"sys_id": "07c3a78f4fc83b008272ece24210c718"},
  "secondaryWishCartList": true,
  "fluid" : true,
  "megamenu" : true,
  "footerMenu" : {
	"sys_id": "d5cc2ef34f44fb008272ece24210c7a2",
    "contact" : {
		"center" : "USWDS PMO",
		"phone" : { "text" : "(800) CALL-WDS", "dial" : "1-800-555-1212" },
		"email" : "info@uswds.gov"
	},
	"social": [
		{"name":"Facebook", "link":"https://www.facebook.com"},
		{"name":"Twitter", "link":"https://www.twitter.com"},
		{"name":"YouTube", "link":"https://www.youtube.com"},
		{"name":"RSS", "link":"https://en.wikipedia.org/wiki/RSS"}
	]
  }
}]
```

### Quick start config

Explanation of the JSON structure and variables in the **Quick start config**
 * **auto_menu** - if no menu is identified then generate menu items for the KB and Service Catalog associated with the portal
 * **secondaryMenu** - the sys_id of the Service Portal Menu to be used as the secondary menu in the header
 * **footerMenu** - data used to generate the footer
     * _sys_id_ : Sys ID of the Service Portal Menu to be used
     * _contact_ : Contact information to be rendered in the footer
     * _social_ : Social Media links to be rendered _**Please Note:**_ the images generated are limited to the examples above
 * **secondaryWishCartList, fluid, and megamenu** - _**not currently implemented**_
