# Maintainer: Edmunt Pienkowsky <roed@onet.eu>

pkgname='audio-injector-utils'
pkgdesc='Tools for Audio Injector Stereo Sound Card'
url="http://github.com/RoEdAl/${pkgname}"
pkgver='3.1'
pkgrel='2'
arch=('any')
license=('GPL')
depends=('alsa-utils')
optdepends=('ffmpeg: required by ainjectortest' 'bc: required by ainjectortest')

source=(
    "${pkgname}-v${pkgver}.tar.gz::http://github.com/RoEdAl/${pkgname}/archive/v${pkgver}.tar.gz"
    'audioinjector-init.service'
)

md5sums=('523808983d0aaa580f828eb5bbe680aa'
         '16a87d4efa406e298c8c393ce1705083')

package(){
    cd ${srcdir}/${pkgname}-${pkgver}

    install -d -m 0755 ${pkgdir}/usr/share/audio-injector
    install -p -m 0644 ainjectorctl/audio-injector-functions.sh ${pkgdir}/usr/share/audio-injector

    install -d -m 0755 ${pkgdir}/usr/bin
    install -p -m 0755 ainjectorctl/ainjectorctl.sh ${pkgdir}/usr/bin/ainjectorctl
    ln -s 'ainjectorctl' ${pkgdir}/usr/bin/audioinjectorctl
    install -p -m 0755 ainjectortest/ainjectortest.sh ${pkgdir}/usr/bin/ainjectortest
    ln -s 'ainjectortest' ${pkgdir}/usr/bin/audioinjectortest
    install -p -m 0755 ainjectorchk/ainjectorchk.sh ${pkgdir}/usr/bin/ainjectorchk
    ln -s 'ainjectorchk' ${pkgdir}/usr/bin/audioinjectorchk

    install -d -m 0755 ${pkgdir}/usr/lib/systemd/system
    install -p -m 0644 ${srcdir}/audioinjector-init.service ${pkgdir}/usr/lib/systemd/system
}
