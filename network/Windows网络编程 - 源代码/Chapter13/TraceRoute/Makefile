# Nmake macros for building Windows 32-Bit apps
TARGETOS=BOTH
#APPVER=5.0

!include <win32.mak>


objs=traceroute.obj

all: traceroute.exe

# Update the resource if necessary

# Update the object file if necessary

.c.obj: 
    $(cc) $(cdebug) $(cflags) $(cvarsmt) /Zp1 $*.c

# Update the executable file if necessary, and if so, add the resource back in.

traceroute.exe: $(objs) $(common_objs) 
    $(link) $(linkdebug) $(conlflags) -out:traceroute.exe $(objs) $(conlibsmt) ws2_32.lib


clean:
	del *.obj
	del *.exe
