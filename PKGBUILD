pkgname=ntrischi-slock
_pkgname=slock
pkgver=aae4107
pkgrel=1
pkgdesc="A simple screen locker for X"
arch=('i686' 'x86_64')
url="https://github.com/ntrischi/slock"
license=('MIT')
depends=('libxext')
makedepends=('git')
source=('https://github.com/ntrischi/slock/tarball/master')
md5sums=('f56598a108c5bd458a93a9a655159d0b')

pkgver() {
	cd "$pkgname"-*
	git describe --always | sed 's|-|.|g'
}

build() {
	cd "$pkgname"-*
	make
}

package() {
	cd "$pkgname"-*
	make DESTDIR="$pkgdir" install
	install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
