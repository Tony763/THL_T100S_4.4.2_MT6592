# THL_T100S_4.4.2_MT6592

#Content is licenced to Mediatek, but they aren't using a Android Source Code in law by it's license.
#If there will be a problem with this, Please send me a message and I will remove this content.
#If you can, let us make this excelent phone even better. Tnank you

Prerequirest:
*       OS                         : Linux distribution Ubuntu 10.04
*       Memory Size                : 4G or above
*       make                       : GNU Make 3.81 or 3.82
*       perl                       : Version 5.10.X
*       python                     : Version 2.6.X
*       arm-linux-androideabi-gcc  : Version 4.6.X
*       gcc                        : Version 4.4.3
*       jdk                        : Version 1.6.X - Oracle Java Development Kit 6u45
*       bison                      : Version 2.4.X
*       flex                       : Version 2.5.X
*       gperf                      : Version 3.0.X
*       mingw                      : Installed
*       unix2dos/tofrodos          : Installed
*       tee                        : Installed
Im running it in Oracle VirtualBox.


It is too big for github so I use a Mega.co.nz for storing files.

1) Download all from https://mega.co.nz/#F!FUJSQC7Z!c9vp0UpprSLjllLzdgiZmw

2) Unpack to one directory

3) Build

cd alps

./makeMtk -help

./mbldenv.sh

ccache -M 10G

prebuilts/misc/linux-x86/ccache/ccache -M 10G

./makeMtk listp

./makeMtk -t check-env

./makeMtk -t check-modem

./makeMtk -t clean

./makeMtk -t bird92_cwet_a_kk n| tee -a build.log

4) Need lots of coding and testing - dont flash if you dont know what are you doing

5) Partitions size are set by:

mediatek/build/tools/ptgen/MT6592/partition_table_MT6592.xls
 
