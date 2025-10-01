# Maintainer: ZeStig <zestig@duck.com>
pkgname=stratos-calamares-config-next
pkgver=1.0
pkgrel=3
pkgdesc="New StratOS Calamares config for online installations"
arch=('x86_64')
url="https://github.com/StratOS-Linux/StratOS-calamares-config-next"
license=('GPL')
depends=(
	'bash'
	'libpwquality'
)
source=()
install=stratos-calamares-config.install

prepare() {
    cp -r "$startdir/branding" "$srcdir/"
    cp -r "$startdir/modules" "$srcdir/"
    install -m 644 "$startdir/settings.conf" "$srcdir/"
}
package() {
    install -d "$pkgdir/etc/calamares"
    cp -r "$srcdir/branding" "$pkgdir/etc/calamares/"
    cp -r "$srcdir/modules" "$pkgdir/etc/calamares/"
    install -m 644 "$srcdir/settings.conf" "$pkgdir/etc/calamares/"
}
