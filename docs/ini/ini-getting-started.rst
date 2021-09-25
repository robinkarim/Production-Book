﻿Getting started with INI
========================

Getting started with INI is easy, hassle-free and secure. To get started, `register for a free account <https://cirrent.infineon.com/login>`_. Next, integrate the CIRRENT™ Agent on your device, and onboard your device to CIRRENT™ Cloud.

Then, simply sit back and watch the data flow into the CIRRENT™ Console, a secure dashboard that provides deep visibility into the performance of your IoT products both at the fleet level, and at individual device-level.

*************************
Steps to configuring INI
*************************

Interested in testing INI on your device? You need to complete a few steps to configure INI and to start receiving device analytics.

**Note:** before you get started with INI you must have an active CIRRENT™ Cloud account so that you register your device and access CIRRENT™ Console where you will view your device data. You also need a device that is compatible with the CIRRENT™ Agent – you can view the requirements here.

* Register for an account on CIRRENT™ Cloud. 

Registration is free and you can do so via this link. Registering automatically creates a user profile on CIRRENT™ Cloud, and gives you full access to CIRRENT™ Console.

* Install the CIRRENT™ Agent on your device

The instructions to install the CIRRENT Agent depends on the operating system on your device:

* View the general steps for installing the CIRRENT™ Agent on a Linux device here.
* View specific steps to configure CIRRENT™ Agent on Raspberry Pi. 
* View specific steps for configuring CIRRENT™ Agent using ModusToolbox

Please contact us on support@cirrent.com if your device runs RTOS. 

Note: CIRRENT™ Agent is already pre-installed on a select range of INFINEON products, including INFINEON AIROC™ Wi-Fi.

* Onboard your device with CIRRENT™ Cloud

The CIRRENT™ Cloud facilitates device authentication for your single device or fleet of devices. Every device that sends INI data to the CIRRENT™ Cloud must first complete an onboarding process. See the next section for more details about onboarding.


* Reviewing your analytics on CIRRENT™ Console

Once data starts steaming in from CIRRENT™ Agent you will be able to review a range of analytics across all your devices, and drill down into device specific analytics. You can read more about the CIRRENT™ Console here.
 
*******************************************
Onboarding devices into the CIRRENT™ Cloud
*******************************************

Before your device can start to send data to the CIRRENT™ Cloud it must first authenticate itself with the CIRRENT™ Cloud through an onboarding process. You onboard your devices to CIRRENT™ Cloud in one of three ways:

* During manufacturing you pre-flash temporary device credentials to your device which your device uses when contacting the CIRRENT™ Cloud to request onboarding and a device ID

* You onboard your devices one by one or in bulk via the OPS API

* You onboard devices one by one using the CIRRENT™ Wi-Fi onboarding app

* Onboarding is pre-integrated with your INFINEON chip

*******************************************
Using the CIRRENT™ Wi-Fi onboarding app
*******************************************

Central to the CIRRENT™ offering is the ability to efficiently perform Wi-Fi onboarding in IoT devices. CIRRENT™ offers an Android and iOS app that helps you to test Wi-Fi onboarding for your device. Choose from either BLE (Bluetooth Low Energy) onboarding, or onboarding via Soft AP.

Both CIRRENT™ Wi-Fi onboarding apps also enable you to easily register a single device with the CIRRENT™ Cloud so that you can analyze the analytics on your device.

To access the Android CIRRENT™ Wi-Fi onboarding app, simply scan the code below:

.. image:: ../img/androidqr.png
    :align: center
    :alt: Dashboard 2
 
For the iOS edition of the app, scan the following code:

.. image:: ../img/iphoneqr.png
    :align: center
    :alt: Dashboard 2
 
If using the iOS you can make use of the in-app walkthrough to smooth the onboarding process.

*******************************************
Using the OPS API to register devices
*******************************************

The OPS API is used for bulk provisioning of devices during your manufacturing process. The API is described in detail `here <https://app.swaggerhub.com/apis/Cirrent/api-ops/1.0.0-oas3>`_. You can use Authorize button on the top right corner of the SwaggerHub page and then click "Try it out" for each API call to check the payload and responses.

You can use any one of the two options below for BasicAuth with this API:

1.	Use Username and Password associated with CIRRENT™ account
2.	Use OPS API Key and Secret generated from CIRRENT™ console

To generate OPS API Key and Secret, please go to the `API Key Management page <https://go.cirrent.com/management/api-key>`_ in the CIRRENT™ Console. Select Key Type as "OPS", enter a name for the key and click "Add". The CIRRENT™ Console will generate OPS API Key and Secret.