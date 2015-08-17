# Maintainer: Andreas Mielke <arch@amielke.de>
pkgname=uex-4.0.0.7
pkgver=4.0.0.7
pkgrel=1
pkgdesc="UltraEdit is a powerful text editor."
arch=('i686' 'x86_64')
url="http://www.ultraedit.com/products/uex.html"
license=('custom')
if [[ $CARCH == i686 ]]; then
  depends+=('atk' 'cairo' 'desktop-file-utils' 'expat' 'fontconfig' 'freetype2' 'gdk-pixbuf2' 'glib2' 'graphite' 'gtk2' 'harfbuzz' 'icu' 'libffi'
         'libice' 'libpng' 'libpng12' 'libsm' 'libx11' 'libxau' 'libxcb' 'libxcomposite' 'libxcursor'
         'libxdamage' 'libxdmcp' 'libxext' 'libxfixes' 'libxi' 'libxinerama' 'libxml2'
         'libxrandr' 'libxrender' 'pango' 'pcre' 'pixman' 'xz' 'zlib')
else
  depends+=('atk' 'cairo' 'desktop-file-utils' 'expat' 'fontconfig' 
	 'freetype2' 'gdk-pixbuf2' 'glib2' 'graphite' 'gtk2' 'harfbuzz' 'icu' 'libffi'
         'libice' 'libpng' 'libpng12' 'libsm' 'libx11' 'libxau' 'libxcb' 'libxcomposite' 'libxcursor'
         'libxdamage' 'libxdmcp' 'libxext' 'libxfixes' 'libxi' 'libxinerama' 'libxml2'
         'libxrandr' 'libxrender' 'pango' 'pcre' 'pixman' 'xz' 'zlib')
fi
install=uex.install
if [[ $CARCH == i686 ]] ; then
  source=(http://www.ultraedit.com/files/uex/Other/uex-${pkgver}_i386.tar.gz)
  md5sums=('d41d8cd98f00b204e9800998ecf8427e')
else
  source=(http://www.ultraedit.com/files/uex/Other/uex-${pkgver}_amd64.tar.gz)
  md5sums=('4e5a8d0414dfcafbb2da68162e62606a')
fi

package() {
  install -d "${pkgdir}/opt" "${pkgdir}/usr/bin" "${pkgdir}/usr/share/pixmaps" "${pkgdir}/usr/share/applications" "${pkgdir}/usr/share/licenses/${pkgname}"

  cp -R "${srcdir}/uex" "${pkgdir}/opt"
  ln -s "/opt/uex/bin/uex" "${pkgdir}/usr/bin/uex"
  ln -s "/opt/uex/share/uex/ue.png" "${pkgdir}/usr/share/pixmaps/ue.png"
  ln -s "/opt/uex/share/uex/uex.desktop" "${pkgdir}/usr/share/applications/uex.desktop"
  ln -s "/opt/uex/share/doc/uex/copyright" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

