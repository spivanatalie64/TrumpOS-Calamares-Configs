# Maintainer: Natalie <natalie@sprungles.org>
pkgname=trumpos-calamares-configs
pkgver=1.0.0
pkgrel=1
pkgdesc="Official Calamares configuration for TrumpOS - Making Computing Great Again"
arch=('any')
url="https://github.com/spivanatalie64/TrumpOS-Calamares-Configs"
license=('GPL')
depends=('calamares')
source=("trumpos-calamares-configs::git+https://github.com/spivanatalie64/TrumpOS-Calamares-Configs.git")
md5sums=('SKIP')

package() {
  # Create destination directory
  install -dm755 "$pkgdir/etc/calamares"

  # Copy all configuration files and assets
  # Using cp -a to maintain permissions and directory structure
  cp -a "$srcdir/trumpos-calamares-configs/etc/calamares/"* "$pkgdir/etc/calamares/"

  # Install the launch script if it exists in the root (though currently it is in etc/calamares)
  if [ -f "$srcdir/trumpos-calamares-configs/etc/calamares/launch.sh" ]; then
    chmod +x "$pkgdir/etc/calamares/launch.sh"
  fi
}
