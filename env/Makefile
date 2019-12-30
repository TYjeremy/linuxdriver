ifneq ($(KERNELRELEASE),)
	mymodule-bojs := hello.o
	obj-m := hello.o
else
	PWD := $(shell pwd)
	KERNELDIR = /lib/modules/$(shell uname -r)/build
all:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) 
clean:
	rm -rf *.o *~ core .depend .*.cmd *.ko *.mod.c *.order *.symvers
endif
