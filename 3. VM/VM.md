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
