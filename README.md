Freetype
====
Provides support for Freetype 2.5.1 on OSX

**Build instructions for OSX:**

`cd freetype-2.5.1`  

`./configure CFLAGS="-arch i386" --without-zlib --without-png --without-bzip2`  
`make`  
`cp objs/.libs/libfreetype.a libfreetype-i386.a`  
`make clean`  

`./configure CFLAGS="-arch x86_64" --without-zlib --without-png --without-bzip2`  
`make`  
`cp objs/.libs/libfreetype.a libfreetype-x86_64.a`  
`make clean`  

`lipo -c libfreetype-i386.a libfreetype-x86_64.a -o libfreetype.a`  

**Build instructions for iOS:**

`cd freetype-2.5.1`  

`./configure --without-zlib --without-png --without-bzip2 'CFLAGS=-arch i686 -pipe -std=c99 -Wno-trigraphs -fpascal-strings -O2 -Wreturn-type -Wunused-variable -fmessage-length=0 -fvisibility=hidden -miphoneos-version-min=5.0 -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator6.1.sdk/usr/include/libxml2/ -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator6.1.sdk/'`  
`make`  
`cp objs/.libs/libfreetype.a libfreetype-i686.a`  
`make clean`  

`./configure --without-zlib --without-png --without-bzip2 '--prefix=/usr/local/iPhone' '--host=arm-apple-darwin' '--enable-static=yes' '--enable-shared=no' 'CC=/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/clang' 'CFLAGS=-arch armv7 -pipe -std=c99 -Wno-trigraphs -fpascal-strings -O2 -Wreturn-type -Wunused-variable -fmessage-length=0 -fvisibility=hidden -miphoneos-version-min=5.0 -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/usr/include/libxml2/ -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/' 'AR=/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/usr/bin/ar' 'LDFLAGS=-arch armv7 -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/ -miphoneos-version-min=5.0'`  
`make`  
`cp objs/.libs/libfreetype.a libfreetype-armv7.a`  
`make clean`  

`./configure --without-zlib --without-png --without-bzip2 '--prefix=/usr/local/iPhone' '--host=arm-apple-darwin' '--enable-static=yes' '--enable-shared=no' 'CC=/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/clang' 'CFLAGS=-arch armv7s -pipe -std=c99 -Wno-trigraphs -fpascal-strings -O2 -Wreturn-type -Wunused-variable -fmessage-length=0 -fvisibility=hidden -miphoneos-version-min=5.0 -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/usr/include/libxml2/ -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/' 'AR=/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/usr/bin/ar' 'LDFLAGS=-arch armv7s -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.0.sdk/ -miphoneos-version-min=5.0'`  
`make`  
`cp objs/.libs/libfreetype.a libfreetype-armv7s.a`  
`make clean`  

`lipo -c libfreetype-i686.a libfreetype-armv7.a libfreetype-armv7s.a -o libfreetype.a`  
