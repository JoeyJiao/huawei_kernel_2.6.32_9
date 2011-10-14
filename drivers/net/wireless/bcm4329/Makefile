# bcm4329
DHDCFLAGS = -DLINUX -DBCMDRIVER -DBCMDONGLEHOST -DDHDTHREAD -DBCMWPA2         \
	-DUNRELEASEDCHIP -DCUSTOM_SDCC_WIFI_SLOT=2 -DCUSTOM_OOB_GPIO_NUM=17   \
	-DBCMWAPI_WPI -DDHD_GPL -DDHD_SCHED -DBDC -DTOE -DDHD_BCMEVENTS       \
	-DSHOW_EVENTS -DBCMSDIO -DDHD_GPL -DBCMLXSDMMC -DBCMPLATFORM_BUS      \
	-Wall -Wstrict-prototypes -Werror -DOOB_INTR_ONLY -DCUSTOMER_HW2      \
	-DDHD_USE_STATIC_BUF -DMMC_SDIO_ABORT -DSOFTAP -DHW_OOB               \
        -DEMBEDDED_PLATFORM -DARP_OFFLOAD_SUPPORT -DPKT_FILTER_SUPPORT        \
	-Idrivers/net/wireless/bcm4329 -Idrivers/net/wireless/bcm4329/include

DHDOFILES = dhd_linux.o linux_osl.o bcmutils.o dhd_common.o dhd_custom_gpio.o \
	wl_iw.o siutils.o sbutils.o aiutils.o hndpmu.o bcmwifi.o dhd_sdio.o   \
	dhd_linux_sched.o dhd_cdc.o bcmsdh_sdmmc.o bcmsdh.o bcmsdh_linux.o    \
	bcmsdh_sdmmc_linux.o

obj-$(CONFIG_BCM4329) += dhd.o
dhd-objs += $(DHDOFILES)
EXTRA_CFLAGS = $(DHDCFLAGS)
EXTRA_LDFLAGS += --strip-debug
