---
title: PSTN connectivity options
author: CarolynRowe
ms.author: crowe
manager: serdars
ms.date: 07/08/2021
ms.topic: article
ms.service: msteams
audience: admin
ms.collection: 
  - M365-collaboration
  - M365-voice
  - m365initiative-voice
  - m365solution-voice
  - m365solution-scenario
ms.reviewer: crowe
f1.keywords:
- CSH
ms.custom: 
  - ms.teamsadmincenter.dashboard.helparticle.cloudvoice
  - seo-marvel-apr2020
  - seo-marvel-may2020
search.appverid: MET150
description: Learn more about Teams calling (PSTN connectivity) options and the decisions that you will make for your organization.
appliesto: 
  - Microsoft Teams
---


# PSTN connectivity options

Microsoft provides complete Private Branch Exchange (PBX) capabilities for your organization through Phone System. However, to enable users to make calls outside your organization, you need to connect Phone System to the Public Switched Telephone Network (PSTN).

This article focuses on PSTN connectivity options. For more information about Microsoft voice solutions, incuding details about Phone System features, see [Plan your Teams voice solution](cloud-voice-landing-page.md).

To connect Phone System to the PSTN, you can choose from the following options:

- [**Calling Plan**](#phone-system-with-calling-plan). An all-in-the-cloud solution with Microsoft as your PSTN carrier.

- [**Operator Connect**](#phone-system-with-operator-connect), which is currently available only in **public preview.**  With Operator Connect, if your existing carrier is a participant in the Microsoft Operator Connect program, they can manage PSTN calling and Session Border Controllers (SBCs). 

- [**Direct Routing**](#phone-system-with-direct-routing), which enables you to use your own PSTN carrier by connecting your Session Border Controller(s) (SBC) to Phone System.


You can also choose a combination of options, which enables you to design a solution for a complex environment, or manage a multi-step migration.

Be aware that the option or options you choose affect how some Phone System features are configured. For more information, see [Configuration considerations](#configuration-considerations) later in this article.


## Phone System with Calling Plan 

Phone System with Calling Plan is Microsoft's all-in-the-cloud voice solution for Teams users. This is the simplest option that connects Phone System to the PSTN. With this option, Microsoft acts as your PSTN carrier, as shown in the following diagram:

![Diagram 1 shows Phone System with Calling Plan.](media/voice-solutions-simple.png)

If you answer yes to the following, then Phone System with Calling Plan is the right solution for you:

- Calling Plan is available in your region.
- You do not need to retain your current PSTN carrier.
- You want to use Microsoft-managed access to the PSTN.

With this option: 

- You get Microsoft Phone System with added Domestic or International Calling Plans that enable calling to phones around the world (depending on the level of service being licensed).

- You do not require deployment or maintenance of an on-premises deployment&mdash;because Calling Plan operates out of Microsoft 365.

- Note: If necessary, you can choose to connect a supported Session Border Controller (SBC) through Direct Routing for interoperability with third-party PBXs, analog devices, and other third-party telephony equipment supported by the SBC.

This option requires uninterrupted connection to Microsoft 365.

For more information about Calling Plan, see the following articles:

- [Which Calling Plan is right for you?](calling-plan-landing-page.md)
- [How to buy a Calling Plan](calling-plans-for-office-365.md)
- [Country and region availability for Calling Plan](./country-and-region-availability-for-audio-conferencing-and-calling-plans/country-and-region-availability-for-audio-conferencing-and-calling-plans.md)
- [Set up Calling Plan](set-up-calling-plans.md)


## Phone System with Operator Connect

With Operator Connect, currently in public preview, if your existing carrier is a participant in the Microsoft Operator Connect program, they can manage the service for bringing PSTN calling to Teams. Your carrier manages the PSTN calling services and Session Border Controllers (SBCs), allowing you to save on hardware purchase and management.

Operator Connect might be the right solution for your organization if:

- Microsoft Calling Plan isn't available in your geographic location.
- Your preferred carrier is a participant in the Microsoft Operator Connect program.
- You want to find a new carrier to enable calling in Teams.

For information on the benefits and requirements of Operator Connect, and for a list of carriers participating in this program, see [Plan Operator Connect](operator-connect-plan.md). For information on how to configure Operator Connect, see [Configure Operator Connect](operator-connect-configure.md).


## Phone System with Direct Routing

This option connects Phone System to your telephony network by using Direct Routing, as shown in the following diagram: 

![Diagram 5 shows Phone System with Direct Routing.](media/voice-solution-with-direct-routing.png)

If you answer yes to the following questions, then Phone System with Direct Routing is the right solution for you:

- You want to use Teams with Phone System.
- You need to retain your current PSTN carrier.
- You want to mix routing, with some calls going through Calling Plan, some through your carrier.
- You need to interoperate with third-party PBXs and/or equipment such us overhead pagers, analog devices, and so on.

With this option:

- You connect your own supported Session Border Controller (SBC) to Phone System without the need for additional on-premises software.

- You can use virtually any telephony carrier with Phone System.

- You can choose to configure and manage this option, or it can be configured and managed by your carrier or partner (ask if your carrier or partner provides this option).

- You can configure interoperability between your telephony equipment&mdash;such as a third-party PBX and analog devices&mdash;and Phone System.

This option requires the following:

- Uninterrupted connection to Microsoft 365.

- Deploying and maintaining a supported SBC.

- A contract with a third-party carrier.
  (Unless deployed as an option to provide connection to third-party PBX, analog devices, or other telephony equipment for users who are on Phone System with Calling Plan.)

For more information about Direct Routing, see the following articles:

- [Plan Direct Routing](direct-routing-plan.md)
- [Configure Direct Routing](direct-routing-configure.md)
- [Manage voice routing policies for use with Direct Routing](manage-voice-routing-policies.md)
- [Plan Location-Based Routing for Direct Routing](location-based-routing-plan.md)
- [List of Session Border Controllers certified for Direct Routing](direct-routing-border-controllers.md)



## Configuration considerations

Most Phone System features are the same regardless of the PSTN connectivity option you choose. For example, call unanswered and forwarding settings, call transfer, custom music on hold, call park, shared line, and voice apps are all available. For a complete list of Phone System features, see [Here's what you get with Phone System](here-s-what-you-get-with-phone-system.md).

There are some differences in functionality, however, that affect how you configure certain Phone System features. For example, Direct Routing requires additional steps to configure call routing. As another example, Direct Routing provides Location-Based-Routing (LBR)--so that you can restrict toll bypass in certain geographic locations where it is not allowed. 

The following table highlights the primary configuration differences. The sections that follow the table provide links to more information and details.

| Option | Description | Phone number management | Call routing | Emergency calling availability |
| :------------| :-------| :-------| :-------| :-------| 
| Calling Plans | -Microsoft acts as PSTN carrier.<br>-You do not need to buy or manage SBCs.| Obtained through Microsoft.| -Managed by Microsoft. <br> -Admin configures user dial plans for number translation. | -Enabled by Microsoft. <br> -Admin registers addresses. <br> -Dynamic calling supported. |
| Operator Connect | -Carrier manages PSTN connectivity and SBCs. <br> -You do not need to buy or manage SBCs. | -Obtained through carrier. <br> - Numbers associated with emergency addresses managed by carrier.	| -Managed by carrier. <br>-Admin configures user dial plans for number translation. | -Enabled by carrier. <br> -Admin registers addresses. <br> -Dynamic calling supported. |
| Direct Routing | -Requires certified SBC purchased from third-party vendor.<br>-Connect your SBC to Phone System.<br> -Use your existing PSTN carrier. | Obtained through carrier. | -Requires extra configuration by admin.<br>-Admin configures trunk dial plans for number translation. <br>-LBR available to restrict toll bypass. | -Requires extra configuration by admin. <br>-Registered addresses not supported. <br>-Dynamic calling supported but requires additional configuration. |
|||||


### Phone number management

Microsoft has two types of telephone numbers available: subscriber (user) numbers, which can be assigned to users in your organization, and service numbers, available as toll and toll-free service numbers. Service numbers have higher concurrent call capacity than subscriber numbers and can be assigned to services such as Audio Conferencing, Auto Attendants, or Call Queues.

You will need to decide:

- Which user locations need new phone numbers from Microsoft?
- Which type of telephone number (subscriber or service) do I need?
- How do I port existing phone numbers to Teams?

How you acquire and manage phone numbers differs depending on your PSTN connectivity option.

- For information about managing phone numbers for Calling Plan, see [Manage phone numbers for your organization](manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md).

- For information about managing phone numbers with Operator Connect, see [Set up phone numbers with Operator Connect](operator-connect-configure.md#set-up-phone-numbers).

- For information about managing phone numbers for Direct Routing, see [Configure the phone number and enable enterprise voice and voicemail](direct-routing-enable-users.md#configure-the-phone-number-and-enable-enterprise-voice-and-voicemail-online).


### Call routing and dial plans

How you configure call routing differs depending on your PSTN connectivity option.  

- For Calling Plans, most of call routing is handled by the Microsoft Calling Plan infrastructure. You configure user dial plans for purposes of number translation for call authorization and call routing. For more information, see [What are dial plans?](what-are-dial-plans.md).

- For Operator Connect, most of call routing is managed by the carrier.  You configure user dial plans for purposes of number translation for call authorization and call routing. For more information, see [What are dial plans?](what-are-dial-plans.md).

- For Direct Routing, you must configure call routing by specifying the voice routes and assigning voice routing policies to users. You can configure dial plans for number translation at the trunk level to ensure interoperability with Session Border Controllers (SBCs). For more information, see [Configure voice routing for Direct Routing](direct-routing-voice-routing.md), [Manage voice routing policies](manage-voice-routing-policies.md) and [Translate phone numbers](direct-routing-translate-numbers.md). 


### Location-Based Routing for Direct Routing

In some countries and regions, it's illegal to bypass the PSTN carrier to decrease long-distance calling costs. Location-Based Routing (LBR) for Direct Routing enables you to restrict toll bypass for Teams users based on their geographic location. For more information about how to plan and configure LBR, see the following articles:

- [Plan Location-Based Routing for Direct Routing](location-based-routing-plan.md)
- [Configure network settings for Location-Based Routing](location-based-routing-configure-network-settings.md)
- [Enable Location-Based Routing for Direct Routing](location-based-routing-enable.md)
- [Contoso case study: Location-Based Routing](voice-case-study-location-based-routing.md)<br>
  Describes how a fictional multi-national corporation, Contoso, implemented Location-Based Routing for their organization.


### Emergency calling

How you configure emergency calling differs depending on your PSTN connectivity option.

- For Calling Plan, each user is automatically enabled for emergency calling and is required to have a registered emergency address associated with their assigned telephone number. Dynamic emergency calling (based on the location of the Teams client) is supported.  

- For Operator Connect, each user is automatically enabled for emergency calling and is required to have a registered emergency address associated with their assigned telephone number but can only be set by the carrier partner. Dynamic emergency calling (based on the location of the Teams client) is supported.

- For Direct Routing, you must define emergency calling policies for users by using a Teams emergency call routing policy (TeamsEmergencyCallRoutingPolicy) to define emergency numbers and their associated routing destination. Registered emergency locations are not supported for Direct Routing users. For dynamic emergency calling, additional configuration is required for routing emergency calls and possibly for partner connectivity.

For more information about emergency calling concepts and terminology, and how to configure emergency calling and dynamic emergency calling, see the following articles:

- [Manage emergency calling](what-are-emergency-locations-addresses-and-call-routing.md)
- [Plan and configure dynamic emergency calling](configure-dynamic-emergency-calling.md)
- [Manage emergency calling policies](manage-emergency-calling-policies.md)
- [Manage emergency call routing policies for Direct Routing](manage-emergency-call-routing-policies.md)
- [Contoso case study: Emergency calling](voice-case-study-emergency-calling.md)<br>
  Describes how a fictional multi-national corporation, Contoso, implemented emergency calling for their organization.


### Network topology for voice features

If you are deploying dynamic emergency calling or Location-Based Routing for Direct Routing, you must configure network settings for use with these features in Microsoft Teams. To learn how to configure network settings for network regions, network sites, network subnets, and trusted IP addresses, see the following articles:

- [Network settings for cloud voice features in Microsoft Teams - Concepts and terminology](cloud-voice-network-settings.md)
- [Manage your network topology for cloud voice features in Microsoft Teams](manage-your-network-topology.md)



