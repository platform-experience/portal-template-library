## Additional Information/Notes

This __template__ package is contains:

Page Layouts – Three (3) layouts that can be used as the portal home page
 * Primary : __pg_home_bondi__ - pre-configured with widgets below
 * Two (2) alternates : __pg_home_alt_1_bondi__ & __pg_home_alt_2_bondi__

Bondi Theme Record

Seven (7) Widgets – 
  * [Navigation Left-Collapsible](https://sc.service-now.com/snds?state=widget-detail&sys_id=c2636430db7bef40b4d974921f9619a2) ( __Desktop Only__ ) <br/>
   ** _Mobile generates as a standard mobile drop-down header_
  * [Welcome Widget - Time of Day Greeting](https://sc.service-now.com/snds?state=widget-detail&sys_id=18e86f42db676b00b41f70921f9619e5)
  * [Typeahead – Flat and Rounded Ends](https://sc.service-now.com/snds?state=widget-detail&sys_id=852e445adb2f6b00b41f70921f961905)
  * [Big - Link To Button](https://sc.service-now.com/snds?state=widget-detail&sys_id=c7ac623ddb676b00b4d974921f9619dc)
  * [Small - Link To Button](https://sc.service-now.com/snds?state=widget-detail&sys_id=78c25fc2dba763403eb8f4bbaf961937)
  * [Highlight User Assets](https://sc.service-now.com/snds?state=widget-detail&sys_id=a7ab506adb6feb00b41f70921f961946)
  * [Popular and My Recent Items](https://sc.service-now.com/snds?state=widget-detail&sys_id=65485c5adb63a3403eb8f4bbaf961963)

_Click on the widgets above to view more info and download individually_

## Installation

Download and install update set **[tpl-bondi.u-update-set.xml](https://raw.githubusercontent.com/platform-experience/portal-template-library/master/src/tpl-bondi/tpl-bondi.u-update-set.xml)**

* SN Product Documentation - ['Load a customization from a single XML file'](https://docs.servicenow.com/bundle/kingston-application-development/page/build/system-update-sets/task/t_SaveAnUpdateSetAsAnXMLFile.html)

## Configuration

We have attempted to cover all the various types of Service Portal Menu options in our support of generating the navigation menu.  There are, howver; _some_ menu scenarios that currently do not function the same as if they were in a normal top navigation header.  

By default none of the configurations below are __required__ in order to use this template and contents.
To take advantage of some of the widget's uniques unique capabilites the following configurations can be applied to the Portal Record.  _Please see individual widgets documentation to learn more about each widget's Instance Option configurations._

#### Navigation Left - Collapsible
---

* __Auto Menu__ - if you do not have a Service Portal Menu and would like to have menu options for the Portal Record's Knowledge Base and Catalog pages generate, then add the following to the 'Quick start config'.
```
[{
	"auto_menu": true
}]
```

* __Secondary Menu__ - There can be a 'top' navigation header that functions as a second menu.  To configure the Secondary Menu use the following syntax in the 'Quick start config' of the Portal record.
```
[{
	"secondaryMenu": {"sys_id": "53616d1e3b013200367aee1234efc439"}
}]
```

* __CSM Virtual Agent vs Live Connect__ -   The Virtual Agent will only launch if the Portal Record's 'Quick start config' is configured with a Secondary Menu.  If a Secondary Menu is not present then the Live Chat will still show in the left navigation list, however; it will only launch the Live Connect at this time. __Note__: the 'Chat Queue' for the portal must also be configured.  Example 'Quick start config':
```
[{
	"secondaryMenu": {"sys_id": "53616d1e3b013200367aee1234efc439"},
	"isCSM":true,
	"default_interaction_queue": "0e4d82d0738513000f4012562ef6a772"
}]
```
