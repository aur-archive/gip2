#gipgui by Tim Songhurst
#
pkgname=gip2
pkgver=2
pkgrel=6
pkgdesc="get_iplayer gui written in free pascal"
arch=('x86_64' 'i686')
url="http://foggybrain.50webs.com/"
license=('GPL')
groups=()
depends=('get_iplayer' 'gtk2')
opdepends=('mplayer')
makedepends=('lazarus')
provides=('gip2')
#replaces=('gip2')
#conflicts=('gip2')
backup=()
install=
source=('http://foggybrain.50webs.com/gipgui/gipgui-2-6.tar.gz')
md5sums=('d10870d67fca59675d6d8ffef0c0fab8')

build() {

mkdir -p $pkgdir/usr/bin
mkdir -p $pkgdir/usr/share/applications
mkdir -p $pkgdir/usr/share/pixmaps

if test "$CARCH" == i686; then
cd $srcdir/gipgui-$pkgver-$pkgrel/gipgui-gtk32
else
cd $srcdir/gipgui-$pkgver-$pkgrel/gipgui-gtk
fi

lazbuild project1.lpr

cp gipgui $pkgdir/usr/bin/
cp gips $pkgdir/usr/bin/
cp gipgui.desktop $pkgdir/usr/share/applications/
cp iplayer.png $pkgdir/usr/share/pixmaps/
chmod +x $pkgdir/usr/bin/gipgui
chmod +x $pkgdir/usr/bin/gips

}