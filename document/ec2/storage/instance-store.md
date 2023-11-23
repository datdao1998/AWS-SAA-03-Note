An **instance store** provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. 

Instance store is ideal for :
* Temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content
* It can also be used to store temporary data that you replicate across a fleet of instances, such as a load-balanced pool of web servers.

# Instance store volume and data lifetime
* Instance store volumes are attached only at instance launch. You can't attach instance store volumes after launch. You can’t detach an instance store volume from one instance and attach it to a different instance.
* An instance store volume exists only during the lifetime of the instance to which it is attached. You can’t configure an instance store volume to persist beyond the lifetime of its associated instance.
* The data on an instance store volume persists even if the instance is rebooted. However, the data does not persist if the instance is stopped, hibernated, or terminated. When the instance is stopped, hibernated, or terminated, every block of the instance store volume is cryptographically erased.
* If you create an AMI from an instance, the data on its instance store volumes isn't preserved and isn't present on the instance store volumes of the instances that you launch from the AMI.
