# Maintainer: Eike Möhlmann <eike DOT moehlmann AT informatik DOT uni DASH oldenburg DOT de>

pkgname=udev-autoxkbmap
pkgver=2
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

sha256sums=('60bbe2a2e830ef015116be833ca9f619895381a54dc6cea835e2c41e2ccb709e'
            '2db5a9a576a0d98512e8784bc9935d4f1a767792473fce4165139be4795bc887'
            'a1a0d875aa0f76eb22d434f495571cf429ad0e068b1baa402f9f88abccb427f4'
            '13de323c7591cca8c4762a8944f45787390730305da10516fac5f64b5e8ee13c')
