1. Android buid
  - Download original android source code (Gingerbread) from http://source.android.com                    
  - Untar opensource packages of Cosmo_Froyo.tar.gz into downloaded android source directory 
  - And, merge the source into the android source code(Gingerbread)
  - Run following scripts to build android
    a) cd android
    b) source ./build/envsetup.sh                                         
    c) choosecombo 1 1 generic 3                                     
    d) make -j4
  - When you compile the android source code, you have to add google original prebuilt source(toolchain) 
    into the android folder 
  - After build, you can find output at out/target/product/generic  
  - x-loader build and re-downloading then boot may not be Because the signing process is missing. 

2. Kernel Build
  - We checked building source at X86_64 architecture 
  - Untar using follwwing command at the android folder
    	tar zxvf Cosmo_Kernel.tar.gz
  - cd Kernel
  - make ARCH=arm CROSS_COMPILE=arm-none-linux-gnueabi- cosmo_rev_1.11_defconfig zImage
  - After Build, You Can find the build image at arch/arm/boot


