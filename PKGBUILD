pkgname=steam-status-tray
pkgver=0.3.1
pkgrel=1
pkgdesc="Steam tray icon with Online/Away/Invisible/Offline, recent games, quick links and a fix for hidden chat windows"
arch=('any')
url="https://github.com/CausticCatastrophe/steam-status-tray"
license=('MIT')
depends=('python' 'python-pyqt6' 'steam')
install=steam-status-tray.install
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
