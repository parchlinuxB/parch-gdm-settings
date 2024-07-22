pkgname=parch-gdm-settings
pkgver=0.1
pkgrel=4
pkgdesc="Parch settings and theme for gdm"
arch=('any')
url="https://github.com/parchlinuxb/parch-gdm-settings"
license=("GPL-3.0")
depends=("gnome-parch")
source=("rootfs.zip")
sha256sums=('SKIP')


package() {
    cp -r * $pkgdir
    chmod 544 /usr/share/gnome-shell/gnome-shell-theme.gresource
    chmod 544 /etc/dconf/db/gdm.d/95-parch-gdm-config
    chmod 544 /etc/gdm/gdm-login-logo
}

post_install(){
    cp /usr/share/gnome-shell/gnome-shell-theme.gresource /usr/share/gnome-shell/gnome-shell-theme.gresource.old
    mv /usr/share/gnome-shell/parch-gnome-shell-theme.gresource  /usr/share/gnome-shell/gnome-shell-theme.gresource 
    chmod 544 /usr/share/gnome-shell/gnome-shell-theme.gresource
    chmod 544 /etc/dconf/db/gdm.d/95-parch-gdm-config
    chmod 544 /etc/gdm/gdm-login-logo
}

pre_remove(){
    mv /usr/share/gnome-shell/gnome-shell-theme.gresource.old /usr/share/gnome-shell/gnome-shell-theme.gresource
}