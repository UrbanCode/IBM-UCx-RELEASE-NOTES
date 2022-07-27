





7.0.4.2

**This article was originaly published in 2019.12.03**


What’s New in UrbanCode Deploy 7.0.4.2
======================================




This release of IBM UrbanCode Deploy is a maintenance release and includes various bug fixes and enhancements. This release is recommended for all customers.Release Summary
---------------

  
* Recommended fixes for UrbanCode Deploy

Release Notes
-------------

  
For information on documentation and support resources, software and hardware requirements and installation steps, see the Getting Started page.


Fixes
-----




|  |  |
| --- | --- |
| [PH17700](http://www.ibm.com/support/docview.wss?uid=swg1PH17700) | ON LAPTOPS WITH SMALL MONITORS, OR UNDER HIGH ZOOM, THE 'OK' BUTTON IS MISSING WHEN SELECTING VERSIONS TO DEPLOY. |
| [PH17506](http://www.ibm.com/support/docview.wss?uid=swg1PH17506) | CHOOSE-VERSION WINDOW WHILE DEPLOYING APPLICATION APPEARS TRUNCATED POST UPGRADE TO 7.0.3.1 FROM 6.2.7.2. |
| [PH17276](http://www.ibm.com/support/docview.wss?uid=swg1PH17276) | WHEN USING LDAP for authentication, the GROUP REALM'S CONNECTION DETAILS are IGNORED |
| [PH17009](http://www.ibm.com/support/docview.wss?uid=swg1PH17009) | UNABLE TO ADD TEAMS TO A GENERIC PROCESS VIA THE REST CALL |
| [PH16897](http://www.ibm.com/support/docview.wss?uid=swg1PH16897) | UNVERSIONED COMPONENT REQUESTS DO NOT SHOW ON THE DEPLOYMENT DETAIL REPORT. |
| [PH16717](http://www.ibm.com/support/docview.wss?uid=swg1PH16717) | WHEN BASE RESOURCES ARE ADDED TO ENVIRONMENT TWICE DUPLICATE ENTRIES ARE INSERTED IN THE DATABASE |
| [PH16539](http://www.ibm.com/support/docview.wss?uid=swg1PH16539) | HISTORY CLEANUP DOES NOT LOG COMPLETION MESSAGES |
| [PH16257](http://www.ibm.com/support/docview.wss?uid=swg1PH16257) | UCD CREATE APPLICATION WIZARD UI ISSUE |
| [PH16019](http://www.ibm.com/support/docview.wss?uid=swg1PH16019) | INTEGRITY CONSTRAINT VIOLATION WHEN CLEANING UP GHOSTED ENVIRONMENT RECORDS |
| [PH15826](http://www.ibm.com/support/docview.wss?uid=swg1PH15826) | MAX SIMULTANEOUS PROCESSES FEATURE NOT WORKING WITH APPLICATION TEMPLATES |
| [PH15133](http://www.ibm.com/support/docview.wss?uid=swg1PH15133) | COMPONENT VERSIONS REVERSED AFTER IMPORT/EXPORT FROM ONE APPLICATION SNAPSHOT TO ANOTHER APPLICATION. |
| [PH15130](http://www.ibm.com/support/docview.wss?uid=swg1PH15130) | SNAPSHOT EXPORT/IMPORT ISSUE INTO THE SAME SERVER, ARTIFACTS DISAPPEAR AFTER IMPORTING FROM ONE APPLICATION TO ANOTHER. |
| [PH14948](http://www.ibm.com/support/docview.wss?uid=swg1PH14948) | WHEN PROPERTY FILES ARE RENAMED UCD WILL NOT START. |
| [PH13513](http://www.ibm.com/support/docview.wss?uid=swg1PH13513) | UCD SERVER STARTUP FAILS WITH DRAFTPROCESSCREATIONUPGRADER ERROR |
| [PH13242](http://www.ibm.com/support/docview.wss?uid=swg1PH13242) | LARGE TABLE DS\_LICENSE\_LOG\_ENTRY CAUSES PERFORMANCE ISSUES |
| [PH12776](http://www.ibm.com/support/docview.wss?uid=swg1PH12776) | FLOATING LICENSES OCCASIONALLY NOT RELEASED IN HA ENVIRONMENTS |
| [PH11564](http://www.ibm.com/support/docview.wss?uid=swg1PH11564) | COMPLIANCE UNCHANGED IF INSTALLATION AND ROLLBACK BOTH FAIL |
| [PI99408](http://www.ibm.com/support/docview.wss?uid=swg1PI99408) | PLUGIN.XML NOT VALIDATED AGAINST SCHEMA WHEN PLUGIN LOADED |
| [PI97459](http://www.ibm.com/support/docview.wss?uid=swg1PI97459) | REOCCURRING ERROR - JAVA.IO.IOEXCEPTION: UNABLE TO UNWRAP DATA, INVALID STATUS [CLOSED] |
| [PI84390](http://www.ibm.com/support/docview.wss?uid=swg1PI84390) | RESOURCE PROPERTIES DEFINED IN THE RESOURCE TEMPLATE ARE NOT IMPORTED TO RESOURCES CREATED USING THE TEMPLATE. |
| [PI82637](http://www.ibm.com/support/docview.wss?uid=swg1PI82637) | AUTO-COMPLETE FOR PROPERTIES NO LONGER WORKS FOR THE SHELL SCRIPT |


Getting Started
---------------

  

Upgrade Notes
-------------


**Starting in 7.0.4.0**
All customers should note that with the UrbanCode Deploy 7.0.4.0 release, **we are officially announcing end of support for DB2 on z/OS on October 8th, 2020**. Starting with 7.0.4.0, new installations of UCD will not be able to use a DB2 on z/OS database. Servers upgraded to 7.0.4.0 can continue to use existing DB2 on z/OS databases, but those servers will not be eligible for support after October 8th, 2020.

**Starting in 7.0.3.0**

All customers should note that with the UrbanCode Deploy 7.0.3.0 release, **we are officially announcing end of support for JMS Communication on June 11th, 2021**. All users are strongly encouraged to upgrade to UrbanCode Deploy 7.x, and migrate to the new WebSocket communication.

With the addition of [Maintenance Mode](https://developer.ibm.com/urbancode/2019/06/07/deploy-703-maintenance-mode/) deployments that were scheduled to run while the server was down will no longer automatically execute upon the starting of the server.

During testing of UrbanCode Deploy 7.0.3.0, we experienced upgrade issues with version 5.0.8 of the MySQL driver. No other tested versions had this issue. If you are upgrading to UrbanCode Deploy 7.0.3.0, please verify that you have a recent version of the MySQL driver if that is the database of your choice.

**Starting in 7.0.2.1**

Users with the "Manage Security" permission will now be able to copy security roles. This functionality will make it easier for managing a large number of similar roles.

**Starting in 7.0.2.0**

All customers should note that with the UrbanCode Deploy 7.0.2.0 release, **we are officially announcing end of support for Java 6 and Java 7 on February 17th, 2020**

UrbanCode Deploy now supports Java 11, and as part of that support we upgraded the version of Groovy we support from 1.8.8 to 2.4.15. If you have customer plugins that statically reference the groovy libraries shipped within the UrbanCode product, you will need to update those references or else your plugin steps will fail on newly installed agents.

For customers who are planning to upgrade to Java 11: If you choose to move off of Oracle Java and move to AdoptOpenJDK, you will need to modify the set\_env file to remove the "endorsed dir" entry, as it is not supported in the AdoptOpenJDK JVM.

Also, we would like to let our customers know that in our testing we discovered that users who are using MariaDB can no longer use MySQL drivers due to a change between MySQL and MariaDB. Please ensure you are using the correct database drivers.

**Starting in 7.0.1.0**
UrbanCode Deploy 7.0.1.0 introduces the concept of Agent Configuration Templates (which are used in migrating agents from JMS communication to the new WEB communication). This upgrade did not grant the System Team access to Agent Configuration Templates. Users will need to grant these permissions to if users on that team wish to access the functionality.

It should also be noted that some of the servers code station metadata has been migrated to the database. Specifically, it is the content of the $APPDATA/var/repository/ptr directory. This stores the association between component versions and artifact blob files. This resolves some server-side performance issues that negatively impacted relay codestation cache cleanup. The old data files are preserved without modification to support upgrade rollback. However, they are not updated going forward. This means that a later rollback would break new, post-upgrade version artifact associations (blobs files would remain but would be inaccessible).

**Starting in 7.0.0.0**

UrbanCode Deploy 7.0 introduces new functionality that allows you to add process change management to your deployment processes. This functionality is still in BETA, and we are actively looking for customer feedback. If you would like to access a cloud instance of UCD, to use and provide feedback without having to set it up, please reach out to your IBM representative and let them know!

UrbanCode Deploy 7.0 also introduces new server/agent communication protocols.
* For new installations of the Deploy server users will be prompted for additional information unconditionally (all new installs will default to the web socket protocol).
* When installing new Deploy agents, users will be asked for their preference, either JMS or web sockets. The default is web.
* When upgrading the Deploy server, the user will be prompted for additional information to support the web socket protocol, however, no agents will change communication protocols as part of the upgrade.
* An interactive (manual) upgrade of an agent will also prompt for new information to support the web sockets protocol. Upgrading through the web-ui will upgrade existing agents and keep them on the current server/agent communication (JMS)
* It should be noted that in all scenarios, UrbanCode Deploy supports running both the new agent communication (web sockets) with the older model (JMS) in parallel.


 

**Starting in 6.2.7.1**

API-breaking changes have been made to the supported REST endpoints that set properties in UCD, affecting the following endpoints:
* setAgentProperty
* setApplicationProperty
* setComponentEnvironmentProperty
* setComponentProperty
* setEnvironmentProperty
* setResourceProperty
* setSystemProperty
* setVersionProperty


 

Any scripts that need to set properties on components, agents, the system, processes, process requests, applications, or environments will need to be adjusted. Previously, the request parameters could be specified on the command line as parameters, **but now we no longer accept request parameters for security reasons**. Instead, the correct behavior now is now to pass a JSON file containing the specified parameters with the command. Consult the [documentation](https://www.ibm.com/support/knowledgecenter/SS4GSP_6.2.7/com.ibm.udeploy.api.doc/topics/rest_cli_environment_propvalue_put.html) for the new syntax.

Also, because of these API changes, the plugins that set properties in UCD are not backwards compatible. In the following list of plugins, any plugin version before the version listed is not compatible with UCD 6.2.7.1 or later, and and any plugin version after the version listed is not compatible with 6.2.7.0 or earlier. On upgrading to UCD 6.2.7.1, the plugins will automatically be updated to a supported version. However, using old versions of processes that are locked in snapshots or downgrading the UCD plugin version may cause steps to fail.


|  |  |
| --- | --- |
| Plugin | 6.2.7.1+ compatible versions |
| IBM UrbanCode Deploy Applications | 77+ |
| IBM UrbanCode Deploy Components | 71+ |
| IBM UrbanCode Deploy Environments | 77+ |
| IBM UrbanCode Deploy Resources | 74+ |


**Starting in 6.2.5.2**

Starting the server for the first time may take longer than usual. For very large installations, allow an extra hour for the first server startup. Subsequent startups will take the regular amount of time.

Users now do not receive notifications based on their membership in a role on the System Team. Users will have to be added to the correct role on a different team as well to receive notifications.

The server now deletes all contents of the var/temp directory on server startup.

**Starting in 6.2.5.1**

Process requests from deleted environments will now be deleted. To keep process requests from deleted environments, add this property to the installed.properties file: com.urbancode.ds.cleanup.HistoryCleanup.disableDeletedEnvironmentCleanup=true

**Starting in 6.2.5.0**

The UCD\_SESSION\_KEY header has been renamed to UCD\_CSRF\_TOKEN. The previous name is also accepted until 6.3 when it will be removed from the product.

Users now require the “Execute” permission on agents in order to run processes against them. All existing user roles will receive this permission when upgrading from a version before 6.2.5.0. When upgrading, ensure that any user that needs to execute processes is on the same team as the agents required to run those processes.

**Starting in 6.2.4.0**

You must upgrade Agent Relays when upgrading from a version below 6.2.4.0. Also, the TLS protocol 3DES is no longer supported.

After upgrading from before 6.2.4.0, users will not be able to view or delete agent relays until they have been granted permission to those relays. Relays that existed before the upgrade are only added to the System Team by default. For users to view agent relays, a user with Manage Security permission should give the correct roles the new For relays that existed before the upgrade, a user with Manage Security permissions will have to add the agent relays to the correct teams and give the correct roles the Agent Relay view and edit permissions.

When upgrading an IBM UrbanCode Deploy agent, end-to-end JMS encryption will automatically be enabled on all agents. In order for agent communication to function properly with end-to-end encryption enabled, the IBM UrbanCode Deploy server and agent clocks need to be synchronized to within a few minutes. To disable this feature, add the line `agent.jms.disable_full_encryption=true`” to the agent’s `conf/agent/installed.properties` file before upgrading the agent.

**Starting in 6.2.3.0**

If you are upgrading from version 6.2.3.0 and earlier, servers and relays must be upgraded at the same time. Agents connected through relays may not connect successfully until both server and relay are upgraded. This is due to an incompatibility between versions of an library used by UCD.

Starting in 6.2.3.0, authentication tokens will be obfuscated in the UI and REST API after their initial creation. Scripts and users will only be able to retrieve the full authentication token immediately after creating it.

The silent install of the IBM UrbanCode Deploy server hangs when prompting for the value of the server installation directory (`install.server.dir`). To workaround the problem, run the following instead of calling `./install-server.sh` directly:
 `echo "" > answerFile.txt echo "" >> answerFile.txt ./install-server.sh < answerFile.txt (or install-server.bat < answerFile.txt for Windows installations)` 
**Starting in 6.2.2.0**

The IBM UrbanCode Deploy server and agent relays now require a Java Runtime Environment (JRE) or Java Development Kit (JDK) version 8. If you are updating or changing the JRE to the latest version, see
[Changing or updating the JRE of servers](http://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.2.4/com.ibm.udeploy.doc/topics/jre_change.html#jre_change) and [Updating the JRE location for agent relays](http://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.2.4/com.ibm.udeploy.doc/topics/update_JRE_agent_relays.html#update_JRE_agent_relays) for instructions. For documentation on the IBM JRE, see [IBM SDK, Java Technology Edition](https://www.ibm.com/support/knowledgecenter/SSYKE2/welcome_javasdk_family.html).

**Starting in 6.2.1.1**

To ensure that all secure property values are obscured, the values of all properties in the history for existing deployments are obscured. In the deployment history for deployments that you run after you upgrade, only secure properties are obscured in the logs.

New security features erase old component version import logs to hide secure information. If you want to keep the logs, in the installed.properties file, set the **com.urbancode.ds.cleanup.sourceConfig.fullCleanupSkip** property to **true**.



Plan & Prepare
For fixes contained in this release, and any known issues, review the [release notes](../release-notes).

For supported platforms and requirements, see the reports that can be dynamically generated using the [Software Product Compatibility Reports (SPCR)](https://www.ibm.com/software/reports/compatibility/clarity/index.html) tool.

**Note:** Some supported plug-ins have system requirements that vary from the core product. Information on system requirements for individual plug-ins is available on the download page for that plug-in.

To get started quickly, IBM UrbanCode Deploy is shipped with an Apache Derby database. Apache Derby deployments are not supported for production environments. As you plan your production topology, review the [installation guide](http://www.ibm.com/support/knowledgecenter/SS4GSP_7.0.4/com.ibm.udeploy.install.doc/topics/install_ch.html).





Install the server
------------------


This release is available for download from [Fix Central](https://www-945.ibm.com/support/fixcentral/swg/downloadFixes?parent=ibm~Rational&product=ibm/Rational/IBM+UrbanCode+Deploy&release=All&platform=All&function=fixId&fixids=7.0.4.2-IBM-UrbanCode-Deploy&includeRequisites=1&includeSupersedes=0&downloadMethod=http), requiring authentication.

Information for installing the server, see the [Installing server](http://www-01.ibm.com/support/knowledgecenter/SS4GSP_7.0.4/com.ibm.udeploy.install.doc/topics/install_ch.html) section in the product documentation.

For information on installing licenses, see [Managing Licenses](https://www.ibm.com/support/knowledgecenter/SS4GSP_7.0.4/com.ibm.udeploy.doc/topics/licenseManage.html).




Learn
-----


To learn more about new enhancements in this release, see [What’s New](../) .

To learn more about IBM UrbanCode Deploy, see the [documentation](http://www-01.ibm.com/support/knowledgecenter/SS4GSP_7.0.4/com.ibm.udeploy.doc/ucd_version_welcome.html).

For help installing or using IBM UrbanCode Deploy, post your questions in the [forums](https://developer.ibm.com/answers?community=urbancode) or contact [support](http://www-947.ibm.com/support/entry/portal/support?brandind=Rational).

To suggest an enhancement to the product, visit the [RFE Community](http://www.ibm.com/developerworks/rfe/execute?use_case=submitRfe).




Get support
-----------


For information from support, including FAQs, visit the [IBM Support portal.](https://www.ibm.com/support/home) You can configure the support portal to view information about specific products.






