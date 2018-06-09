# Maintainer: Edmunt Pienkowsky <roed@onet.eu>

pkgname='audio-injector-utils'
pkgdesc='Tools for Audio Injector Stereo Sound Card'
url='http://github.com/RoEdAl/ainjectorctl'
pkgver='2.0'
pkgrel='1'
arch=('any')
license=('GPL')
depends=('alsa-utils')
optdepends=('ffmpeg: required by ainjectortest' 'bc: required by ainjectortest')

source=(
    "${pkgname}-v${pkgver}.tar.gz::http://github.com/RoEdAl/${pkgname}/archive/v${pkgver}.tar.gz"
)

md5sums=('50bc29eb9d098bb379a343d9987cbbba')

package(){
    cd ${srcdir}/${pkgname}-${pkgver}

    install -d -m 0755 ${pkgdir}/usr/share/audio-injector
    install -p -m 0644 ainjectorctl/audio-injector-functions.sh ${pkgdir}/usr/share/audio-injector

    install -d -m 0755 ${pkgdir}/usr/bin
    install -p -m 0755 ainjectorctl/ainjectorctl.sh ${pkgdir}/usr/bin/ainjectorctl
    ln -s 'ainjectorctl' ${pkgdir}/usr/bin/audioinjectorctl
    install -p -m 0755 ainjectortest/ainjectortest.sh ${pkgdir}/usr/bin/ainjectortest
    ln -s 'ainjectortest' ${pkgdir}/usr/bin/audioinjectortest
}
