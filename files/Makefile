PWD	:= $(shell pwd)
OBJ	:= kedei
SRC := $(shell pwd)

obj-m := $(OBJ).o
#dtb-m := kedei-overlay.dtb

all: modules

modules:
	$(MAKE) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KERNEL_SRC) M=$(SRC) modules

modules_install:
	$(MAKE) -C $(KERNEL_SRC) M=$(SRC) modules_install

clean:
	rm -fr $(OBJ).o $(OBJ).ko
