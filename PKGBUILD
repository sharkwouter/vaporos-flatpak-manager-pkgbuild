# Maintainer: Wouter Wijsman <wwijsman@live.nl>
pkgname=vaporos-flatpak-manager
pkgver=2.0
pkgrel=1
pkgdesc="A frontend for flatpak with gamepad support"
arch=('i686' 'x86_64')
url="https://github.com/sharkwouter/vaporos-flatpak-manager"
license=('MIT')
depends=('python-requests' 'python-appdirs' 'python-pygame' 'flatpak' 'ttf-liberation' 'gtk3')
makedepends=('python-setuptools')
optdepends=('ttf-liberation-sans-narrow')
source=("https://github.com/sharkwouter/vaporos-flatpak-manager/archive/2.0-alpha.tar.gz")
md5sums=('6d9af8333ca0e058c4494cef5b2ad8fe')
build() {
        cd "$srcdir/$pkgname-$pkgver-alpha"
        python setup.py build
}
package() {
        cd "$srcdir/$pkgname-$pkgver-alpha"
        python setup.py install --root="$pkgdir" --prefix=/usr --skip-build
}
