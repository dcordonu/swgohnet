# Maintainer: dcordonu <radagast_thebrown at pm dot me>
pkgname=swgohnet
pkgver=2.0.1
pkgrel=1
pkgdesc="Client for swgohNet - api.swgoh.help updating network"
arch=('x86_64')
url="https://api.swgoh.help/swgohNet"
license=('MIT')
options=('!strip')
install=${pkgname}.install
source=('swgohnet.service' 'swgohnet.conf' 'swgohnet.install'
'https://raw.githubusercontent.com/r3volved/api-swgohNet/master/x64/tar-gz/swgohNet_Client-linux.tar.gz')
md5sums=('7c22eefff28ff07f68ae082dc2ce0014'
         '3654527dfc37a9a99a3bd6065080757b'
         '5a650db1c23d75f1bb454a071e0a5b5c'
         '05a8b8c849951f73987c338137f7980b')

package() {
	install -D "${srcdir}/swgohNet_Client-linux" "${pkgdir}/usr/bin/${pkgname}"
	install -d "${pkgdir}/etc/swgohnet/"
	install -Dm644 swgohnet.service "${pkgdir}/usr/lib/systemd/system/swgohnet.service"
	install -Dm644 swgohnet.conf "${pkgdir}/etc/swgohnet/swgohnet.conf"	
	chmod 755 "${pkgdir}/usr/bin/${pkgname}"
}
