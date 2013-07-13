# Maintainer: sputnikus <mputniorz at gmail a-dot com>

pkgname=synopsitv-scrobbler
pkgver=1.0
pkgrel=1
pkgdesc="Synopsi TV desktop application allows you to keep track of your watched movies, rate them and checkin to http://synopsi.tv as you're watching them."
arch=('i686' 'x86_64')
url="http://features.synopsi.tv/scrobbler/"
license=('unknown')
groups=('multimedia')
depends=('libappindicator' 'libdrm' 'mesa-libgl' 'glib2' 'gstreamer0.10-base-plugins' 'xz' 'orc' 'sqlite' 'libx11' 'libxcomposite' 'libxext' 'libxrender' 'libxslt')
provides=("synopsitv-scrobbler=$pkgver")
replaces=("synopsitv-scrobbler")
_arch=i386
[ "$CARCH" = 'x86_64' ] && _arch=amd64
source=("scrobbler-1.0.${_arch}.deb::https://s3.amazonaws.com/download.synopsi.tv/scrobbler-1.0.${_arch}.deb")
md5sums=('1dc0473202812200fbef7ace6ac8d5cf')
[ "$CARCH" = 'x86_64' ] && md5sums[0]='a2642fedee205462e250e3d28e441523'

PKGEXT='.pkg.tar'

package() {
    msg2 "Extracting the data.tar.gz"
    bsdtar -xf data.tar.gz -C "$pkgdir/"

    chmod 755 "$pkgdir"/opt/SynopsiTV/Scrobbler/scrobbler
}
