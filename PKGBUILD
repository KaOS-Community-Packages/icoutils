pkgname=icoutils
pkgver=0.31.0
pkgrel=1
pkgdesc='Extracts and converts images in MS Windows(R) icon and cursor files.'
arch=('x86_64')
license=('GPL')
url='http://www.nongnu.org/icoutils/'
depends=('libpng>=1.0.0' 'perl-libwww>=5.64')
source=("http://savannah.nongnu.org/download/${pkgname}/${pkgname}-${pkgver}.tar.bz2")
md5sums=('fe12dcfb7796cb6cb4ac9bb0720ae362')

build() {
  cd ${pkgname}-${pkgver}
  ./configure \
    --prefix=/usr \
    --mandir=/usr/share/man
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install
}
