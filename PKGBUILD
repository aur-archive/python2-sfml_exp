# Maintainer: Nick Kavalieris <ph4ntome@gmail.com>
pkgname=python2-sfml_exp
pkgver=1.3
pkgrel=2
pkgdesc="An experimental build for unofficial Python binding for SFML"
arch=('i686' 'x86_64')
url="http://python-sfml.org"
license=('LGPL')
depends=('sfml' 'python2')
conflicts=('python2-sfml2' 'python2-sfml')
makedepends=('cython2')
source=("https://launchpad.net/ubuntu/trusty/+source/python-sfml/1.5.1.is.1.3+dfsg-1build2/+files/python-sfml_1.5.1.is.1.3+dfsg.orig.tar.xz")
md5sums=('e1aa84bcd42227fc06c32b5cbbcf6399')

build() {
	cd "$srcdir"/"python-sfml"-"$pkgver"
	python2 setup.py build_ext
}

package() {
	cd "$srcdir"/"python-sfml"-"${pkgver}"
	python2 setup.py install --root="${pkgdir}" --prefix=/usr
	install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
