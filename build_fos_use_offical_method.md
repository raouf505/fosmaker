
```

build fos use offical method: (need network connection)
	target: galaxy-nexus (magro)
	(toro can run too, with 3G fail)
	

extra debpkg:
	autoconf2.13
	ccache

git clone git://github.com/mozilla-b2g/B2G.git
cd B2G
./config.sh galaxy-nexus
./build.sh

#install
TOP=`pwd`
OUT=$TOP/out/target/product/maguro
fastboot flash boot $OUT/boot.img
fastboot flash system $OUT/system.img
fastboot flash userdata $OUT/userdata.img

```