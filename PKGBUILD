# Maintainer: Eike Möhlmann <eike DOT moehlmann AT informatik DOT uni DASH oldenburg DOT de>

pkgname=udev-autoxkbmap
pkgver=2
pkgrel=2
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
            'fa7ce174dc7919cfd90d7f0648e4959ce1d28d96a93a588cd97cbed86fdbb9d1'
            'a1a0d875aa0f76eb22d434f495571cf429ad0e068b1baa402f9f88abccb427f4'
            '13de323c7591cca8c4762a8944f45787390730305da10516fac5f64b5e8ee13c')
