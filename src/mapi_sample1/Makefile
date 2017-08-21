# Makefile
# Created Mon Aug 21 14:40:01 AKDT 2017
# Copyright (C) 2017 by Raymond E. Marcil <marcilr@gmail.com>
#

GCC=/usr/bin/gcc
PKGCONFIG=/usr/bin/pkg-config


all: mapi_sample1

mapi_sample1: mapi_sample1.c
	$(GCC) mapi_sample1.c -o mapi_sample1 '$(PKGCONFIG) libmapi --cflags --libs'
