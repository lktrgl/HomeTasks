#CONFIG_MODULE_SIG=n

#
# ssd1306 OLED graphic display module
#
ifneq ($(KERNELRELEASE),)

obj-m := ssd1306.o

else


ifeq ($(BUILD_KERNEL),)
	$(error Path to kernel tree - BUILD_KERNEL variable is not defined!)
endif

.PHONY: all clean dtb

all:
	$(MAKE) -C $(BUILD_KERNEL) M=$(CURDIR) modules

clean:
	$(MAKE) -C $(BUILD_KERNEL) M=$(CURDIR) clean

dtb:
	cp am335x-bone-common.dtsi $(KERNEL_SOURCE)/arch/arm/boot/dts/
	$(MAKE) -C $(BUILD_KERNEL) M=$(CURDIR) dtbs


endif
