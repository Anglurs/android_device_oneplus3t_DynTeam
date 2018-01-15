## TWRP device tree for OnePlus 3T (oneplus3t)

Add to `.repo/local_manifests/oneplus3t.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/oneplus/oneplus3t" name="android_device_oneplus_oneplus3t" remote="TeamWin" revision="android-8.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
make clean
. build/envsetup.sh
lunch omni_oneplus3t-userdebug
make recoveryimage -j16
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_oneplus_msm8996/tree/3T-twrp-8.0
