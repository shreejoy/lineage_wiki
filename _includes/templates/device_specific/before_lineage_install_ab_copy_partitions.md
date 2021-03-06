## Pre-install instructions

Thanks to some OEMs shipping A/B devices with slot `b` unpopulated, we need to populate it by copying the contents of slot `a` to avoid a potential hard-brick.

To do this, sideload the copy-partitions.zip package by doing the following:
1. Download the copy-partition zip file from [here](https://androidfilehost.com/?fid=4349826312261678890).
{% if device.uses_lineage_recovery %}
2. Sideload the copy-partitions `.zip` package:
    * On the device, select "Apply Update", then "Apply from ADB" to begin sideload.
    * On the host machine, sideload the package using: `adb sideload filename.zip`
{% else %}
2. Sideload the copy-partitions `.zip` package:
    * On the device, select "Advanced", "ADB Sideload", then swipe to begin sideload.
    * On the host machine, sideload the package using: `adb sideload filename.zip`
{% endif %}