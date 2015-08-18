# Maintainer: David J. Haines <djhaines at gmx dot com>

pkgname=xboomx
pkgver=0.50
pkgrel=1
pkgdesc="dmenu wrapper that sorts based on frequency of usage (like yeganesh, but without all the haskell)"
arch=('i686' 'x86_64')
url="https://bitbucket.org/dehun/xboomx/wiki/Home"
license=('BSD')
groups=()
depends=('dmenu' 'python2')
makedepends=('python2-setuptools')
provides=()
conflicts=()
replaces=()
backup=()
options=(!emptydirs)
install=xboomx.install
source=(https://bitbucket.org/dehun/${pkgname}/get/${pkgver}.tar.bz2)
md5sums=('00a4c4d71ffeb3b9b88b1c8cbc469b51')

build() {
    cd "$srcdir/dehun-xboomx-2fbe9a6f5b38"
    python2 setup.py build
}

package() {
    cd "$srcdir/dehun-xboomx-2fbe9a6f5b38"
    python2 setup.py install --root="$pkgdir/" --optimize=1
    mkdir -p "$pkgdir/usr/share/xboomx"
    cp "$srcdir/dehun-xboomx-2fbe9a6f5b38/etc/config" "$pkgdir/usr/share/xboomx"
}

# vim:set ts=2 sw=2 et:
