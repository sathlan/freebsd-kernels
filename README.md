FreeBSD Kernels
===============

# Soekris 4801 - SOEKRIS #

From [the soekris wiki](http://wiki.soekris.info/Installing_FreeBSD) I got
the necessary options and comments.

    CPU_SOEKRIS enables support www.soekris.com hardware
    CPU_ELAN enables support for AMDs ElanSC520 CPU
        CPU_ELAN_PPS enables precision timestamp code
        CPU_ELAN_XTAL sets the clock crystal frequency in Hz 
    CPU_GEODE is for the SC1100 Geode embedded processor - This option is necessary because the i8254 timecounter is toast. 

From [this project](http://www.wirelessleiden.nl/projects/nodefactory/browser/hybrid/branches/releng-10/nanobsd/cfg/kernel.wleiden) I got a running kernel configuration.

On the board there is a safenet 1141 crypto accelerator. The man [safe(4)](http://www.freebsd.org/cgi/man.cgi?query=safe&apropos=0&sektion=0&manpath=FreeBSD+10.0-RELEASE&arch=default&format=html) has the missing part.

Eventually there is the `glxsb` driver that should not be activated,
but that's fine as I cannot find information about it execpt
[there](http://pfsensesetup.com/tag/glxsb/)

