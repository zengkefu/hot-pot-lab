obj-$(CONFIG_OPROFILE) += oprofile.o

obj-y := dummy.o

ifeq (0, 1)
DRIVER_OBJS = $(addprefix ../../../drivers/oprofile/, \
		oprof.o cpu_buffer.o buffer_sync.o \
		event_buffer.o oprofile_files.o \
		oprofilefs.o oprofile_stats.o \
		timer_int.o )

ifeq ($(CONFIG_HW_PERF_EVENTS),y)
DRIVER_OBJS += $(addprefix ../../../drivers/oprofile/, oprofile_perf.o)
endif

oprofile-y				:= $(DRIVER_OBJS) common.o
endif