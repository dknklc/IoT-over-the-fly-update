
# Over-The-Air Software Updates for IoT Devices

### 1. Mender
Mender is a free open source end-to-end over-the-air software update manager with a client-server architecture. Whether the need is to install the latest security patch, delight customers with new features, or fix bugs - every company must be able to deploy overthe-air (OTA) software updates to their fleet of devices.

Mender provides a complete over-the-air update infrastructure for developers and support teams. Whether in the field or the factory, remotely and easily manage device software without the need for manual labor.It also provides:

- Update without the risk of bricking devices.
- Robust in the face of limited bandwidth, unstable connectivity or power loss.
- Advanced scheduling for safe deployment to large device fleets.
- Secure and verified to standards, at every step.

Mender supports 2 methods for updating a connected device: __system updates__ and __applications updates__. 
- In system updates, the entire disk partition on a device is updated and provide the benefit of a secure and robust updates at the cost of file size, bandwidth, speed and memory footprint. 
 - In application updates only certain parts of software on the disk is updated which enable targeted application-level updates, which can be just a few kilobytes in size for much lower bandwidth usage, faster updates, and more frequent deployments.
 ### Standard Features
- Out-of-the-box support for updates such   as applications, packages, containers, files,  and proxy deployment of attached  peripherals
- Support for Yocto Debian, Ubuntu and  Raspbian OSes.
- Dual A/B root filesystem updates with  rootfs compression to save bandwidth
- Scripting support for custom actions (e.g.  checks after the update is installed)
- eMMC, SD card, and raw NAND/NOR flash  support
- Standalone deployments (no server)
- One mechanism to update your  applications and kernel
- Device groupings for controlled rollouts

### Operating System & Board Support
Mender currently supports Linux-based embedded devices with a fast-growing number of boards and operating systems. Mender Hub is the only online open source community dedicated to enabling OTA software updates on any hardware platform and operating system. Mender’s consulting services has deep expertise for all size projects, specializing in the rapid implementation of OTA update management. Mender also provides consulting for more generic embedded devices, including system design architecture and recommendations.

### Compatibility
- Mender as Debian package: Mender is easy to install and use for application-based updates, with support for ARMv6 and Debian family OSes e.g. Debian, Ubuntu and Raspbian
- Raspberry Pi reference integration:
   Mender is fully integrated for system and application-level updates with a ready-to-flash Raspbian image


### Links

- [@menderio](https://mender.io/product/features) about open-source, basic, professional (robust delta updates) and enterprise packages

- [@howitworks](https://mender.io/how-it-works) about its working

- [@docs](https://docs.mender.io/) its documentation
  
  
### 2. RAUC
RAUC is a lightweight update client that runs on your Embedded Linux device and reliably controls the procedure of updating your device with a new firmware revision. RAUC is also the tool on your host system that lets you create, inspect and modify update artifacts for your device.

RAUC is free and open-source software. It is released under the GNU General Public License (GPL) version 2. This means that you have the freedom to use, modify, and distribute RAUC according to the terms of the license.

From a top view, the RAUC update framework provides a solution for four basic tasks:

- generating update artifacts
- signing and verification of update artifacts
- robust installation handling
- interfacing with the boot process

RAUC is basically an image-based updater, i.e. it installs file images on devices or partitions. But, for target devices that can have a file system, it also supports installing contents from tar archives. This often provides much more flexibility as a tar does not have to fit a specific partition size or type. RAUC ensures that the target file system will be set up correctly before unpacking the archive.

### Compatability

As long as your ARM-based device is supported by the Debian-based operating system you are using and meets the system requirements for RAUC, you should be able to integrate and utilize RAUC for managing software updates on your ARM-based system.

RAUC (Robust Auto Update Controller) is compatible with Raspberry Pi and Debian-based operating systems. RAUC is a software update framework designed for embedded systems, and it supports various hardware platforms, including Raspberry Pi.


### Links

- [@raucio](https://rauc.io/) official website

- [@docs](https://rauc.readthedocs.io/en/latest/index.html)  its documentation

### 3. SWUpdate

SWUpdate is the the framework for you to update your device locally or remotely. Thanks to its high flexibility, you can tune any aspect of the update and integrate it into your project. SWUpdate does not set any special requirement and it can be integrated in any embedded Linux project. It does not matter if you want to update from a local USB stick, or via a Webserver, or via a fleet management – SWUpdate will fit your needs.

SWUpdate is a framework and this guarantees the highest flexibility, but it requires a learning curve to be integrated into an existing or new project.Thus, they offer Online Training (1 day) about SWUpdate and its integration on Embedded Linux projects.


 ### Standard Features
 - __Update everything:__ SWUpdate is able to update all components of your device: __Bootloader__, __Linux Kernel__, __Root filesystem__, __Application__

 - __Full and Incremental Update:__ SWUpdate can update the whole device or can update single files, and since 2021.11 supports incremental update of binary images. SWUpdate works autonomously and you can put your update package where you want, and SWUpdate is able to compute the differences to the running software before downloading. You have still full control, and you can reduce the required bandwidth without losing reliability.
 - __100% Open Source__: SWUpdate is 100% Open Source

 - __Security__: SWUpdate is developed with security in mind to avoid that not authorized software can run on your device.
 - __Customizable__: SWUpdate is developed with security in mind to avoid that not authorized software can run on your device.
 - __Many use cases__: You will update from a USB stick, or you need a fleet management systems – SWUpdate provides the right solution for you !
 - __Reduce recall costs:__ SWUpdate provides safe updates and help you to drastically reduce the need to recall devices from fields.

 SWUpdate can provide ad-hoc updates for each step of the life of your device, from the early development as part of BSP  to large scale rollouts in field.

 


### 4. SWUPD
Swupd is an OS-level software update program that applies updates 
to a __Clear Linux OS__ which is a Linux distribution developed by Intel.

Swupd has two main functions.

    1. Manage software and replace APT or YUM, by installing bundles rather than package.
    2. Check for system updates and install them.

__Bundles__ contain everything needed to deliver a software capability. They are the smallest granularity component that is managed by Clear Linux OS. A bundle comes with all of its dependencies rather than downloading a cascade of package dependencies when installing a piece of software.

### Updating

Clear Linux OS enforces regular updating of the OS by default and automatically checks for updates against a version server. The content server provides the file and metadata content for all versions and can be the same as the version server. The content url server provides metadata in the form of manifests, which list and describe file contents, symlinks, and directories. Additionally, the actual content is provided to clients in the form of archive files.

Software updates with Clear Linux OS are also efficient. Unlike package-based distributions, swupd only updates files that have changed, rather than entire packages. For example, it is quite common for an OS security patch to be as small as 15 KB. Using binary deltas, Clear Linux OS is able to apply only what is needed

### How it works
#### Prerequisites

- The device is on a well-connected network.
- The device is able to connect to an update server. The default server is: https://cdn.download.clearlinux.org/update/

#### Updates

Clear Linux OS updates are automatic by default, but can be set to occur only on demand. swupd makes sure that regular updates are simple and secure. It can also check the validity of currently installed files and software, and can correct any problems.

### 5. UpdateHub

UpdateHub is an enterprise-grade solution which makes simple to remotely update all your Linux-based devices in the field, with maximum security and efficiency, while you focus in adding value to your product.

It handles all aspects related to sending Firmware Over-the-Air (FOTA) updates with maximum security and efficiency, making your project the center of your attention.



### Features
- HTTP API to control the system remotely
- Single and team managed products
- Atomic Updates: A failure occurring during update package installation process must not brick your device or let it inconsistent state.
- Secure TLS communication: All network communication with UpdateHub is encrypted to ensure the confidentiality of all data sent and received.

__Note:__ TLS is a widely adopted security protocol designed to facilitate privacy and data security for communications over the Internet. A primary use case of TLS is encrypting the communication between web applications and servers, such as web browsers loading a website.

- Integrity checksum: Update package integrity is always verified on device to avoid corruption during file transfer over a network.

- Package signing: Update package authenticity is validated using cryptographic signatures before it is installed on device.

There are two options for pricing your business:

__1.Free:__ Up to 5 Devices, Up to 1 GB Bandwidth, Up to 1 GB Storage.

__2.METERED BILLING:__ Starting at $10 / month, and the pricing changes with respect to the number of devices and etc.

### Compatability
The support provided by the UpdateHub for the device includes:

- Support for multiple Yocto Project™ and Zephyr Project™ versions
- Bootloader upgrade support (U-Boot and GRUB)
- Flash support (NAND, NOR)
- UBIFS support
- Update package signature validation for security
- Automated rollback in case of update fail
- Conditional installation (content, version, and custom pattern support)
- Callback support for every update step
- HTTP API to control and inquiry the local agent

### Links

- [@doc](https://docs.updatehub.io) about its documentation
- [@pricing](https://updatehub.io/pricing/#pricing) about its pricing



### 6. Balena

The secure container-based technology stack that enables you to develop, deploy, manage, and scale fleets of IoT Linux devices.

#### Features
- __Updating:__ Robust and resilient updates for your fleet, managed remotely using the balenaCloud dashboard
- __Monitoring:__ View the status and monitor deployments across your fleet in the balenaCloud Dashboard.
- __Maintaining:__ Diagnose, debug and resolve issues at the individual device level with a SSH connection for each device

### Compatability

- Types of devices supported, from Raspberry Pi to x86 to Jetson Orin
- Single-board computers (SBCs): Balena supports popular SBCs such as Raspberry Pi (all models), NVIDIA Jetson Nano, Intel NUC, BeagleBone, Odroid, and others.
- x86-based hardware: Balena supports x86-based devices, which include desktop PCs, laptops, servers, and virtual machines. It allows running containerized applications on a wide range of x86 hardware.
- Arm-based devices: Balena is compatible with Arm-based devices, including Arm-based servers, mini PCs, and embedded devices. This includes devices utilizing Armv7 and Armv8 architectures.

### Links

- [@docs](https://docs.balena.io/learn/welcome/introduction/) its documentation
### 7. Snap

Snap IoT OTA is a way to deliver **secure and reliable** software updates to Linux devices using **snaps**, which are **application containers** with all their dependencies. Snaps can be installed using a single command on any device running Linux, and they run fully isolated in their own sandbox. Snaps are hosted in the global **Snap Store**, an application repository hosted and managed by Canonical, and are free for anyone to download. Snap IoT OTA is in use right now by many companies and developers who want to create, publish and distribute software on one platform, with **automatic and resilient** over-the-air updates to only their devices in a **secure and validated** way. You can find out more about Snap IoT OTA and how to get your own IoT app store here.

#### Compatibility

- Is snap store compatible with arm based controller beaglebone?

  - Yes, snap store is compatible with arm based controller beaglebone. You can install snap store on Ubuntu using the snap store snap. Snaps are compatible across architectures, so you can run the same snap on any device running Linux, including beaglebone. You can also find snaps for beaglebone on the snap store website.

- Is it compatible with debian distribution?

  - Yes, snap store is also compatible with debian distribution. You can install snap store on debian using the snapd command line package manager, which is available through the system repositories. You can follow the detailed installation instructions here.


### Links

- [@Snap](https://ubuntu.com/core/services/guide/snap-store-vs-iot-app-store) about snap store and IoT app store 

## How had Android overcome over-the-air updates?
 
### A/B (Sorunsuz) sistem güncellemeleri

A/B sistem güncellemeleri, yuvalar (normalde yuva A ve yuva B) olarak anılan iki grup bölüm kullanır. Kullanılmayan yuvadaki bölümlere normal çalışma sırasında çalışan sistem tarafından erişilmezken sistem mevcut yuvadan çalışır. Bu yaklaşım, kullanılmayan yuvayı yedek olarak tutarak güncellemeleri hataya dayanıklı hale getirir: Bir güncelleme sırasında veya hemen sonrasında bir hata meydana gelirse, sistem eski yuvaya geri dönebilir ve çalışan bir sisteme sahip olmaya devam edebilir. Bu amaca ulaşmak için, geçerli yuva tarafından kullanılan hiçbir bölüm OTA güncellemesinin bir parçası olarak güncellenmemelidir (yalnızca bir kopyası olan bölümler dahil).

Her yuvanın, yuvanın aygıtın önyükleme yapabileceği doğru bir sistem içerip içermediğini belirten önyüklenebilir bir özniteliği vardır. Geçerli yuva, sistem çalışırken önyüklenebilir, ancak diğer yuvada sistemin eski (hâlâ doğru) bir sürümü, daha yeni bir sürümü veya geçersiz veriler olabilir. Geçerli yuva ne olursa olsun, etkin yuva (önyükleyicinin bir sonraki önyüklemede önyükleme yapacağı yuva) veya tercih edilen yuva olan bir yuva vardır.

Her yuva, kullanıcı alanı tarafından ayarlanan başarılı bir özniteliğe de sahiptir; bu, yalnızca yuva aynı zamanda önyüklenebilir ise geçerlidir. Başarılı bir yuva kendini başlatabilmeli, çalıştırabilmeli ve güncelleyebilmelidir. Başarılı olarak işaretlenmemiş bir önyüklenebilir yuva (buradan önyükleme yapmak için birkaç deneme yapıldıktan sonra), aktif yuvanın başka bir önyüklenebilir yuvaya (normalde önyükleme girişiminden hemen önce çalışan yuvaya) değiştirilmesi de dahil olmak üzere, önyükleyici tarafından önyüklenebilir olarak işaretlenmelidir. yeni, aktif olana). Arayüzün belirli ayrıntıları boot_control.h dosyasında tanımlanmıştır.


### Links

- [@android](https://source.android.com/docs/core/ota/ab?hl=tr#slotss) A/B sistem güncellemeleri hakkında

