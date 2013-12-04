Freetype
====
Provides support for Freetype 2.5.1 on OSX

**Build instructions for OSX:**

`cd freetype-2.5.1`  
`./configure CFLAGS="-arch i386" --without-zlib --without-png --without-bzip2`  
`make`  

Then grab `libfreetype.a` from `obj/.libs`
