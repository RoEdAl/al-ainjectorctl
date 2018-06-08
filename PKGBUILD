# Maintainer: Edmunt Pienkowsky <roed@onet.eu>

pkgname='ainjectorctl'
pkgdesc='ainjectorctl - mixer tool for Audio Injector Stereo Sound Card for Raspberry Pi'
url='http://github.com/RoEdAl/ainjectorctl'
pkgver='1.0'
pkgrel='1'
arch=('any')
license=('GPL')
depends=('alsa-utils')

source=(
    "${pkgname}-v${pkgver}.tar.gz::http://github.com/RoEdAl/ainjectorctl/archive/v${pkgver}.tar.gz"
)

md5sums=('ad6f5cfe1774350c4accc61703a50268')

package(){

    cd ${srcdir}/${pkgname}-${pkgver}

    install -d -m 0755 ${pkgdir}/usr/share/audio-injector
    install -p -m 0644 audio-injector-functions.sh ${pkgdir}/usr/share/audio-injector
    install -p -m 0644 README.md ${pkgdir}/usr/share/audio-injector

    install -d -m 0755 ${pkgdir}/usr/bin
    install -p -m 0755 ainjectorctl.sh ${pkgdir}/usr/bin/ainjectorctl
    ln -s 'ainjectorctl' ${pkgdir}/usr/bin/audioinjectorctl 
}
