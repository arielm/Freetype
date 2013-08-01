Freetype
====
Provides support for Freetype 2.4.10 on OSX

**Build instructions for OSX:**

`cd freetype-2.4.10`  
`export MACOSX_DEPLOYMENT_TARGET=10.6`  
`./configure --with-old-mac-fonts --without-bzip2 \`  
`make`  

Then grab `libfreetype.a` from `obj/.libs`
