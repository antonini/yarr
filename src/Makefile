KERNEL_DIR := /lib/modules/`uname -r`/build
EXTRA_CFLAGS += -DDEBUG

obj-m += yarr.o
yarr-objs := debug.o funcs.o config.o intrhandler.o interrupt.o \
			 syscall.o hide.o hook.o yarrops.o main.o
hook-objs := syscall.o

all:
	make -C $(KERNEL_DIR) SUBDIRS=$(PWD) modules

clean:
	make -C $(KERNEL_DIR) SUBDIRS=$(PWD) clean
