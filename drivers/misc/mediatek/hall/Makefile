include $(srctree)/drivers/misc/mediatek/Makefile.custom


obj-$(CONFIG_MTK_TINNO_HALL)	+= hall_device.o

WIKO_UNIFY_DEF := $(strip $(subst ro.wiko.type =,,$(shell cat $(PWD)/build.ini |grep ^ro.wiko.type)))
ifeq ($(strip $(WIKO_UNIFY_DEF)),unify)
ccflags-y += -DCONFIG_WIKO_UNIFY
$(warning ---add marco CONFIG_WIKO_UNIFY---)
endif
ifeq ($(strip $(CONFIG_PROJECT_V2802_WIK_FR)),yes)
ccflags-y += -DCONFIG_PROJECT_V2802_WIK_FR
$(warning ---add marco CONFIG_PROJECT_V2802_WIK_FR---)
endif

