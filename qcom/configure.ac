#                                               -*- Autoconf -*-
# configure.ac -- Autoconf script for qcom audioreach-conf
#

# Process this file with autoconf to produce a configure script

# Requires autoconf tool later than 2.61
AC_PREREQ(2.69)
# Initialize the acdbdata package version 1.0.0
AC_INIT([acdbdata],1.0.0)
# Does not strictly follow GNU Coding standards
AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects])


# Checks for programs.
AC_PROG_CC
AM_PROG_CC_C_O
AC_PROG_CXX
AC_PROG_LIBTOOL
AC_PROG_AWK
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
PKG_PROG_PKG_CONFIG

# Check for automotive support
AC_ARG_WITH([automotive],
    AS_HELP_STRING([--with-automotive], [Enable automotive support]))

# Define conditional for automotive support
AM_CONDITIONAL([AUTOMOTIVE], [test "x$with_automotive" = "xyes"])

# Conditionally configure automotive subdirectory
AS_IF([test "x$with_automotive" = "xyes"], [
    AC_CONFIG_SUBDIRS([automotive])
])

AC_ARG_WITH([qli],
    AS_HELP_STRING([--with-qli], [Enable qli support]))

# Define conditional for qli support
AM_CONDITIONAL([QLI], [test "x$with_qli" = "xyes"])

# Conditionally configure qli subdirectory
AS_IF([test "x$with_qli" = "xyes"], [
    AC_CONFIG_SUBDIRS([qli])
])

AC_CONFIG_FILES([ \
        Makefile \
        kvh2xml.pc \
        ])

AC_OUTPUT