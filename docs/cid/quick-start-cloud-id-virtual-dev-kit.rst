Quick Start: Cloud ID Virtual Dev Kit
======================================

**note this is currently the older version of the developer kit - will be replaced shortly**

Do you want to take Cloud ID for a test run? This set of instruction will help you get up and running with Cloud ID and show you just how easy it is to provision your devices with Cloud ID.

To start, first register an account with Infineon’s CIRRENT™ division. You can do so by visiting https://cirrent.infineon.com/. Simply select **Create a new account**, and follow the steps to complete the account creation process. You can then log in using your new credentials, which will present you with this screen:

.. image:: ../img/qs-1.png
    :align: center
    :alt: Dashboard 2

For your next steps, you need to decide whether you want to test Cloud ID by using a Manifest File to inject device certificates into your Product Cloud, or whether you want to set up an API link to your Product Cloud.

Using Manifest Files
*********************

You can provision devices in your Product Cloud by registering the devices with Cloud ID, and then generating a Manifest File with device certificates which you upload into your Product Cloud.

**Binding ownership in CIRRENT™ Cloud ID**

Your Cloud ID-compatible devices comes pre-installed with a device certificate. To bind ownership with these devices you need to add the devices to CIRRENT™ Cloud ID by entering group product ID for the group of devices into the Cloud ID section in the CIRRENT™ Console.

Don’t have any Cloud ID devices on hand? Not to worry, we’ll provide you with a sample Product Group ID and QR code below.

To start the process navigate to **Device Management** and to **Cloud ID**. The default Cloud ID panel displays the groups of devices you have already onboarded. To add a new group of devices click on the **Add Infineon Devices** button.

.. image:: ../img/qs-2.png
    :align: center
    :alt: Dashboard 2

Next, you’ll see the following screen:

.. image:: ../img/qs-3.png
    :align: center
    :alt: Dashboard 2
 

In the Product Group ID field you enter the GUID associated with the devices you want to bind ownership to. This could be a reel of chips, for example, such as the unique alpha-numeric string found in your OPTIGA Reel. 

.. note:: If you have don’t have access to a Cloud ID compatible chip you can use one of the dummy reels to test functionality – including <demo-reel-1> , <demo-reel- 2>, 3, …,  up to 10.

You can enter the GUID manually, by copying and pasting the GUID, or by using a barcode scanner attached to your PC. Here is a sample QR code:

<image of QR Code>

Because you will be downloading the Manifest File to manually upload it to your Product Cloud you need to leave the Product Cloud API field blank. Simply click Add to complete the binding process.

You should now see the group of devices listed in your list of Infineon devices:

.. image:: ../img/qs-4.png
    :align: center
    :alt: Dashboard 2

You will see a counter reflecting the number of registered devices, indicating the number of devices contained in that Group Product ID.

**Downloading the Manifest File in CIRRENT™ Console**

Now that you have bound your devices in CIRRENT™ Cloud ID you can proceed to download the Manifest File containing the device certificates. To do so, click on the download button next to the entry for the list of device you’d like to import into your Product Cloud:

.. image:: ../img/qs-5.png
    :align: center
    :alt: Dashboard 2

Clicking the download button will automatically trigger the download of an .csv file. This csv file contains three data fields:

* **device_id:** containing the unique device ID for an individual device
* **group_id:** the Group Product ID the device is associated with
* **certificate:** the full device security certificate

As a final step, you need to ingest the .csv Manifest File into your product cloud by using an import tool appropriate for your environment.

Using an API
*************

In the previous section we described how you can use a Manifest File to extract device certificates, which you needed to your Product Cloud to complete onboarding.

In this section we outline how you can use an API that connects to your cloud service - including AWS, Azure, or your custom cloud – to inject device certificates into your Product Cloud when you bind a group of devices to your Cloud ID account. 

**Configuring a cloud API**

In order to provision devices using an API you need to first set up a link to your Product Cloud by configuring a cloud API in CIRRENT™ Console.

To configure your first cloud API with Cloud ID, navigate to **Device Management** and **Cloud ID**. Select the **Product Cloud APIs** tab, and click on **Add Cloud API**. You’ll be presented with a dialog box where you need to complete your Product Cloud API details.

.. image:: ../img/qs-6.png
    :align: center
    :alt: Dashboard 2
 

* **Name:** This is the name of your Product Cloud that will appear in CIRRENT™ Cloud ID. This name will help you identify which Product Cloud you are provisioning a device into when you set up automated provisioning – or when you manually provision a device.

* **Type:** To speed up configuration, choose the relevant cloud service you are configuring – including Azure, AWS or your private cloud.

* **Credentials:** The username and password combination that you have set up to allow CIRRENT™ Cloud ID to communicate with your product cloud. Simply enter the combination as username:password, for example: johndoe:abcxyz123

* **URL:** this is the web address of your Product Cloud.

You have now added your Product Cloud to CIRRENT™ Cloud ID and can now provision devices registered with Cloud ID directly into your product cloud.

**Manually provisioning devices into your Cloud API**

Once you’ve set up your Product Cloud within Cloud ID you can now proceed to provision devices. First, you need to bind ownership of the devices with CIRRENT™ Cloud ID. Your Cloud ID-compatible devices comes pre-installed with a device certificate. To bind ownership with these devices you need to add the devices to CIRRENT™ Cloud ID by entering group product ID for the group of devices into the Cloud ID section in the CIRRENT™ Console.

To do so, navigate to Device Management and to Cloud ID. The default Cloud ID panel displays the groups of devices you have already onboarded. To add a new group of devices click on the Add Infineon Devices button.

.. image:: ../img/qs-7.png
    :align: center
    :alt: Dashboard 2

Next, you’ll see the following screen:

.. image:: ../img/qs-8.png
    :align: center
    :alt: Dashboard 2


In the Product Group ID field you enter the GUID associated with the devices you want to bind ownership to. This could be a reel of chips, for example, such as the unique alpha-numeric string found in your OPTIGA Reel. 

.. note:: If you have don’t have access to a Cloud ID compatible chip you can use one of the dummy reels to test functionality – including <demo-reel-1> , <demo-reel- 2>, 3, …,  up to 10.

You can enter the GUID manually, by copying and pasting the GUID, or by using a barcode scanner attached to your PC. Here is a sample QR code:

<image of QR Code>

Next, you need to specify the Product Cloud API into which you would like to provision the devices. Simply click Add to complete the binding process.

You should now see the group of devices listed in your list of Infineon devices:

.. image:: ../img/qs-9.png
    :align: center
    :alt: Dashboard 2

You will see a counter reflecting the number of registered devices, indicating the number of devices contained in that Group Product ID.

**Triggering a distinct API provisioning step**

You also have the option inject device certificates for a group of devices into your Product Cloud of choice by triggering a specific API provisioning step. You can trigger this step as many times as needed in order to provision devices into as many Product Clouds as required.

To do so, navigate to **Device Management** and to **Cloud ID**. Select the Infineon Devices tab. Next, click the provisioning button 

.. image:: ../img/qs-10.png
    :align: center
    :alt: Dashboard 2

to open the provisioning dialog box. 

Next, simply select the Product Cloud API you’d like to inject the device certificates into, and click **Provision Now**. 

.. image:: ../img/qs-11.png
    :align: center
    :alt: Dashboard 2
