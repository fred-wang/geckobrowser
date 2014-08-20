geckobrowser
============

Very basic Android browser application that uses the GeckoView widget.

This is a fork of [GeckoBrowser](https://github.com/mfinkle/geckobrowser) that
uses `make` and `ant` to download the dependencies, setup the Android projects,
build and install the GeckoBrowser app.

Build Instructions
------------------

Follow the [prerequisites to build Fennec](https://wiki.mozilla.org/Mobile/Fennec/Android), so that you have an Android development environnement compatible
with Gecko's requirements. Be sure to set the `ANDROID_HOME` variable to the
path of your android sdk.

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

By default, the `geckoview_assets.zip` and `geckoview_library.zip` files will
be downloaded from the official mozilla-central nightly builds. If you wish to
use your own local builds, you can use the convenient command

      make importLocal FENNEC_OBJDIR=/path/to/fennec/objdir

to import the zip archives.

Try `make help` for more commands.
