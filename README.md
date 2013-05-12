android_kernel_pantech_ef47s
============================

Sky VegaRacer2 Kernel Source JB
Edit by Mir(whdghks913)


You Should turn off option "Automatically append version information to the version string"

- ./build.sh menuconfig

- General setup > Automatically append version information to the version string

"CONFIG_LOCALVERSION_AUTO=y" in .config



Build.sh command list

- ./build.sh

- ./build.sh menuconfig

- ./build.sh clean

- ./build.sh mrporper


1. How to build Kernel source of IM-A830S_JB

    - Firstly Get Toolchain from android git server and etc ¡Š
        GCC correct version is arm-eabi-4.6
    - modify build_kernel shell script.
        edit "CROSS_COMPILE" to toolchain path ( You downloaded )
        ex) CROSS_COMPILE=$(your download directory)/prebuilts/gcc/linux-x86/arm/arm-eabi-4.6/bin/arm-eabi-
    - run build_kernel.sh
        $./build_kernel.sh
         

2.	Output File Location
    - kernel : ./obj/KERNEL_OBJ/arch/arm/boot/zImage
    - module : ./obj/KERNEL_OBJ/drivers/*/*.ko
      
3.	How to Clean Kernel object files
    - run clean_kernel.sh
        $./clean_kernel.sh
