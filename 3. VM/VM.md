Availability Options:
--
* No infrastructure redundancy required: 
-- Means there's no backup setup for your resources. 
-- It's cheaper but may have downtime if something fails, so it's best for testing or non-essential work.

* Availability zone: 
-- An Availability Zone in Azure is a separate location within a region. You get options to select zone.

* Virtual machine scale set:
-- A Virtual Machine Scale Set(Auto Scalling Group) in Azure is a tool that automatically creates and manages a group of identical virtual machines (VMs). 

* Availability set:
-- An Availability Set in Azure keeps your virtual machines (VMs) on different hardware to protect them from failures.
-- This setup helps ensure your VMs stay available if there’s a hardware issue.

Security type: 
--
* Standard:
-- Standard refers to the basic level of security applied to certain resources, like virtual machines.
-- With "Standard" security, Azure provides essential protections, such as secure boot, baseline encryption, and basic access controls, without advanced or additional security features.

* Trusted launch virtual machines:
-- Trusted Launch VMs offer a higher level of security, making them suitable for sensitive workloads and applications requiring strong protection against threats.

* Confidential virtual machines:
-- enhanced level of security by protecting your data and code while in use.
-- Confidential VMs are ideal for workloads that handle sensitive information, such as financial applications, healthcare data, or any situation where privacy and security are paramount.

Architecture Types:
--
ARM64:
Usage: Best for smartphones, tablets, and energy-efficient cloud servers.
x64:
Usage: Common in desktops, laptops, and most server applications.


Azure spot discount:
--
-- No guarentee for resource you use.
-- Might go down any time.

Virtual Machine Types:
--
* B-series: Only for free trail. Learning purpose.
* D-series: General Purpose Aplications.
* E-series: Memory Intense Applications.
* F-series: Compute Intense(multiple processes running).
* H-series: High Performance Applications.
* L-series: Storage Optimised(For DB, where there is a need of storage processing.).
etc...

Enable Hibernation: 
--
-- Setting that allows a computer to save its current state (open applications and documents) to the hard drive and then completely power off. When the computer is turned back on, it can quickly restore everything to how it was before hibernation.

Custom data:
--
* When you want to execute set of commands, when creating vm then use this.

User data:
--
* If you want to store some files or data at particular location inside VM, then use this.

Comparison between RSA and Ed25519 SSH keys:
--
* Security: Ed25519 is very secure even with smaller keys (256-bit), while RSA needs larger keys (2048+ bits) for similar security.
* Speed: Ed25519 is faster and uses less computing power, which is helpful for many SSH connections or limited systems. RSA can be slower, especially with larger keys.
* Size: Ed25519 keys are smaller and quicker to use, while RSA keys are longer and take up more space.
* Compatibility: RSA works almost everywhere, even on older systems. Ed25519 works on most modern systems but might not be supported on some older ones.

General use case:
--
* Use Ed25519 for speed, compact size, and modern security.
* Use RSA if you need the widest compatibility across all systems.

NOTE:
--
* In Azure VM configurations are pre-defined i.e, we can't customise VM's(CPU, memory etc....). Know the requirement and use the machine types.
* VM's come under IAAS.
* Hourly based billing.
* They use Page blob(binary large object) as storage - upto 8tb size.
* If you dont know the type of machie to take then select general purpose machine.
* The entire virtulization platform runs on hyperV.
* Azure VM's are backed by vhd's(virtual hard drives) - We can download vhd's using storage-expower(azure tool), using the downloaded vhd's we can customise or storage back up images and re-upload the VM's.
* 
