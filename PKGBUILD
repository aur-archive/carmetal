# Contributor: moostik <mooostik_at_gmail.com>
# Contributor: Jean-Christophe Imbert <imbert@crans.org>
# Maintainer: Stefan Husmann <stefan-husmann@t-online.de>

pkgname=carmetal
pkgver=3.8.5
pkgrel=1
url="http://db-maths.nuxit.net/CaRMetal/"
pkgdesc="A dynamic geometry program using the C.a.R. engine"
arch=('any')
license=('GPL')
depends=('java-environment' 'desktop-file-utils' 'hicolor-icon-theme' 'shared-mime-info')
install=carmetal.install
source=($pkgname-$pkgver.zip::http://db-maths.nuxit.net/CaRMetal/download/src.zip
	${pkgname}.sh
	${pkgname}.desktop
	${pkgname}.png
	${pkgname}.xml
	application-x-${pkgname}.png)
md5sums=('3cbc822e388c86713b0c826db5ab1752'
         'e312ac3a26be3dde1125ab48311c7401'
         'a3fde4cca7750a8c39d2d13f6737384f'
         'ea61df10e0fdd8dfe999c4052663fba5'
         '58e62164346bc3de85e86a0025cd0a3c'
         '11fa5b737f6e76cff5d0cff27ea5b8d0')

package() {
	cd "${srcdir}"
	install -d ${pkgdir}/usr/share/java/${pkgname}
	install -Dm644 CaRMetal.jar *.mcr $pkgdir/usr/share/java/${pkgname}
	install -d $pkgdir/usr/share/pixmaps
	install -Dm644 ${pkgname}.png $pkgdir/usr/share/pixmaps/${pkgname}.png
	install -Dm755 ${pkgname}.sh $pkgdir/usr/bin/${pkgname}
	install -Dm644 ${pkgname}.desktop $pkgdir/usr/share/applications/${pkgname}.desktop
	install -Dm644 application-x-$pkgname.png \
	  $pkgdir/usr/share/icons/hicolor/48x48/mimetypes/application-x-$pkgname.png
	install -Dm644 $srcdir/$pkgname.xml $pkgdir/usr/share/mime/packages/$pkgname.xml
} 
