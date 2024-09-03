obj-m += kernelspace.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
	gcc -o userspace userspace.c

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
	rm userspace