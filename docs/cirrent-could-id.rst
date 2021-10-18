CIRRENT™ Cloud ID
=========================================

.. topic:: What is CIRRENT™ Cloud ID?

	Only authentic, authorized devices should be allowed to communicate with a Product Company’s cloud environment. Product Companies (OEMs) commonly rely on hardware security modules used on the manufacturing line to ensure only authentic devices are admitted to the Product Cloud. This process involves time-consuming physical handling of individual chips, and often requires delegating security and trust to a third party – a contract manufacturer. Alternative software solutions exist, but these are vulnerable to security breaches.

	CIRRENT™ Cloud ID is designed to solve many of the device authentication difficulties associated with hardware security modules (HSMs), while avoiding the security risks of software-only alternatives. Cloud ID works by extending the silicon-based chain of trust from Product Company devices to the cloud. It does so by acting as a registration intermediary, relying on hardware-based certificates in Cloud ID compatible chips to authenticate devices, subsequently facilitating provisioning of authorized devices with the Product Cloud.

	Thanks to Cloud ID, Product Companies no longer need to manually handle devices on the manufacturing line to process registration, nor do Product Companies need to risk insecure software solutions..

.. topic:: How Cloud ID works

	Cloud ID works by including a secure, unique, unspoofable device identity on a chip that Product Companies install in their products. Cloud ID-compatible chips have a unique X.509 device certificate built in at Infineon’s manufacturing facility. 

	The nature of the asymmetric cryptography used prevents security compromises because the private key never leaves the device – there is no need for contract manufacturers to access the device certificate, for example. The process that enables a device to gain communications access to your Product Cloud looks as follows:

	1.	Device certificates for Cloud ID compatible devices are pre-populated in CIRRENT™ Cloud ID.

	2.	A Product Company designated or authorized representative binds that device or batch of devices with CIRRENT™ Cloud ID. 

	3.	CIRRENT™ Cloud ID uses an API to communicate to your Product Cloud that a device or batch of devices have been authorized to connect with the Product Cloud.

	4.	Your Product Cloud adds the device to its access control list (ACL).

	5.	As the device is now added to your Product Cloud ACL your Product Cloud will allow the device to initiate communications when that device attempts to do so – when the end-user switches it on, for example.

	Your Product Cloud can therefore securely accept data from verified devices and prevent unauthorized or spoofed devices from pumping data into your Product Cloud.

.. topic:: Cloud ID deployment options

	Every manufacturing line is different and to accommodate these needs Cloud ID provides Product Companies with different routes to device provisioning, each with increasing levels of automation.

	* **Manual Product Cloud provisioning via Manifest File.** You start the provisioning process by binding the devices to your Cloud ID account – either by scanning a QR code or by entering the Product Batch ID in the CIRRENT™ Console. You then download a Manifest File containing the device certificates which you import into your Product Cloud to complete the provisioning step.

	* **Manual Product Cloud provisioning via API.** You start the provisioning process by binding the devices to your Cloud ID account – either by scanning a QR code or by entering the Product Batch ID in the CIRRENT™ Console. Next, when ready, you trigger an injection of certificates into your Product Cloud using the API link that you configured with CIRRENT™ Cloud ID., and this completes the provisioning step.

	* **Automatic Product Cloud provisioning via API** You start the provisioning process by binding the devices to your Cloud ID account – either by scanning a QR code or by entering the Product Batch ID in the CIRRENT™ Console. CIRRENT™ Cloud ID automatically injects the device certifications into your Product Cloud using the default cloud API you configured with CIRRENT™ Cloud ID, thereby completing provisioning automatically.

	The different processes allow you to keep just the right level of control across the device onboarding process and allows you to flexibly manage when and where device certificates are injected into your Product Cloud.

.. topic:: Key Cloud ID terms

	**Binding**

	Binding is the step where you assign a batch of devices to a specific CIRRENT™ Account. This is typically done by scanning a QR-code, but you can also manually add a Product Batch ID into the browser UI of the CIRRENT™ web console.

	**Device**

	The Product Company device e.g. washing machine, microwave, connected security device. The device will include a Cloud ID-compatible chip.

	**CIRRENT™ Account**

	A CIRRENT™ Account is a collection of users with roles, devices, configuration profiles. A user may have access to multiple accounts.

	**CIRRENT™ Console**

	This is the web application that allows users to interface with CIRRENT™ software services including CIRRENT™ Cloud ID.

	**Device Certificate**

	A Device Certificate is a unique X.509 certificate that is built into a specific instance of a product.  Examples of these are Infineon products that house an Infineon signed certificate.  

	**Registration**

	Registration is the process of adding a group of devices into a CIRRENT™ Account. This is can be done with a QR-code or by manually adding a Product Group ID into the CIRRENT™ web console.

	**Provisioning**

	Provisioning is the process of informing your Product Cloud that a particular device should be authorized and how to authenticate the device. This may be done manually outside of the Cloud ID system by uploading a Manifest File, or may be done automatically by the Cloud ID service through a Product Cloud API configuration. This will add the device to your Product Cloud access control list. Note that the provisioning step involves no changes on the physical device.

	**Product Cloud API**

	Product Cloud APIs are the API provided by the Cloud Infrastructure company (i.e. Azure, AWS) or private cloud to interact with Product Company Clouds.  Supported use cases include device provisioning. 

	**Product Company**

	The Product Company (aka OEM – Original Equipment Manufacturer) is the company ultimately responsible for the Device. This would typically be the owners of the brand.  This is not the same role as the manufacturer or cloud service provider. 

	**Product Cloud**

	The Product Cloud is the cloud, owned by the Product Company, that the device is supposed to connect to, and it is operated by you, the Product Company, or your delegate.  This may be a private cloud on private or public infrastructure (e.g. AWS or Azure), or may be an IoT platform (AWS IoT Core, Azure IoT Hub, etc.).


.. toctree::
   :maxdepth: 2
   :hidden:

   /cid/getting-started-with-cloud-id
   /cid/provisioning-devices-with-cloud-id
   /cid/cirrent-console-for-cloud-id
   /cid/quick-start-cloud-id-virtual-dev-kit
