FOSTools is a Linux tool that can convert Android images into FireFox OS images. A prebuilt FOS binary package is released out.

Beta Release is placed at http://fosmaker.googlecode.com/files/fostools_beta_1.tgz



Usage:
  * ./fostools/maker.sh -t typename foo.zip
    * typically foo.zip include boot.img,system and META-INF folders
    * a define file at ./fostools/type/typename, see ./fostools/type/onex for example
  * ./fostools/maker.sh foofolder
    * foofolder shall include boot.img system.img
will gen a fosmaker\_out.zip under current dir
# onex #

  * ecovery img use recovery-clockwork-5.8.4.0-endeavoru.img (check http://wiki.cyanogenmod.org/w/Install_CM_for_endeavoru)
  * m-9-20121014-NIGHTLY-endeavoru.zip (http://mirrors.reflected.net/pub/get.cm/jenkins/10144/ or else )
./fostools/maker.sh -t onex cm-9-20121014-NIGHTLY-endeavoru.zip

c9c2952255d5e6498224935099a01434  cm-9-20121014-NIGHTLY-endeavoru.zip

ab78a70005cc5d925de1a7de0c0a6af0  recovery-clockwork-5.8.4.0-endeavoru.img

  * ![http://fosmaker.googlecode.com/files/htconex_fos_thumb.jpg](http://fosmaker.googlecode.com/files/htconex_fos_thumb.jpg)
# toro #

  * https://developers.google.com/android/nexus/images#mysidimm76k (extract boot.img and system.img and put to ./toro-google )

./fostools/maker.sh ./toro-google



## only 4.0 ( ics ) support ##
Fos only support android 4.0x , don't waster your time with 4.1 or higher img

  * if only 4.2 bsp on hand, porting it back to 4.0 is a way can go (like I met)