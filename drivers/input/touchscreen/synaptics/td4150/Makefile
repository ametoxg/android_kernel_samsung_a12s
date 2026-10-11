#
# Makefile for the Synaptics TCM touchscreen driver.
#

# Each configuration option enables a list of files.
obj-$(CONFIG_TOUCHSCREEN_SYNAPTICS_TCM_SPI) += synaptics_tcm_spi.o
obj-$(CONFIG_TOUCHSCREEN_SYNAPTICS_TCM_CORE) += synaptics_tcm_core_module.o synaptics_tcm_sec_fn.o synaptics_tcm_sec_fn_test.o
synaptics_tcm_core_module-objs := synaptics_tcm_core.o synaptics_tcm_touch.o
obj-$(CONFIG_TOUCHSCREEN_SYNAPTICS_TCM_ZEROFLASH) += synaptics_tcm_zeroflash.o
