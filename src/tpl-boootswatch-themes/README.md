## Additional Information/Notes

This is a set of 9 Service Portal themes adapted from the [Bootswatch]('https://bootswatch.com/3/') collection of open-source Bootstrap themes. Both theme variables and assignments of properties are included in a theme record. (Service Portal gives the property assignments extra specificity by reapplying them after any page, instance, or widget styling.)

Themes included are:

* Cerulean
* Cosmo
* Cyborg
* Darkly
* Lumen
* Sandstone
* Simplex
* United
* Yeti

Service-Portal-specific elements are also assigned properties extending the values of each theme. Any fonts specific to the themes are also included as links to Google Fonts, associated by CSS Include.

[//]: <> (SP-specific properties:)
[//]: <> (* set defaults for some homepage variables and elements.)
[//]: <> (* coordinates most input/form elements' properties – colors, height, etc.)
[//]: <> (* styles some configuration elements for readability.)
[//]: <> (* directly styles panels and alerts, bypassing Service Portal's mixins.)
[//]: <> (* restyles panels with white-border `b` class to context-based border color.)

Note: The hierarchy of Service Portal's CSS/Sass build appears to be gaining some additional options starting in Madrid, so property assignment will likely be properly broken out into separate include records for that release.

## Installation

Download and install update set **[tpl-bootswatch-themes.u-update-set.xml](https://github.com/platform-experience/portal-template-library/blob/master/src/tpl-bootswatch-themes/tpl-bootswatch-themes.u-update-set.xml)**

* SN Product Documentation - ['Load a customization from a single XML file'](https://docs.servicenow.com/bundle/kingston-application-development/page/build/system-update-sets/task/t_SaveAnUpdateSetAsAnXMLFile.html)

## Configuration

Open the portal record you would like to try a Bootswatch theme with, and select it in the Theme field.

Note: These themes are associated with the Stock Header record. To use the header of your choice, select in the Header field of the theme record.