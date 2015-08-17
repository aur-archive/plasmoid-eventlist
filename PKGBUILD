# Maintainer: (locke87) Felix Mauch
# based on http://kde-apps.org/content/show.php?content=124416

pkgname=plasmoid-eventlist
pkgver=0.6
pkgrel=1
pkgdesc="This is a plasmoid to show the events from Akonadi resources (KOrganizer, Birthdays etc.)."
url="http://kde-look.org/content/show.php/Eventlist?content=107779"
license=('GPL')
arch=('i686' 'x86_64')
depends=('kdebase-workspace>=4.7.0' 'boost-libs')
makedepends=('gcc' 'cmake' 'automoc4' 'boost')
source=(http://www.kde-look.org/CONTENT/content-files/107779-plasmoid-eventlist-$pkgver.tar.bz2)
md5sums=('4bde86ea2ba56a5449fa95483b42b0cb')

 
build() {
  cd $startdir/src/plasmoid-eventlist-$pkgver/
  mkdir build
  cd build
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ../
  make || return 1
  make DESTDIR=$pkgdir install
}