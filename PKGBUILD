# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>
_gitname=mkcal
pkgname=mkcal6
pkgver=1.7.26
pkgrel=1
pkgdesc="SQlite storage backend for KCalendarCore"
arch=('x86_64' 'aarch64')
url="https://github.com/neochapay/${_gitname}"
license=('BSD-3-Clause')
depends=('kcalendarcore>=6.0' 'timed')
makedepends=('cmake' 'extra-cmake-modules>=6.0')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('ea8782a10be1debdc09b01769e5eaa3f0f86c01c1a31aa45e15efa37f912be62')

build() {
    cd ${_gitname}-$pkgver
    cmake -DCMAKE_INSTALL_PREFIX:PATH='/usr' .
    make  all
}

package() {
    cd ${_gitname}-$pkgver
    make DESTDIR="$pkgdir" install
}
