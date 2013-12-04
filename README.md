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
