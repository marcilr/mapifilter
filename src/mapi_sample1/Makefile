# -*- Mode: Makefile -*-
#
# Makefile
# Created Tue Aug 22 15:25:00 AKDT 2017
# Copyright (C) 2017 by Raymond E. Marcil <marcilr@gmail.com>
#
# 
# Permission is granted to copy, distribute and/or modify this document
# under the terms of the GNU Free Documentation License, Version 1.3
# or any later version published by the Free Software Foundation;
# with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
# A copy of the license is included in the section entitled "GNU
# Free Documentation License".
#
# Makefile for mapifilter
#

#
# Configuration
#
TARGET    = mapi_sample1

#
# Binaries
#
# Binaries
CC        = /usr/bin/gcc
PKGCONFIG = /usr/bin/pkg-config
RM        = /bin/rm


# Define phony. i.e. non-file targets.
.PHONY: all clean mostlyclean cycle dist

all:
	$(CC) mapi_sample1.c -o mapi_sample1 `pkg-config libmapi --cflags --libs`

clean: $(TARGET)
	$(RM) -f $(TARGET)

cycle: clean all
