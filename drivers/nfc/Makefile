# SPDX-License-Identifier: GPL-2.0
#
# Makefile for nfc devices
#

ifneq ($(SEC_BUILD_CONF_USE_ESE_TZ), false)
	CFLAGS_pn547.o += -DENABLE_ESE_SPI_SECURED
endif

ifeq ($(CONFIG_SAMSUNG_NFC),m)
obj-$(CONFIG_SAMSUNG_NFC)		+= nfc_sec.o
nfc_sec-$(CONFIG_NFC_FEATURE_SN100U)	+= cold_reset.o
nfc_sec-$(CONFIG_SEC_NFC)		+= sec_nfc.o
nfc_sec-$(CONFIG_SEC_NFC_LOGGER)	+= nfc_logger/nfc_logger.o
nfc_sec-$(CONFIG_NFC_PN547)		+= pn547.o
else
obj-$(CONFIG_NFC_PN547)			+= pn547.o
obj-$(CONFIG_NFC_FEATURE_SN100U)	+= cold_reset.o
obj-$(CONFIG_SEC_NFC)			+= sec_nfc.o
obj-$(CONFIG_SEC_NFC_LOGGER)		+= nfc_logger/nfc_logger.o
endif
ccflags-$(CONFIG_NFC_DEBUG) := -DDEBUG

