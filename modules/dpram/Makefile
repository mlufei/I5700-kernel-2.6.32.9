##############################################################################
# COPYRIGHT(C)	: Samsung Electronics Co.Ltd, 2006-2011 ALL RIGHTS RESERVED
# AUTHOR		: KyoungHOON Kim (khoonk)
##############################################################################
# VERSION&DATE	: Version 1.00	2006/06/02 (khoonk)
##############################################################################

MOD_NAME = dpram

ifneq ($(KERNELRELEASE), )

EXTRA_CFLAGS += -I$(PRJROOT)/modules/include

obj-m := $(MOD_NAME).o

else

all:
	@$(MAKE) --no-print-directory -C $(KDIR) \
		SUBDIRS=$(CURDIR) modules

clean:
	rm -f *.o *.ko *.mod.c *.mod.o *~ .*.cmd .*.o.cmd Module.symvers modules.order $(obj-m)
	[ -d .tmp_versions ] && ( rm -rf .tmp_versions/*; rmdir .tmp_versions; )

install:
	@$(MAKE) --no-print-directory -C $(KDIR) \
		SUBDIRS=$(CURDIR) modules_install

endif
