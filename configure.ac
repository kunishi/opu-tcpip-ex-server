#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([FULL-PACKAGE-NAME], [VERSION], [BUG-REPORT-ADDRESS])
AC_CONFIG_SRCDIR([server.c])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([Makefile])
AM_INIT_AUTOMAKE

# Checks for programs.
AC_PROG_CC

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([arpa/inet.h stdlib.h string.h sys/socket.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_ARG_WITH([server-addr],
  AS_HELP_STRING([--with-server-addr], [Specify Server IP Address]),
  AC_DEFINE_UNQUOTED([SERVER_ADDR], ["$withval"], [Server IP Address])
)
AC_ARG_WITH([server-port],
  AS_HELP_STRING([--with-server-port], [Specify Server Port Number]),
  AC_DEFINE_UNQUOTED([SERVER_PORT], [$withval], [Server Port Number])
)

# Checks for library functions.
AC_CHECK_FUNCS([memset socket])

AC_OUTPUT
