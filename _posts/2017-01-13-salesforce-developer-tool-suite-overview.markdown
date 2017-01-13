---
layout: post
author: Artyom Kukharev
title: "Salesforce Developer Tool Suite Overview"
comments: true
date: 2017-01-13 16:00:00 +0300
tags:
- chrome
- debug
- developer tool suit
- extension
- logs
- salesforce
- sdts
---
Usually you would get logs from developer console, MavensMate, Force.com IDE or another your favorite environment. But without comparing, it's hard to decide what will be more comfortable for you and suits your requirements so let's have a look on the different ways of retrieving debug logs from a Salesforce org.
<!--more-->

Not so far ago I have found `Salesforce Developer Tool Suite` (<em>SDTS</em>). It is a Chrome Extension (you can download it from the Chrome Web Store) which allows you to view debug logs in a simple way.

> SDTS gives you:
>
>* hierarchical view of debug logs, which are better to analyse.
>* ability to set logging level or traceflags for any users or apex code.
>* tracking of logs for multiple users in same windows, as different tabs.

Let's take a brief look and compare it with the existing developer console.
Go to <a href="https://chrome.google.com/webstore/detail/salesforce-developer-tool/fiaakhiohminpblhmlihfcdhclmphjcd" target="_blank">the google web store</a> and install the extension to Chrome.  The small icon in the top right corner <img class="alignnone size-full wp-image-62" src="{{ site.baseurl }}/assets/images/sfdst-offline1.png" alt="sfdst-offline" width="39" height="37" /> indicates whether your page has opened Salesforce org or not.

Login to any existing org. The icon will become active <img class="alignnone size-full wp-image-65" src="{{ site.baseurl }}/assets/images/sfdst-on.png" alt="sfdst-on" width="39" height="38" />. Now we can start working with the Developer Tool Suite.

The first thing that I've noticed is that you can operate with debug logs easily. They are presented in a well structed form and have enough related information listed near them.
<img class="alignnone size-full wp-image-90" src="{{ site.baseurl }}/assets/images/sfdst-main-window.png" alt="sfdst-main-window" width="812" height="601" />

You can switch between logs of a particular user and all logs:
<img class="alignnone size-full wp-image-112" src="{{ site.baseurl }}/assets/images/sfdst-logs-switch.png" alt="sfdst-logs-switch" width="777" height="98" />

When you click on action dropdown you see available options for viewing logs. You can view logs in the same window as the SDTS extension, download them to the computer, open in a new browser tab or even in a new window:

<img class="alignnone size-full wp-image-95" src="{{ site.baseurl }}/assets/images/sfdst-action-dropdown.png" alt="sfdst-action-dropdown.png" width="159" height="204" />

You can change settings to show logs only with `DEBUG` level, hide `time`, `objectId` field etc.
<img class="alignnone size-full wp-image-100" src="{{ site.baseurl }}/assets/images/sfdst-logs-options.png" alt="sfdst-logs-options" width="612" height="125" />

Debug log levels can be set up in that way: click on `settings` button and then on `MANAGE DEBUG LEVELS`.
<img class="alignnone size-full wp-image-116" src="{{ site.baseurl }}/assets/images/sfdst-logs-deblev.png" alt="sfdst-logs-deblev" width="788" height="601" />

You will see this modal window:
<img class="alignnone size-full wp-image-116" src="{{ site.baseurl }}/assets/images/manage-debug-levels.png" alt="manage-debug-levels" />

Click on `NEW DEBUG LEVEL`, fill name, tracing levels(Apex Code, Visualforce, Apex Profiling etc.) and then save <img class="alignnone size-full wp-image-116" src="{{ site.baseurl }}/assets/images/save-log-level.png" alt="save-log-level" />

Pretty easy, right?
For now let's configure tracing logic.
<img class="alignnone size-full wp-image-116" src="{{ site.baseurl }}/assets/images/trace-config.png" alt="trace-config" />

`NEW TRACE CONFIG` button `->` select object to trace (User / Class / Trigger) `->` type name of the record, expiration date and debug level that we've created earlier.
That's all.


# Here are the list of the coming soon features:
> * Ability to create TraceFlags for classes and triggers
> * Ability to show desktop notifications when watching for logs
> * "remembering where you left" keep the extension in same state where you last left it i.e. if you are viewing a debug log and somehow closed the popup, opening it next time will show the same.

# Some thoughts
Generally, you would use completed multifunctional IDE instead of this Chrome extension, but there are some circumstances when SDTS can be useful.
This extension is really convenient to use when you would like to see debug logs just in one click without opening developer console or other IDE. SDTS helps you collect all the logs in the one place and in the same tab.