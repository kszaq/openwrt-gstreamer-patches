## Package definitions to add current gstreamer + gmrender-resurrect to OpenWRT

Based on [gmediarender-resurrect](https://github.com/hzeller/gmrender-resurrect), [OpenWrt-gmediarender](https://github.com/JiapengLi/OpenWrt-gmediarender/blob/master/README.md) and various patches on the [OpenWRT patch tracker](http://patchwork.openwrt.org/project/openwrt/list/).

## HOW TO

This HOWTO assumes that you already have a configured OpenWRT Buildroot or SDK

If you are compiling for Attitude Adjustment you will need to update glib2, libffi and libsoup to the most recent versions (grab Makefiles and patches from trunk).

Clone this repository into feeds/packages/multimedia folder

	cd openwrt/trunk
	./scripts/feeds update -a
	./scripts/feeds install -a
  
	make menuconfig
	// Select appropriate package

	make package/<package name>/compile V=s
	make package/<package name>/install V=s
	make package/index


The patches for gst1-libav, gst1-plugins-bad and gst1-plugins-ugly are untested and only included for the sake of completeness.

Patches originally made by [alibenpeng](https://github.com/alibenpeng)
[See author's blog](http://testblog.arles-electrique.de)
