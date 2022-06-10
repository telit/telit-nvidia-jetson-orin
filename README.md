# telit-nvidia-jetson-orin
Telit customizations and prebuilt binaries for NVIDIA Jetson Orin

Copy the kernel modules:

```
$ sudo cp lib/modules/5.10.65-tegra/kernel/drivers/usb/class/cdc-wdm.ko /lib/modules/5.10.65-tegra/kernel/drivers/usb/class/
$ sudo cp lib/modules/5.10.65-tegra/kernel/drivers/net/usb/usb/cdc_mbim.ko /lib/modules/5.10.65-tegra/kernel/drivers/net/usb/
```
Regenerate the list of dependencies:

```
$ sudo depmod -a
```
For further instructions refer to Telit document 80455NT11986A
