# SPDX-License-Identifier: GPL-2.0-only
KBUILD_CFLAGS	+= -mllvm -inline-threshold=1600 -fno-strict-aliasing -funit-at-a-time
KBUILD_CFLAGS	+= -mllvm -inlinehint-threshold=1750
KBUILD_CFLAGS   += -mllvm -unroll-threshold=20
obj-$(CONFIG_EROFS_FS) += erofs.o
erofs-objs := super.o inode.o data.o namei.o dir.o utils.o pcpubuf.o
erofs-$(CONFIG_EROFS_FS_XATTR) += xattr.o
erofs-$(CONFIG_EROFS_FS_ZIP) += decompressor.o zmap.o zdata.o
