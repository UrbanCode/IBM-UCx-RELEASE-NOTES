





New and Updated Integrations

**This article was originaly published in 2015.09.01**


New and Updated Integrations - September, 2015
==============================================





### FileUtils (Updated)


* Added step for retrieving properties from an XML file
* Added Include and Exclude fields to the unzip plugin step
* Added Destination Directory field to the Update XML File with XPath step
* Update Property File step to have text area inputs for includes and excludes to allow editing multiple property files.
* Modified Untar step to allow wildcards for tarball name.
* Updated Unzip step to use the system default encoding.
* Updated the ‘Update XML File with XPath’ plugin step to correctly get the encoding from the prolog of the XML Document.e
* Updated the ‘Update INI File’ plugin step. Added option to allow users to add comments to sections. Added an option to give the user a choice between ‘;’ and ‘#’ for comments. The default comment character will now be ‘;’. Fixed a bug where sections were deleted if they did not have a property. Multiple comments are allowed but empty lines between comments will not be preserved.
* Added an option to the ‘Update Property File’ plugin step which causes it to read the properties file using the agent’s native encoding or a custom character encoding
* Changed name of the ‘Update Property File’ step to be ‘Update Java Properties File’ to clarify that it is used with Java Properties files. Fixed an issue in the ‘Update INI File’ step where comments at the end of the file would be deleted. Added option to the ‘Update INI File’ step to allow the user to specify the encoding of the INI file and added an option to let them delete sections from an INI file.
* Fixed APAR PI31431 – the ‘Replace Tokens’ properties file was not being deleted if the step failed.
* Fixed APAR PI37793 – Update Java Properties File was throwing NullPointerException if property value was empty
* Fix broken upgrades so the plugin can be loaded into servers with older versions of the plugin
* Learn more about this plug-in [for version 6.1 and later](https://developer.ibm.com/urbancode/plugin/file-utils-ubuild/)




### Rally (Updated)


* Fix some issues when creating defects and changing Rally artifact properties when using Rally’s v2.0 API
* Learn more about this plug-in [for version 6.1 and later](https://developer.ibm.com/urbancode/plugin/rally-ubuild/)







