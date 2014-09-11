pkgname=vorbisgain
pkgver=0.37
pkgrel=1
pkgdesc="A utility that computes the ReplayGain values for Ogg Vorbis files."
arch=('x86_64')
url="http://sjeng.org/vorbisgain.html"
license=('GPL')
depends=('libvorbis')
source=(http://sjeng.org/ftp/vorbis/${pkgname}-${pkgver}.tar.gz)
md5sums=('850b05a7b2b0ee67edb5a27b8c6ac3a2')

build() {
  cd ${srcdir}/${pkgname}-${pkgver}

  ./configure --prefix=/usr \
  	--enable-recursive \
	--mandir=/usr/share/man
  make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}

  make DESTDIR=${pkgdir} install
}