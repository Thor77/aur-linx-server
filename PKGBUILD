# Maintainer: Thor77 <thor77 at thor77 dot org>
# Contributor (backup): Thomas Fanninger <thomas at fanninger dot at>

pkgname=linx-server
pkgver=2.2.3
pkgrel=1
pkgdesc='Self-hosted file/code/media sharing website '
arch=('i686' 'x86_64' 'arm')
url='https://github.com/andreimarcu/linx-server'
license=('GPL3')
install=linx-server.install
options=('!strip')
noextract=('linx-server')
backup=('etc/webapps/linx-server/config.ini')

source=('linx-server.service' 'config.ini')
md5sums=('ff2e46fa6491fb58f24294e037092799'
         '8c2fe5caef5e0477d0da15cc0d947337')
md5sums_i686=('558cb4c08a89cf2ec8e223d2bbdf3924')
md5sums_x86_64=('5ea957c64a3312c9a2b0ff0e435afddd')
md5sums_arm=('3f49adb6d2f215628c8058d080d5c3c6')

source_i686=("linx-server::https://github.com/andreimarcu/linx-server/releases/download/v$pkgver/linx-server-v${pkgver}_linux-386")
source_x86_64=("linx-server::https://github.com/andreimarcu/linx-server/releases/download/v$pkgver/linx-server-v${pkgver}_linux-amd64")
source_arm=("linx-server::https://github.com/andreimarcu/linx-server/releases/download/v$pkgver/linx-server-v${pkgver}_linux-arm")


package() {
  cd $srcdir
  install -Dm755 linx-server "$pkgdir/usr/bin/linx-server"
  install -Dm644 config.ini "$pkgdir/etc/webapps/linx-server/config.ini"
  install -Dm644 linx-server.service "$pkgdir/usr/lib/systemd/system/linx-server.service"
  install -d "$pkgdir/usr/share/webapps/linx-server/"
}
