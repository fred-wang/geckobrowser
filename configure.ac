dnl -*- Mode: Autoconf; tab-width: 4; indent-tabs-mode: nil; -*-
dnl vi: set tabstop=4 shiftwidth=4 expandtab syntax=m4:
dnl This Source Code Form is subject to the terms of the Mozilla Public
dnl License, v. 2.0. If a copy of the MPL was not distributed with this
dnl file, You can obtain one at http://mozilla.org/MPL/2.0/.

AC_PREREQ(2.13)
AC_INIT(GeckoBrowser, 0.1)
AC_CONFIG_SRCDIR(src/)

AC_SUBST(ANDROID_HOME)
AC_SUBST(ANDROID_TARGET_ID, android-19)
AC_SUBST(ANDROID_SUPPORT_LIBRARY_JAR, $ANDROID_HOME/extras/android/support/v4/android-support-v4.jar)
AC_SUBST(GECKOVIEW_URI, http://ftp.mozilla.org/pub/mozilla.org/mobile/nightly/latest-mozilla-central-android)

AC_CHECK_PROGS(ADB, adb, adb, $PATH:$ANDROID_HOME/platform-tools)
AC_CHECK_PROGS(ANDROID, android, android, $PATH:$ANDROID_HOME/tools)
AC_CHECK_PROGS(ANT, ant)
AC_CHECK_PROGS(UNZIP, unzip)
AC_CHECK_PROGS(WGET, wget)

if ! test -d "$ANDROID_HOME" ; then
    AC_MSG_WARN(["Android SDK not found. Did you set the \$ANDROID_HOME variable?"])
else
    if ! test -f "$ANDROID_SUPPORT_LIBRARY_JAR" ; then
       AC_MSG_WARN(["Android Support Library (version 4) not found."])
    fi
fi

AC_CONFIG_FILES(project.properties)
AC_CONFIG_FILES(Makefile)
AC_OUTPUT
