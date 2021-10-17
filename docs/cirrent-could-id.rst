CIRRENT™ Cloud ID
=========================================

.. topic:: What is CIRRENT™ Cloud ID?

	It is important to ensure that only authentic, authorized devices are allowed to communicate with a Product Company’s cloud environment. Commonly, Product Companies (OEMs) rely on hardware security modules used on the manufacturing line. 

	This process involves time-consuming physical handling of individual chips, and often requires delegating security and trust to a third party – a contract manufacturer. Alternative software solutions exist, but these are vulnerable to security breaches.

	CIRRENT™ Cloud ID is designed to solve many of the device authentication difficulties associated with hardware security modules (HSMs), while avoiding the security risks of software-only alternatives.

	Cloud ID works by extending the silicon-based chain of trust from Product Company devices to the cloud. It does so by acting as a registration intermediary, relying on hardware-based certificates in Cloud ID compatible chips to authenticate devices, subsequently confirming the registration with the Product Cloud.

	By using Cloud ID, Product Companies no longer need to manually handle devices on the manufacturing line to process registration, nor do Product Companies need to risk insecure software solutions.

.. topic:: How Cloud ID works

	Cloud ID works by including a secure, unique, unspoofable device identity on a chip that Product Companies include in their products. Cloud ID-compatible chips have a unique X.509 device certificate built in at Infineon’s manufacturing facility. 

	The nature of the asymmetric cryptography used prevents security compromises because the private key never leaves the device – there is no need for contract manufacturers to access the device certificate, for example. The process that enables a device to gain communications access to your Product Cloud looks as follows:

	1.	Device certificates for Cloud ID compatible devices are pre-populated in CIRRENT™ Cloud ID

	2.	A Product Company staff member alerts CIRRENT™ Cloud ID that a device (or group of devices) should be registered (bound) to the Product Company, and admitted to the Product Cloud. 

	3.	CIRRENT™ Cloud ID uses an API to communicate to your Product Cloud that a device or group of devices have been authorized.

	4.	Your Product Cloud adds the device to its access control list (ACL).

	5.	As the device is now added to your Product Cloud ACL your Product Cloud will allow the device to initiate communications when that device attempts to do so.

	Your Product Cloud can therefore accept data from verified devices and prevent unauthorized or spoofed devices from pumping data into your Product Cloud.

.. topic:: Cloud ID deployment options

	Every manufacturing line is different and to accommodate these needs Cloud ID provides Product Companies with different routes to device registration, each with increasing levels of automation.

	* **Manual Product Cloud registration via Manifest File.** You trigger the registration process for your devices with Cloud ID by scanning a QR code or by entering the Product Group ID in the CIRRENT™ Console. You then download a Manifest File containing the device certificates which you import into your product cloud.

	* **Manual Product Cloud registration via API.** You trigger the registration process for your devices with Cloud ID by scanning a QR code or by entering the Product Group ID in the CIRRENT™ Console. Next, when ready, you trigger an injection of certificates into your Product Cloud using the API link that you configured with CIRRENT™ Cloud ID.

	* **Automatic Product Cloud registration via API.** You trigger the registration process for your devices with Cloud ID by scanning a QR code or by entering the Product Group ID. CIRRENT™ Cloud ID automatically injects the device certifications into your Product Cloud using the default cloud API you configured with CIRRENT™ Cloud ID.

	The different processes allow you to keep just the right level of control across the device onboarding process and allows you to flexibly manage when and where device certificates are injected your Product Cloud.

.. topic:: Key Cloud ID terms

	**Binding**

	Binding is the step where you assign a group of devices in a unique 1-1 relationship to a specific CIRRENT™ Account. This is typically done by scanning a QR-code, but you can also manually add a Product Group ID into the browser UI of the CIRRENT™ web console.

	**Device**

	The Product Company device e.g. washing machine, microwave, connected security device. The device will include a Cloud ID-compatible chip.

	**CIRRENT™ Account**

	A CIRRENT™ Account is a collection of users with roles, devices, configuration profiles. A User may have access to multiple accounts.

	**CIRRENT™ Console**

	This is the web application that allows users to interface to the CIRRENT™ Software Services including CIRRENT™ Cloud ID.

	**Device Certificate**

	A Device Certificate is a unique X.509 certificate that is built into a specific instance of a product.  Examples of these Infineon products that house an Infineon signed cert includes OPTIGA Trust M and PSoC 64.  

	**Registration**

	Registration is the process of adding a group of devices into a CIRRENT™ Account. This is can be done with a QR-code or by manually adding a Product Group ID into the CIRRENT™ web console.

	**Provisioning**

	Is the process of informing your Product Cloud that a particular device should be authorized and how to authenticate the device. This may be done manually outside of the Cloud ID system by uploading a Manifest File, or may be done automatically by the Cloud ID service through a Product Cloud API configuration.  This will add the device to your Product Cloud access control list.

	**Product Cloud API**

	Product Cloud APIs are the API provided by the Cloud Infrastructure company (i.e. Azure, AWS, GCP) or private cloud to interact with Product Company Clouds.  Supported use cases include device provisioning. 

	**Product Company**

	The Product Company (aka OEM – Original Equipment Manufacturer) is the company ultimately responsible for the Device. This would typically be the owners of the brand.  This is not the same role as manufacturer or cloud service provider. 

	**Product Cloud**

	The Product Cloud is the cloud, owned by the Product Company, that the device is supposed to connect to, and it is operated by you, the Product Company, or your delegate.  This may be a private cloud on private or public infrastructure (e.g. AWS or Azure or GCP), or may be an IoT platform (AWS IoT Core, Azure IoT Hub, Arm Pelion, etc).


.. toctree::
   :maxdepth: 2
   :hidden:

   /cid/getting-started-with-cloud-id
   /cid/provisioning-devices-with-cloud-id
