# -*- tab-width:8; indent-tabs-mode:t; c-basic-offset:2; -*-
# vim: set noet sw=2 ts=8 sts=0:
#
# Copyright (c)
#   2020 FAU -- Joachim Falk <joachim.falk@fau.de>
# 
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 2 of the License, or
# (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_INIT(
  [SysteMoC Top], [1.0],
  [joachim.falk@fau.de],
  [systemoc-top])
AC_PREREQ(2.64)
ACJF_INIT

AC_CONFIG_SRCDIR([forall-projects.sh])
AC_CONFIG_AUX_DIR([BuildSystem])
AC_CONFIG_MACRO_DIR([BuildSystem/m4])

AC_CANONICAL_BUILD
AC_CANONICAL_HOST

dnl Checks for programs.
ACJF_CHECK_CROSSTOOL(CC, gcc)
ACJF_CHECK_CROSSTOOL(CXX, g++)
ACJF_CHECK_CROSSTOOL(AR, ar)
ACJF_CHECK_CROSSTOOL(RANLIB, ranlib)
ACJF_CHECK_CROSSTOOL(NM, nm)
AC_PROG_CXXCPP
AC_PROG_CPP
# Checks for programs.
#AC_PROG_LIBTOOL
#AC_PROG_INSTALL
#AC_PROG_LN_S
#AC_PROG_MAKE_SET

AC_DISABLE_SHARED
AC_PROG_LIBTOOL

AM_INIT_AUTOMAKE([subdir-objects])

ACJF_ARG_DEBUG([yes], [], [-DNDEBUG])

AC_CONFIG_HEADER([config.h])

dnl check for exe extension
AC_EXEEXT

# Checks for header files.
# AC_FUNC_ALLOCA
# AC_HEADER_STDC
# AC_CHECK_HEADERS([OS.h fcntl.h limits.h mach/mach.h malloc.h stddef.h stdint.h stdlib.h string.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

ACJF_CONFIG_PKG([CoSupport], [[compile:Support]])
dnl ACJF_CONFIG_PKG([LibNGAnalysis])
dnl ACJF_CONFIG_PKG([LibSGX])
dnl ACJF_CONFIG_PKG([LibSGXUtils])
dnl ACJF_CONFIG_PKG([SGXUtils])
dnl ACJF_CONFIG_PKG([Maestro-Crescendo], [[disabled],[compile:Maestro/Bruckner]])
dnl ACJF_CONFIG_PKG([Maestro], [[disabled],[compile:Maestro/MetaMap]])
ACJF_CONFIG_PKG([SysteMoC])
ACJF_CONFIG_PKG([SystemC-VPC])
dnl ACJF_CONFIG_PKG([Maestro-Crescendo], [[disabled],[compile:Maestro/Crescendo]])
dnl ACJF_CONFIG_PKG([Maestro], [[disabled],[compile:Maestro/ModelLibrary]])
dnl ACJF_CONFIG_PKG([Synthesis-Framework])
dnl ACJF_CONFIG_PKG([Synthesis-SW])
dnl ACJF_CONFIG_PKG([Synthesis-Pthread])
dnl ACJF_CONFIG_PKG([Synthesis-SystemC])
dnl ACJF_CONFIG_PKG([Synthesis-Cynthesizer])
dnl ACJF_CONFIG_PKG([Synthesis-TLM])
dnl ACJF_CONFIG_PKG([Tools])
dnl ACJF_CONFIG_PKG([Clustering])
dnl ACJF_CONFIG_PKG([ActorLibrary])
dnl ACJF_CONFIG_PKG([Testcases])
dnl ACJF_CONFIG_PKG([Examples])
dnl ACJF_CONFIG_PKG([toolsupport])

SUBDIRS=$subdirs
AC_SUBST(SUBDIRS)

AC_CONFIG_FILES([Makefile])

ACJF_DONE

AC_OUTPUT
