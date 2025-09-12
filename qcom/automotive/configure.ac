#                                               -*- Autoconf -*-
# configure.ac -- Autoconf script for automotive audioreach-conf
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

# Check for platform
AC_ARG_WITH([sa8797],
    AS_HELP_STRING([--with-sa8797], [Enable sa8797 support]))

# Define conditional for automotive support
AM_CONDITIONAL([SA8797], [test "x$with_sa8797" = "xyes"])

AC_CONFIG_FILES([ \
        Makefile \
        ])

# Only generate sa8797 files if --with-sa8797 is specified
AS_IF([test "x$with_sa8797" = "xyes"], [
    AC_CONFIG_FILES([
        sa8797/Makefile
        sa8797/config.pc
    ])
])

AC_OUTPUT
