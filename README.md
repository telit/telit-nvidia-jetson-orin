# telit-nvidia-jetson-orin
Telit customizations and prebuilt binaries for NVIDIA Jetson Orin

Checkout the branch related to the Jetson Linux version in use, e.g.

```
$ git checkout origin/<branch>
```
e.g.

```
$ git checkout origin/jetson-linux-34.1.1
```
Copy the kernel modules:

```
$ sudo cp lib/modules/<kernel version>/kernel/drivers/usb/class/cdc-wdm.ko /lib/modules/<kernel version>/kernel/drivers/usb/class/
$ sudo cp lib/modules/<kernel version>/kernel/drivers/net/usb/usb/cdc_mbim.ko /lib/modules/<kernel version>/kernel/drivers/net/usb/
```
Regenerate the list of dependencies:

```
$ sudo depmod -a
```
For further instructions refer to Telit document 80455NT11986A
