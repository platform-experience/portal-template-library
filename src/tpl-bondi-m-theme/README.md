## Additional Information/Notes

Developed as part of the Bondi Template, this theme uses Bootstrap's theme template as a starting point for a comprehensive theming of Service Portal, and extends the rules of Bootstrap elements slightly. For example, Bondi uses a panel's context to color its `panel-body` section, and applies inverted text colors for its contents, other than specific components with their own coloring – tables, list groups, nav elements, etc.

Specific targeting in the stylesheet is used to address some conflicts with existing out-of-box Service Portal elements, but the theme should generally be compatible with elements using Bootstrap classes.

Out-of-box portal configurations tested with the theme include:

* Standard Service Portal
* Customer Service
* Customer Support
* HR Portal
* Service Catalog
* Knowledge
* Community

Along with their associated pages:

* Home / Landing pages and associated widgets
* List (and tiled) pages – e.g. Search results / Categorized views
* Forms and input elements – fields coordinated in size & style
* Other individual views: Ticket pages, Article view, User Profile, etc.

Theme has not been tested with all of these elements upon upgrade, so some adjustments may be needed for newer components with off-Bootstrap styles.

## Release Information

Note that this is a reconfiguration of the Bondi theme that was previously published for ServiceNow's London release, now also appropriately labeled as 'Bondi Theme for London' in this library. This version uses CSS Include records to associate stylesheets directly, lowering the burden of processing from a single Theme document, and allowing for clearer organization of variables. This version will not work in London or earlier releases.

## Installation

Download and install update set **[tpl-bondi-m-theme.u-update-set.xml](https://raw.githubusercontent.com/platform-experience/portal-template-library/master/src/tpl-bondi-m-theme/tpl-bondi-m-theme.u-update-set.xml)**

* SN Product Documentation - ['Load a customization from a single XML file'](https://docs.servicenow.com/bundle/kingston-application-development/page/build/system-update-sets/task/t_SaveAnUpdateSetAsAnXMLFile.html)

## Configuration

Open the portal record you would like to try the Bondi theme with, and select 'Bondi M+' in the Themes field.

Note that this theme is not associated with a Header or Footer record – to use together with the sidebar navigation, please download the Bondi Template, which includes them together. Or use the header of your choice – one can be selected in Header field of the theme record.