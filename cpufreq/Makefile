# compile with 
# make CFLAGS_MODULE=-fno-pic modules

KERNEL_SRC = /home/sunatomo/Xperia_Z/kernel-stock/kernel
BUILD_DIR := $(shell pwd)
CROSS_COMPILE = /opt/prebuilts/gcc/linux-x86/arm/arm-eabi-4.6/bin/arm-eabi-
ARCH = arm
CFLAGS_MODULE = -fno-pic modules
KBUILD_EXTMOD = $(KERNEL_SRC)/drivers/cpufreq
MAKEARCH = $(MAKE) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) CFLAGS_MODULE=$(CFLAGS_MODULE)

symsearch-y := search.o hijack.o
obj-m += symsearch.o
#obj-m += xperiaz_HYPER.o
#obj-m += xperiaz_abyssplug.o
#obj-m += xperiaz_abyssplugv2.o
#obj-m += xperiaz_adaptive.o
#obj-m += xperiaz_alucard.o
#obj-m += xperiaz_asswax.o
#obj-m += xperiaz_badass.o
#obj-m += xperiaz_dancedance.o
#obj-m += xperiaz_darkness.o
#obj-m += xperiaz_intelliactive.o
#obj-m += xperiaz_intellidemand.o
#obj-m += xperiaz_lionheart.o
#obj-m += xperiaz_nightmare.o
obj-m += cpufreq_pegasusq.o
obj-m += cpufreq_smartassH3.o
#obj-m += xperiaz_wheatley.o
obj-m += cpufreq_intellimm.o

all:
	$(MAKEARCH) -C $(KERNEL_SRC) SUBDIRS=$(BUILD_DIR) modules

clean:
	$(MAKE) -C $(KERNEL_SRC) SUBDIRS=$(BUILD_DIR) clean
