all:
	sudo mkdir -p /home/cogroid/local/libgmp/x64
	mkdir -p ../../build/x64
	cd ../../build/x64; \
	../../configure \
	--prefix=/home/cogroid/local/libgmp/x64; \
	make

clean:
	cd ../../build/x64; \
	make clean

install:
	sudo sh -c 'cd ../../build/x64; \
	make install;'

