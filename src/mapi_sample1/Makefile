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

# Binaries
CC=/usr/bin/gcc
PKGCONFIG=/usr/bin/pkg-config
RM=/bin/rm

TARGET=mapi_sample1

#CFLAGS=-g -Wall -Wextra

TARGET    = mapi_sample1


# Phony targets
.PHONY: all clean

# Build everything
all: $(TARGET)

# Cycle
cycle: clean

# Build targte
$(TARGET):$(TARGET).c
	$(CC) mapi_sample1.c -o mapi_sample1 `pkg-config libmapi --cflags --libs`

clean: $(TARGET)
	$(RM) -f $(TARGET)
