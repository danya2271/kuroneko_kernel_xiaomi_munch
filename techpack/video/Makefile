# SPDX-License-Identifier: GPL-2.0-only
KBUILD_CFLAGS	+= -mllvm -inline-threshold=1600
KBUILD_CFLAGS	+= -mllvm -inlinehint-threshold=1750
KBUILD_CFLAGS   += -mllvm -unroll-threshold=20
# auto-detect subdirs
ifeq ($(CONFIG_ARCH_KONA), y)
include $(srctree)/techpack/video/config/konavid.conf
endif

ifeq ($(CONFIG_ARCH_KONA), y)
LINUXINCLUDE    += -include $(srctree)/techpack/video/config/konavidconf.h
endif

# auto-detect subdirs
ifeq ($(CONFIG_ARCH_LITO), y)
include $(srctree)/techpack/video/config/litovid.conf
endif

ifeq ($(CONFIG_ARCH_LITO), y)
LINUXINCLUDE    += -include $(srctree)/techpack/video/config/litovidconf.h
endif

# auto-detect subdirs
ifeq ($(CONFIG_ARCH_BENGAL), y)
include $(srctree)/techpack/video/config/bengalvid.conf
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
LINUXINCLUDE    += -include $(srctree)/techpack/video/config/bengalvidconf.h
endif

obj-y +=msm/
