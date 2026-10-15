pkgname=steam-status-tray
pkgver=0.1.0
pkgrel=1
pkgdesc="Tray icon with Steam friends status (Online/Away/Invisible/Offline) and quick links"
arch=('any')
url="https://github.com/CausticCatastrophe/steam-status-tray"
license=('MIT')
depends=('python' 'python-pyqt6' 'steam')
source=('steam-status-tray' 'steam-status-tray.desktop' 'LICENSE')
sha256sums=('SKIP' 'SKIP' 'SKIP')

package() {
  install -Dm755 steam-status-tray "$pkgdir/usr/bin/steam-status-tray"
  install -Dm644 steam-status-tray.desktop \
    "$pkgdir/usr/share/applications/steam-status-tray.desktop"
  install -Dm644 steam-status-tray.desktop \
    "$pkgdir/etc/xdg/autostart/steam-status-tray.desktop"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
