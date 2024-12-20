pkgname=gruvbox-dark-gtk4
pkgver=1.0.0
pkgrel=1
pkgdesc='A gruvbox dark theme. Supports GTK 2.0, 3.0 and sort of 4.0.'
conflicts=(gruvbox-dark-gtk)
arch=('any')
url="https://github.com/m-pasik/gruvbox-dark-gtk4"
license=('GPL3')
source=("$pkgname-$pkgver.tar.gz::https://github.com/m-pasik/gruvbox-dark-gtk4/archive/v$pkgver.tar.gz")
sha256sums=('cad3f19495a13cacace355e94bf2b966a68bcffbe09b3eecb86a527150d77f87')

package() {
    mkdir -p "$pkgdir/usr/share/themes/gruvbox-dark-gtk"
    cd "$srcdir/$pkgname-$pkgver"
    cp -r "gtk-2.0" \
        "gtk-3.0" \
        "gtk-3.20" \
        "gtk-4.0" \
        "assets" \
        "unity" \
        "xfwm4" \
        "metacity-1" \
        "cinnamon" \
        "index.theme" \
        "$pkgdir/usr/share/themes/gruvbox-dark-gtk"
    chown -R root:root "$pkgdir/usr/share/themes"
    chmod -R ugo+rX "$pkgdir/usr/share/themes"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
