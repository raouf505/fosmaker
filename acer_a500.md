# Introduction #

run fos on acer a500 tablet which is tegra2 based, without neon support.


# Details #
  * bootloader and recovery use V8-UNL-ICS-HC-bootloader-MULTI-cwm
    * http://forum.xda-developers.com/showthread.php?t=1622425

16748b01a102497b0f64741b5981b298  bootloader\_v8.bin

48839df15d40733689fa82bc894cc08b  recovery\_thor17\_403.img
  * cm-9-20120708-UNOFFICIAL-a500.zip (http://forum.xda-developers.com/showthread.php?t=1597102)

  * download fosmaker (http://fosmaker.googlecode.com/files/fostools_beta_1.tgz)
  * create type file  (type/a500)
```
#600M
SYSTEMSIZE=629145600
SYSPARTITION=/dev/block/mmcblk0p3
BOOTPARTITION=/dev/block/mmcblk0p2
#list to rm
SYSRM="
/system/lib/hw/hwcomposer.tegra.so
"
```

  * replace the fos\_bin folder with fos\_bin\_a6df3ea6\_noneon.zip (http://fosmaker.googlecode.com/files/fos_bin_a6df3ea6_noneon.zip)
    * default fos\_bin at the tools is neno enable

  * ./fostools/maker.sh -t a500 a500/cm-9-20120708-UNOFFICIAL-a500.zip (get ota zip : fosmaker\_out.zip )