# Maintainer: Eike Möhlmann <eike DOT moehlmann AT informatik DOT uni DASH oldenburg DOT de>

pkgname=udev-autoxkbmap
pkgver=1
pkgrel=1
pkgdesc='Udev rules to run autoxkbmap after usb keyboard hotplug.'
arch=(any)
url='TODO'
license=(GPL)
depends=(udev libusb)

source=(
		10-keyboard-hotplug.rules
		autoxkbmap
		autoxkbmap.desktop
		autoxkbmap.service
)

package() {
  install -m755 -d "${pkgdir}/etc/xdg/autostart"
  install -m755 -d "${pkgdir}/usr/lib/udev/rules.d"
  install -m755 -d "${pkgdir}/usr/bin"
  install -m755 -d "${pkgdir}/usr/lib/systemd/system"

  install -m644 "${srcdir}/10-keyboard-hotplug.rules" "${pkgdir}/usr/lib/udev/rules.d/"
  install -m644 "${srcdir}/autoxkbmap.service" "${pkgdir}/usr/lib/systemd/system"
  install -m644 "${srcdir}/autoxkbmap.desktop" "${pkgdir}/etc/xdg/autostart"
  install -m755 "${srcdir}/autoxkbmap" "${pkgdir}/usr/bin/"
}
md5sums=('4aae06c35e5cc581f7d3356578c355b3'
         'db946c948b02b1dd683b9531013cfa0e'
         'ce5bdd3f8e95653a872f39ff7aa87383'
         'e38423541e594c9fd100141688bd2031')
