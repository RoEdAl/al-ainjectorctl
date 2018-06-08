# Maintainer: Edmunt Pienkowsky <roed@onet.eu>

pkgname='audio-injector-utils'
pkgdesc='Tools for Audio Injector Stereo Sound Card'
url='http://github.com/RoEdAl/ainjectorctl'
pkgver='1.0'
pkgrel='1'
arch=('any')
license=('GPL')
depends=('alsa-utils')

source=(
    "ainjectorctl-v${pkgver}.tar.gz::http://github.com/RoEdAl/ainjectorctl/archive/v${pkgver}.tar.gz"
)

md5sums=('ad6f5cfe1774350c4accc61703a50268')

package(){

    cd ${srcdir}/ainjectorctl-${pkgver}

    install -d -m 0755 ${pkgdir}/usr/share/audio-injector
    install -p -m 0644 audio-injector-functions.sh ${pkgdir}/usr/share/audio-injector
    install -p -m 0644 README.md ${pkgdir}/usr/share/audio-injector

    install -d -m 0755 ${pkgdir}/usr/bin
    install -p -m 0755 ainjectorctl.sh ${pkgdir}/usr/bin/ainjectorctl
    ln -s 'ainjectorctl' ${pkgdir}/usr/bin/audioinjectorctl 
}
