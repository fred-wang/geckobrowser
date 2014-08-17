geckobrowser
============

Very basic Android browser application that uses the GeckoView widget.

This is a fork of [GeckoBrowser](https://github.com/mfinkle/geckobrowser) that
uses `make` and `ant` to download the dependencies, setup the Android projects,
build and install the GeckoBrowser app.

Build Instructions
------------------

Follow the [prerequisites to build Fennec](https://wiki.mozilla.org/Mobile/Fennec/Android), so that you have an Android development environnement compatible
with Gecko's requirements. Be sure to have `ant` and `android` in your `PATH`
and set the `ANDROID_SDK` variable to the path of your android sdk.

You need classical dependencies installed by default and/or available from the
package manager of Linux/Mac/Cygwin:
[coreutils](https://www.gnu.org/software/coreutils/),
[make](https://www.gnu.org/software/make/),
[unzip](http://www.info-zip.org/UnZip.html),
[wget](https://www.gnu.org/software/wget/) and
[ant](http://ant.apache.org/).

Now, just follow the standard procedure:

      ./configure
      make all
      make install # This assumes that you have a simulator/device connected

Use `make help` for more commands.
