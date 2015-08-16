# Contributor: Rustam Tsurik <rustam.tsurik@gmail.com

pkgname=nagiq-demo
_realname=NagiQ-1.0-linux-x86
pkgver=1.0
pkgrel=1

pkgdesc='NagiQ is an attractive, family-friendly word game (demo).'
url='http://www.ikigames.com/nagiq/'
arch=('i686' 'x86_64')

source=('http://www.ikigames.com/demos/NagiQ-1.0-demo-linux-x86.tar.bz2'
        'nagiq-demo.desktop'
        'nagiq-demo')
md5sums=('e1116a7f12489d46ca805fbd3b07715a'
         'd6f493055838f4edc45702d80b0ef700'
         'd64ceafcd99056a7faf80f06f6efbfae')

makedepends=('icoutils')
license=('custom')
options=(!strip)

package() {
    cd ${srcdir}/${_realname}

    icotool -x --index=6 game/icon.ico
    mkdir -p ${pkgdir}/usr/share/icons
    mv icon_6_96x96x32.png ${pkgdir}/usr/share/icons/nagiq-demo.png

    mkdir -p ${pkgdir}/usr/share/applications      
    cp ${srcdir}/nagiq-demo.desktop ${pkgdir}/usr/share/applications/

    mkdir -p ${pkgdir}/usr/bin
    cp ${srcdir}/nagiq-demo ${pkgdir}/usr/bin/
    chmod 755 ${pkgdir}/usr/bin/nagiq-demo

    mkdir -p ${pkgdir}/opt/nagiq-demo
    mv * ${pkgdir}/opt/nagiq-demo/
}
