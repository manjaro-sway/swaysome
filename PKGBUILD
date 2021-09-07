# Maintainer: Jonas Strasel <info@jonas-strassel.de>

pkgname="swaysome"
pkgver=1.1.0
pkgrel=0
pkgdesc="This binary helps you configure sway to work a bit more like Awesome. This currently means workspaces that are name-spaced on a per-screen basis." 
arch=("x86_64" "aarch64")
url="https://git.hya.sk/skia/$pkgname"
license=("none")
makedepends=("rust" "cargo" "git")
_commit="60fdf90d4d4ab075b4eb4121c09ea9ef855df109"
source=("$pkgname-$pkgver.tar.gz::$url/archive/$pkgver.tar.gz")
sha256sums=('20b9ced1440cd604444a7e89ee1568847e7a075312398777b35374564fce7b38')

build() {
    cd "$srcdir/$pkgname"
    cargo build --release --locked 
}

package() {
    install -D -m755 "$srcdir/$pkgname/target/release/$pkgname" "$pkgdir/usr/bin/$pkgname"
    install -D -m644 "$srcdir/$pkgname/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
