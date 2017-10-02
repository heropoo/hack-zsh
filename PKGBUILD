#Maintainer: Heropoo <aiyouyou1000@163.com>

_pkgname='Hack-zsh'
pkgname=hack-zsh
pkgver=1.0.0
pkgrel=1
pkgdesc='A hack zsh config'
arch=(any)
license=(GPL)
depends=('zsh')
install="hack-zsh.install"
url="https://github.com/heropoo/hack-zsh"
#source=("git+https://github.com/heropoo/hack-zsh#branch=master")
source=("zshrc" "keephack")	
sha256sums=("dea99639a48e81e2825452e6a9383d56f4850e4404644858bfad382dcd42aa01"
	"b679b26d5cb65d61108b45c9600307fd56e1d0090a41463fc7f7cd8b8c3bdc10"
)
	
package() {
	mkdir -p "${pkgdir}/etc/zsh/"
	rm -f "${pkgdir}/etc/zsh/zshrc"
	cp -f "${srcdir}/zshrc" "${pkgdir}/etc/zsh/"
	rm -f "${pkgdir}/etc/zsh/keephack"
	cp -f "${srcdir}/keephack" "${pkgdir}/etc/zsh/"

	mkdir -p "${pkgdir}/etc/skel/"
	rm -f "${pkgdir}/etc/skel/zshrc"
	cp -f "${srcdir}/zshrc" "${pkgdir}/etc/skel/.zshrc"

	mkdir -m 700 -p "${pkgdir}/${HOME}/"
	rm -f "${pkgdir}/${HOME}/.zshrc"
	cp -f "${srcdir}/zshrc" "${pkgdir}/${HOME}/.zshrc"
}
