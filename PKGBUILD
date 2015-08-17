# Maintainer: Florian Léger <florian6 dot leger at laposte dot net>

_appname=mplayer.py
pkgname=python-"${_appname}"
pkgver=0.7.0
pkgrel=2
pkgdesc="Lightweight and dynamic MPlayer wrapper with a Pythonic API"
arch=('any')
url="http://code.google.com/p/python-mplayer/"
license=('LGPL')
depends=('mplayer' 'python')
makedepends=('python-distribute')
optdepends=('python-pyqt: for Qt integation')
source=("http://pypi.python.org/packages/source/${_appname::1}/${_appname}/${_appname}-${pkgver}.tar.gz")
md5sums=('8440abf66111b3c5437b32e896b0c44e')

build() {
  cd "${srcdir}/${_appname}-${pkgver}"

  python setup.py build
}

package() {
  cd "${srcdir}/${_appname}-${pkgver}"

  python setup.py install -O1 --root="${pkgdir}"
}
