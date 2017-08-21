# Makefile
# Created Mon Aug 21 14:40:01 AKDT 2017
# Copyright (C) 2017 by Raymond E. Marcil <marcilr@gmail.com>
#
# Links
# =====
# How to use pkg-config in Make
# Solid detials here
# https://stackoverflow.com/questions/28533059/how-to-use-pkg-config-in-make
#

CC        = /usr/bin/gcc
PKGCONFIG = /usr/bin/pkg-config

#CFLAGS    = -Wall -W -pedantic
#CFLAGS    += -llibmapi
#CFLAGS    += -L/usr/lib/x86_64-linux-gnu
#CFLAGS    += -I/usr/include/libmapi
#CFLAGS    += -I/usr/include/samba-4.0

CFLAGS=-g -Wall -Wextra $(shell pkg-config --cflags libmapi.so.2.2)
LDFLAGS=$(shell pkg-config --libs libmapi.so.2.2)

# Alleviate:
# /usr/include/libmapi/libmapi.h:45:20: fatal error: dcerpc.h: No such file or directory
# include <dcerpc.h>
#CFLAGS     += /usr/include/samba-4.0
CFLAGS      += /usr/include/samba-4.0/gen_ndr 


#FLAG      = -DDEBUG_FLAG
#CFLAGS    += $(FLAG)

TARGET    = mapi_sample1


all: $(TARGET)

#
# Dependencies:
# -I.                                For libmapi/libmapi.h 
# /usr/include/libmapi/libmapi.h

# -I/usr/include/samba-4.0           For dcerpc.h
# -I/usr/include/samba-4.0/gen_ndr   For exchange.h>
#
# /usr/lib/x86_64-linux-gnu/libmapi.so
# /usr/lib/x86_64-linux-gnu/libmapi.so.0
# /usr/lib/x86_64-linux-gnu/libmapi.so.2.2
# /usr/lib/x86_64-linux-gnu/libmapiadmin.so.0
# /usr/lib/x86_64-linux-gnu/libmapiadmin.so.2.2
# /usr/lib/x86_64-linux-gnu/pkgconfig/libmapi.pc
#
# Syntax:
#   -I <searchpath to include files>
#   -L <searchpath to the lib file>
#   -l<thelibname>
#
# --How to include needed C library using gcc?
#   https://stackoverflow.com/questions/6016815/how-to-include-needed-c-library-using-gcc
#
$(TARGET): $(TARGET).c
	@echo "In Makefile: FLAG = <$(FLAG)>"
	$(CC) $(TARGET).c $(CFLAGS) $< -o $@
#	$(CC) mapi_sample1.c  -o mapi_sample1 -I/usr/include/samba-4.0 '$(PKGCONFIG) --cflags --libs libmapi'
