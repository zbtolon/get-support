---

copyright:

  years: 2015, 2018

lastupdated: "2019-02-18"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Best practices for monitoring status
{: #best-practices}

To stay informed and plan accordingly, use the following best practices for monitoring the status of {{site.data.keyword.Bluemix}}.
{: shortdesc}

## Check for upcoming maintenance windows
{: #monbp-checmaintwin}

Check for upcoming maintenance windows posted on the {{site.data.keyword.Bluemix_notm}} console Dashboard page, at least once every 24 hours, by using one of the following options:
* Check out the Planned maintenance widget on the [Dashboard ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){: new_window}. Click **All events** to view all planned maintenance.
* Navigate directly to the [Status - Planned maintenance ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/status?selected=maintenance){: new_window} page

## Check for current maintenance windows or an incident in progress
{: #monbp-checcurmaninprog}

If you suspect that {{site.data.keyword.Bluemix_notm}} isn't functioning as expected, check the Status page for current maintenance windows or an incident in progress. To report an incident that isn't already listed on the Status page, open a support case by clicking **Support** from the menu bar. Then, click **Create new case** on the Get support tab.

## Take advantage of multiple {{site.data.keyword.Bluemix_notm}} locations
{: #monbp-multpreg}

All users of {{site.data.keyword.Bluemix_notm}} automatically have access to the Dallas, London, Frankfurt, Sydney, Washington DC, and Tokyo locations. The {{site.data.keyword.Bluemix_notm}} Global Operations team manages all locations to avoid maintenance impacts and minimize the risk of incidents that affect all locations at the same time.

To switch locations, go to your dashboard and expand the **LOCATION** menu.

## Prepare for minor interruptions
{: #monbp-prepmininter}

In most cases, {{site.data.keyword.Bluemix_notm}} can continue to be used normally, even during the maintenance window. However, minor interruptions of a service can't always be avoided. Running applications typically remain available even if the application management functions of {{site.data.keyword.Bluemix_notm}}, such as starting and stopping apps, are temporarily interrupted. To maximize the availability of your running applications, run at least three instances of each application.

## Subscribing to email notifications
{: #monbp-subscribing}

If you're a Lite account owner, you can select whether to receive email notifications about {{site.data.keyword.Bluemix_notm}} platform unplanned events, such as outages, and planned events, such as maintenance. Additionally, if you have a Pay-As-You-Go or Subscription account, you can choose whether to receive {{site.data.keyword.Bluemix_notm}} infrastructure email notifications about unplanned events, maintenance, and announcements. For more information, see [Setting email preferences](/docs/account?topic=account-account_setup#account_setup).



