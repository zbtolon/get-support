---

copyright:

  years: 1994, 2019

lastupdated: "2019-08-19"

keywords: data centers, data center support, dal01 pod, wdc01 pod 

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Withdrawal of support for some US data centers
{: #dc-migrate}

IBM is withdrawing support for the following data centers in the United States: 

* dal01 pods 1, 4, and 5
{:shortdesc}

##  Why am I required to move to another data center?
{: #required-data}

To continue bringing you the best service, hardware, and connectivity, all of the sites are continually evaluated to ensure that they meet networking, electrical, and other infrastructure standards. Even though these sites are adequate, they no longer meet the ongoing standards.

## Do I have to be fully migrated by the date listed?
{: #data-list}

Yes. To ensure that you have no interruption in service, we're trying to allow as much lead time as possible to make the transition easy. We communicated this site movement in May 2018.

## Will I need to move to another data center ever again?
{: #move-data}

We constantly evaluate the quality of our sites to bring you the best and most dependable service. It's possible that we might have other moves as we continue to evaluate some of the older sites.

## Can I choose any {{site.data.keyword.Bluemix_notm}} US data center?
{: #us-data}

Yes, you can choose any US IBM site that meets your location needs.

## How do I select which data center to deploy to?
{: #deploy-data}

IBM has more than 60 data centers in locations around the world. View the data center map on our global data centers page to see which data centers you can deploy in. 

The following factors might influence which data center you select:
* Proximity to the users of the systems
* Proximity to any other systems that this server needs to communicate with
* Any data policies or regulations that require data to be stored in a specific location

## Am I required to also use US sites for the transition period?
{: #transition}

You can use any worldwide {{site.data.keyword.cloud_notm}} site during your transition period, which lasts up to 60 days.

## Are the two free months of transition period resources in addition to my existing server time?
{: #free}

Yes. You can contact an appropriate support representative who can help you through the process of acquiring your transition period servers.

## How do I determine my current hardware configuration?
{: #current-hardware}

Log in to the customer portal. From the **Device List**, select the server that you're interested in and find the system configuration details. From there, you can view the processor type, for example, Single Intel Xeon E3-1270 (4 Cores, 3.50 GHz). You can also view the amount of memory (RAM), storage, and other data.

## How do I determine the utilization of my current hardware?
{: #utilization} 

Most operating systems provide tools that you can use to understand the utilization of your system, for example, vmstat and iostat on Linux or Windows System Performance Monitor. There are also many other performance monitoring tools that might be available to you. Performance monitoring and tuning is something that you might invest significant time and effort in. In general, you need to understand whether there are specific resources within the system (processor, memory, disk, network) that are heavily used or not used. Having this information can help you better size your new system. For example, a system where memory capacity is frequently overcommitted is likely to benefit from larger memory sizes in the target system that you migrate to.

## How do I compare old and new processors?
{: #old-new}

To compare the specifications of old and new Intel processors, go to [https://ark.intel.com/content/www/us/en/ark.html#@Processors](https://ark.intel.com/content/www/us/en/ark.html#@Processors){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"). If you know the processor type, you can navigate through the menus. Alternatively, you can use the search option to locate the specifications of the two processors. Newer processors tend to have more processor cores and typically run at slower clock speeds than older variants. If you have a workload that is processor-bound (its performance is limited by the speed of the processor), we advise choosing a processor with fewer cores and a higher clock speed.  If you run many workloads that aren't constrained by processor speed, choosing a processor with more cores and a similar, or slower, clock speed might be a better course of action.

## How do I choose my new operating system?
{: #operating-system}

If the server is in use for many years and not kept up-to-date, it's likely that you're running an older version of the operating system. This can present challenges with the migration. You might not have the installation media for the old operating system to install from.  You might also find that the newer server hardware you're migrating to is not supported by the older operating system version. You might need to choose a different operating system to move to.

The operating system choice might be prescribed by the applications that you're running. As part of the migration, you might need to run the application on a later version of the operating system. Ensure that it works on the newer version.

Available skills in a particular operating system might also influence your choice. If you have the source code for the application, ensure the necessary development tools and supporting operating system or middleware functions are available on the new platform. In general, Linux type systems are better at supporting older applications on newer versions of the operating system than Windows.

## What bandwidth do I get with my new configuration and is it at the same rate I currently have?
{: #bandwidth}

You receive a current bandwidth package that is most closely related to the package you currently have. The rate for that package is whatever your current rate or package includes.

## How do I copy data from my old server to the new one?
{: #old-server}

After you establish connectivity between the old and new servers, you should consider how you move data between them.  Assuming that you have sufficient storage in the new server to accommodate the volume of data, a direct server-to-server copy is the simplest way to achieve this.  There are many tools available that you can use.  

* scp is a good choice to securely copy a file from source to destination. It performs a plain linear copy. 
* If you need to copy multiple files, rsync over ssh is much faster than scp. rsync also copies directory structures and preserves file permissions.

In general, you should only copy applications and application data between systems. Copying older versions of operating system files to a newer version can cause problems.

Shut down databases before you copy them between the systems to ensure that the data is consistent. When migrating database data, ensure that data is migrated in a way that doesn’t limit your options to import it into the new system. Rather than copy database data from system to system, consider exporting it to a format so you can import it to a newer database. Flat text files, CSV files, and other files, provide more options than using proprietary or closed file formats when it comes to moving data between systems. Always test your data migration approaches on a small set of test data before doing the official copying.

## Do I need to set up my networking again at the new site?
{: #networking}

Most likely your networking needs to change to work with the new servers and site. If you need help with this process, contact support team by phone or chat.

## What do I do if I don’t have the skills to migrate?
{: #migrate-skills}

Application migration can be a complex undertaking. Not the least of these are the skills that are required to do this. If code changes are required to the application, make sure that you have the required programming skills. This is the case with older systems where skills might be in short supply or there's a lack of documentation or knowledge about the system itself. If there's significant effort and the system is critical to the business, consider investing in paid services or other migration services to help you.

## How do I get general help with the migration?
{: #gen-migration}

Depending on the level of help you need, you can contact support by phone or chat. Or you can contact the managed services team for assistance.

## Who do I contact if I don’t have an account manager?
{: #account-contact}

You can contact support by phone or chat for any migration questions that you have.
