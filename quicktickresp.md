---

copyright:

  years: 2015, 2018

lastupdated: "2018-03-15"

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

You define the severity of the issue based on your business needs and your level of support. All tickets are investigated to identify and resolve the root cause of the issue. When problem diagnostic data is needed to determine the root cause of the issue, you will be asked for approval to access log files and other problem determination data from your application. Without this data, the resolution of your issue might be delayed.

If you are asked to supply diagnostic information, use the following instructions to gather and provide the requested information as quickly as possible.

## Collecting diagnostic information
{: #collecting-diagnostic-information}

To diagnose and resolve problems with {{site.data.keyword.Bluemix_notm}} applications and services, the {{site.data.keyword.Bluemix_notm}} Support team might ask you to collect diagnostic information.

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

## Can I escalate a support ticket?
{: #escalation}

With premium or advanced support, if you have not received a timely response to a support ticket, or if you feel that a support ticket is not being addressed appropriately, you can escalate the support ticket.  
{:shortdesc}

See [Types of support](/docs/get-support/getstarttssup.html#typesofsupport) for more information about premium and advanced support.

Through the support ticket escalation process, IBM management reviews your concerns and works with you to improve the support experience.

To submit an escalation request, complete the following steps:
  1. Open a new support ticket with the summary **Escalation Request**.
  2. To ensure that your escalation request can be matched with the original support ticket, include the following information in the body of the ticket:
      * The ticket number of your open support ticket that needs escalation.
      * A brief summary of the reasons that escalation is needed.

## Hours of operation
{: #support-hours-operation}

Severity 1 issues are monitored 24 hours a day, 7 days a week. Form submissions for issues with all other severity levels are monitored from Sunday at 21:30 UTC to Friday at 23:59 UTC (excluding holidays).

For assistance in converting these support hours to your local time zone, see [Timeanddate.com ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.timeanddate.com). For more information about the holiday schedule, see [{{site.data.keyword.Bluemix_notm}} Support Holidays ![External link icon](../icons/launch-glyph.svg "External link icon")](http://ibm.biz/bluemixholidays).
