# Maintainer: Sergey Slipchenko <faergeek@gmail.com>
pkgname=marvo-gt-56
pkgver=0.0.1
pkgrel=1
pkgdesc="Emulate Xbox 360 wireless controller with Marvo GT-56 bluetooth controller"
arch=('any')
license=('GPL')
depends=('xboxdrv')
backup=('etc/marvo-gt-56.xboxdrv')
source=('99-marvo-gt-56.rules'
        'marvo-gt-56@.service'
        'marvo-gt-56.xboxdrv')
md5sums=('8d066afcaa90719bdb48b60352cf8e76'
         'f005986a9cc59f80a315c630617c8dcf'
         'd6240b89f2a9dc95dc9f4c5d91a4d503')

package() {
  mkdir -p "${pkgdir}/usr/lib/udev/rules.d"
  install -Dm 644 "${srcdir}/99-marvo-gt-56.rules" "${pkgdir}/usr/lib/udev/rules.d/"

  mkdir -p "${pkgdir}/usr/lib/systemd/system/"
  install -Dm 644 "${srcdir}/marvo-gt-56@.service" "${pkgdir}/usr/lib/systemd/system/"

  mkdir -p "${pkgdir}/etc"
  install -Dm 644 "${srcdir}/marvo-gt-56.xboxdrv" "${pkgdir}/etc/"
}
