_APP_PKG_=${APP_PKG}
APP_DIR=/data/data/${_APP_PKG_}

all:
	sudo rm -f /home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a/libc++.so
	sudo ln -s /home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a/libc++_shared.so /home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a/libc++.so
	sudo rm -rf /home/cogroid/local/libgmp/armv7/*
	sudo mkdir -p /home/cogroid/local/libgmp/armv7/bbin
	sudo cp -rf ./bin/* /home/cogroid/local/libgmp/armv7/bbin/
	sudo rm -f /home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin/arm-linux-androideabi-cc
	sudo ln -s /home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin/arm-linux-androideabi-gcc /home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin/arm-linux-androideabi-cc
	cp -f /home/cogroid/local/android-ndk-r18b/platforms/android-24/arch-arm/usr/lib/crtbegin_so.o ../../
	cp -f /home/cogroid/local/android-ndk-r18b/platforms/android-24/arch-arm/usr/lib/crtend_so.o ../../
	sudo rm -rf ${APP_DIR}/libgmp
	sudo mkdir -p ${APP_DIR}
	sudo ln -s /home/cogroid/local/libgmp/armv7 ${APP_DIR}/libgmp
	cd ../../; \
	export PATH="/home/cogroid/local/libgmp/armv7/bbin:/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/arm-linux-androideabi/bin:/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin:${PATH}"; \
	./configure \
	--disable-static \
	--disable-assembly \
	ABI=32 \
	LDFLAGS=" -stdlib=libc++  -v --target=arm-linux-androideabi -march=armv7-a -fPIC -fno-integrated-as --sysroot /home/cogroid/local/android-ndk-r18b/sysroot -isystem /home/cogroid/local/android-ndk-r18b/sysroot/usr/include/arm-linux-androideabi -D__ANDROID_API__=22 -fexceptions -frtti -ffunction-sections -funwind-tables -fstack-protector-strong -Wno-invalid-command-line-argument -Wno-unused-command-line-argument -no-canonical-prefixes -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/include -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++abi/include -I/home/cogroid/local/android-ndk-r18b/sources/android/support/include -DANDROID -Wa,--noexecstack -Wformat -Werror=format-security -DNDEBUG -O2 -L/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -B/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -L/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -B/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -L/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a -B/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a  " \
	CFLAGS=" -stdlib=libc++  -v --target=arm-linux-androideabi -march=armv7-a -fPIC -fno-integrated-as --sysroot /home/cogroid/local/android-ndk-r18b/sysroot -isystem /home/cogroid/local/android-ndk-r18b/sysroot/usr/include/arm-linux-androideabi -D__ANDROID_API__=22 -fexceptions -frtti -ffunction-sections -funwind-tables -fstack-protector-strong -Wno-invalid-command-line-argument -Wno-unused-command-line-argument -no-canonical-prefixes -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/include -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++abi/include -I/home/cogroid/local/android-ndk-r18b/sources/android/support/include -DANDROID -Wa,--noexecstack -Wformat -Werror=format-security -DNDEBUG -O2 -L/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -B/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -L/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -B/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -L/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a -B/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a  " \
	CPPFLAGS=" -stdlib=libc++  -v --target=arm-linux-androideabi -march=armv7-a -fPIC -fno-integrated-as --sysroot /home/cogroid/local/android-ndk-r18b/sysroot -isystem /home/cogroid/local/android-ndk-r18b/sysroot/usr/include/arm-linux-androideabi -D__ANDROID_API__=22 -fexceptions -frtti -ffunction-sections -funwind-tables -fstack-protector-strong -Wno-invalid-command-line-argument -Wno-unused-command-line-argument -no-canonical-prefixes -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/include -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++abi/include -I/home/cogroid/local/android-ndk-r18b/sources/android/support/include -DANDROID -Wa,--noexecstack -Wformat -Werror=format-security -DNDEBUG -O2 -L/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -B/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -L/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -B/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -L/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a -B/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a  " \
	CXXFLAGS=" -stdlib=libc++  -v --target=arm-linux-androideabi -march=armv7-a -fPIC -fno-integrated-as --sysroot /home/cogroid/local/android-ndk-r18b/sysroot -isystem /home/cogroid/local/android-ndk-r18b/sysroot/usr/include/arm-linux-androideabi -D__ANDROID_API__=22 -fexceptions -frtti -ffunction-sections -funwind-tables -fstack-protector-strong -Wno-invalid-command-line-argument -Wno-unused-command-line-argument -no-canonical-prefixes -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/include -I/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++abi/include -I/home/cogroid/local/android-ndk-r18b/sources/android/support/include -DANDROID -Wa,--noexecstack -Wformat -Werror=format-security -DNDEBUG -O2 -L/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -B/home/cogroid/local/android-ndk-r18b/platforms/android-22/arch-arm/usr/lib -L/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -B/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/lib/gcc/arm-linux-androideabi/4.9.x/armv7-a/thumb -L/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a -B/home/cogroid/local/android-ndk-r18b/sources/cxx-stl/llvm-libc++/libs/armeabi-v7a  " \
	--build=i386-linux-gnu \
	--host=arm-linux-androideabi \
	--prefix=${APP_DIR}/libgmp

build:
	cp -f /home/cogroid/local/android-ndk-r18b/platforms/android-24/arch-arm/usr/lib/crtbegin_so.o ../../
	cp -f /home/cogroid/local/android-ndk-r18b/platforms/android-24/arch-arm/usr/lib/crtend_so.o ../../
	cd ../../; \
	export PATH="/home/cogroid/local/libgmp/armv7/bbin:/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/arm-linux-androideabi/bin:/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin:${PATH}"; \
	make

clean:
	cd ../../; \
	make clean

install:
	sudo sh -c 'cd ../../; \
	export PATH="/home/cogroid/local/libgmp/armv7/bbin:/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/arm-linux-androideabi/bin:/home/cogroid/local/android-ndk-r18b/toolchains/arm-linux-androideabi-4.9/prebuilt/linux-x86_64/bin:${PATH}"; \
	make install;'

