#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

# AC_PREREQ([2.69])
AC_INIT([libmysql-connector], [0.1], [bjtj10@gmail.com])

AC_CONFIG_SRCDIR([src/mysql-connector.cpp])
AC_CONFIG_HEADERS([config.h])

AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_AUX_DIR([build-aux])

AM_SILENT_RULES([yes])

AM_INIT_AUTOMAKE
LT_PREREQ([2.2])
LT_INIT([dlopen])

AC_LANG([C++])

# Checks for programs.
AC_PROG_CXX

# Checks for libraries.
ACX_PTHREAD
PKG_CHECK_MODULES([LIBOSLAYER], [oslayer])


# Checks for header files.
AC_CHECK_HEADERS([arpa/inet.h netdb.h netinet/in.h sys/socket.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_TYPE_SIZE_T

# Checks for library functions.
AC_CHECK_FUNCS([clock_gettime memset mkdir select socket dlopen])

# mysql client
PKG_CHECK_MODULES([LIBMYSQLCLIENT],[mysqlclient],
	[HAVE_PKG_MYSQLCLIENT=yes],[HAVE_PKG_MYSQLCLIENT=no])


#
AC_CONFIG_FILES([Makefile
				 src/Makefile
				 tests/Makefile
				 mysql-connector.pc])
AC_OUTPUT
