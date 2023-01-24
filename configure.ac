
# SPDX-License-Identifier: GPL-2.0
AC_PREREQ([2.69])
AC_INIT([bccmd], [6.0])
AM_INIT_AUTOMAKE([subdir-objects])

AC_CONFIG_SRCDIR([src/bccmd.c])
AC_CONFIG_HEADERS([config.h])

AC_PROG_CC

AC_CHECK_LIB([bluetooth], [bt_error])

AC_CHECK_HEADERS([fcntl.h stdint.h sys/ioctl.h sys/socket.h termios.h unistd.h])

AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT8_T

AC_FUNC_MALLOC
AC_FUNC_MMAP
AC_CHECK_FUNCS([memset munmap strcasecmp strchr strdup strerror strncasecmp strpbrk strstr strtol])

AC_ARG_ENABLE(manpages, AS_HELP_STRING([--disable-manpages],
			[disable building of manual pages]),
					[enable_manpages=${enableval}])
AM_CONDITIONAL(MANPAGES, test "${enable_manpages}" != "no")

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
