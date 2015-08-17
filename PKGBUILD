# Maintainer: Antoni Segura Puimedon <antonisp@celebdor.com>
pkgname=sosreport
pkgver=3.0
pkgrel=2
pkgdesc="A set of tools to gather troubleshooting information from a system."
arch=('i686' 'x86_64')
url="https://github.com/sosreport/sosreport"
license=('GPL')
groups=()
depends=()
provides=()
conflicts=()
replaces=()
backup=()
options=(!emptydirs)
install=
source=("https://github.com/sosreport/sosreport/archive/sos-3.0.tar.gz")
sha256sums=('b044bb55d6d6413e89a85dab0ae8b7a174ae5746737c65806584ee6da8495730')
_dirname="$pkgname-sos-$pkgver"

build() {
  cd "$srcdir/$_dirname"
  grep "PYTHON=python" * -R -l | xargs sed -i -e 's/PYTHON=python/PYTHON=python2/'
  make
}

package() {
  cd "$srcdir/$_dirname"
  make DESTDIR=$pkgdir install
}
