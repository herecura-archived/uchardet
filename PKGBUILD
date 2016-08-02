# Maintainer: Blake Imsland <blake@retroco.de>

pkgname=uchardet
pkgver=0.0.6
pkgrel=1
pkgdesc="An encoding detector library"
arch=('i686' 'x86_64')
url="https://www.freedesktop.org/wiki/Software/uchardet"
license=('MPL')
makedepends=('cmake')
source=("https://www.freedesktop.org/software/$pkgname/releases/$pkgname-$pkgver.tar.xz")
sha256sums=('8351328cdfbcb2432e63938721dd781eb8c11ebc56e3a89d0f84576b96002c61')

build() {
    cd "$pkgname-$pkgver"
    cmake \
        -DCMAKE_INSTALL_PREFIX=/usr \
        -DCMAKE_INSTALL_LIBDIR=lib \
        -DCMAKE_BUILD_TYPE=Release
    make
}

check() {
    cd "$pkgname-$pkgver"
    #make -k check
}

package() {
    cd "$pkgname-$pkgver"
    make DESTDIR="$pkgdir/" install
}
