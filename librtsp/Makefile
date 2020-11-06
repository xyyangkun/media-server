ROOT:=../../sdk

#--------------------------------Output------------------------------
# OUTTYPE: 0-exe, 1-dll, 2-static
#--------------------------------------------------------------------
OUTTYPE = 2
OUTFILE = librtsp.a

#-------------------------------Include------------------------------
#
# INCLUDES = $(addprefix -I,$(INCLUDES)) # add -I prefix
#--------------------------------------------------------------------
INCLUDES = . \
					./include \
					../libmpeg/include/ \
					../../avcodec/avbsf/include/ \
					../libflv/include/ \
					../libmov/include/ \
					$(ROOT)/include \
					$(ROOT)/libhttp/include \
					../librtp/include

#-------------------------------Source-------------------------------
#
#--------------------------------------------------------------------
SOURCE_PATHS = source source/client source/server source/utils
SOURCE_FILES = $(foreach dir,$(SOURCE_PATHS),$(wildcard $(dir)/*.cpp))
SOURCE_FILES += $(foreach dir,$(SOURCE_PATHS),$(wildcard $(dir)/*.c))

SOURCE_FILES += $(ROOT)/source/digest/md5.c
SOURCE_FILES += $(ROOT)/source/base64.c

SOURCE_FILES += ../../avcodec/avbsf/src/aacbsf.c
SOURCE_FILES += ../../avcodec/avbsf/src/h264bsf.c
SOURCE_FILES += ../../avcodec/avbsf/src/h265bsf.c


#-----------------------------Library--------------------------------
#
# LIBPATHS = $(addprefix -L,$(LIBPATHS)) # add -L prefix
#--------------------------------------------------------------------
LIBPATHS =
ifdef RELEASE
# relase library path
LIBPATHS +=
else
LIBPATHS +=
endif

LIBS = 

STATIC_LIBS =

#-----------------------------DEFINES--------------------------------
#
# DEFINES := $(addprefix -D,$(DEFINES)) # add -L prefix
#--------------------------------------------------------------------
DEFINES =

include ../gcc.mk
