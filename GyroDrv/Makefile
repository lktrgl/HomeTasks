
#
# mpu6050 accelerometer & gyroscope
#
ifneq ($(KERNELRELEASE),)

obj-m := mpu6050.o

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