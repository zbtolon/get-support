---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-01"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# How do I get a quick response to my ticket?
{: #quicktickresp}

When you contact support and open a support ticket, you can request a specific severity level, depending on the type and urgency of the problem. The severity level can affect how quickly your issue is addressed.
{:shortdesc}

You define the severity of the issue based on your business needs and your level of support. See [Support plans](/docs/get-support/index.html) for more information about levels of support plans. All tickets are investigated to identify and resolve the root cause of the issue. When problem diagnostic data is needed to determine the root cause of the issue, you are asked for approval to access log files and other problem determination data from your application. Without this data, the resolution of your issue might be delayed.

## Collecting diagnostic information
{: #collecting-diagnostic-information}

To diagnose and resolve problems with {{site.data.keyword.Bluemix_notm}} applications and services, the {{site.data.keyword.Bluemix_notm}} Support team might ask you to collect diagnostic information. Use the following instructions to gather and provide the requested information as quickly as possible.

Before you collect diagnostic information, complete the following steps:

1. Ensure that you have installed the latest cf command line interface. For more information, see [Installing the cf command line interface](/docs/starters/install_cli.html).
>**Note:** If you do not have the latest cf command line interface installed, after the cf command line is connected to {{site.data.keyword.Bluemix_notm}}, the `cf logs` command might not return output.
2. Ensure that you connected the cf command line interface to where {{site.data.keyword.Bluemix_notm}} is running by using the `cf api` command.

Use one of the following scripts to collect diagnostic information:

  * For Windows operating systems, download the [bmdiag-general.bat ![External link icon](../icons/launch-glyph.svg "External link icon")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} file and run it.
  * For Linux and Mac operating systems, download the [bmdiag-general.sh ![External link icon](../icons/launch-glyph.svg "External link icon")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} file and run it.

The scripts use the cf command line interface to extract the following information from your application environment:
  * Application logs
  * Application metadata
  * Configured routes
  * Events
  * Provisioned services

## Escalating support tickets
{: #escalation}

As an {{site.data.keyword.Bluemix_notm}} customer, you can request further assistance by escalating your case to the {{site.data.keyword.Bluemix_notm}} Support Manager on duty. The escalation process enables you to surface critical issues and also to voice your concern if you feel your support ticket is not being addressed appropriately. After a case is escalated, the manager on duty reviews the information in the support ticket, engages the appropriate members of the {{site.data.keyword.Bluemix_notm}} support technical team, and provides you with appropriate updates.

To escalate a support ticket, you must have an active {{site.data.keyword.Bluemix_notm}} Subscription account with basic, advanced, or premium support and you must have opened a support ticket for the issue.  Also, ensure that the technical issue is well documented in the support ticket that you opened.

 To escalate an issue, complete the following steps:

  1. Contact the {{site.data.keyword.Bluemix_notm}} Support Team by phone or chat :
    * By phone at the following number: 866-403-7638.
    * By chat from the {{site.data.keyword.Bluemix_notm}} [Support Center ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} or, if you have a SoftLayer account that is not linked, from the [customer portal ![External link icon](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Provide your existing ticket number and request to escalate the issue.
  3. Provide the justification for escalation and the business impact of your issue.

{{site.data.keyword.Bluemix_notm}} Support Managers are on duty and available 24 hours a day, every day of the week. The managers on duty engage the appropriate resources to address your issue and then inform you about the actions taken.


## Hours of operation
{: #support-hours-operation}

Severity 1 issues are monitored 24 hours a day, every day of the week. Form submissions for issues with all other severity levels are monitored from Sunday at 21:30 UTC to Friday at 23:59 UTC.

For assistance in converting these support hours to your local time zone, see [Timeanddate.com ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.timeanddate.com).
