# Maintainer: Your Name <youremail@domain.com>
pkgname=teip-bin
pkgver=2.2.0
pkgrel=1
pkgdesc="Select partial standard input and replace with the result of another command efficiently"
arch=('x86_64')
url="https://github.com/greymd/teip"
license=('MIT')
source=("https://github.com/greymd/teip/releases/download/v$pkgver/teip-$pkgver.$CARCH-unknown-linux-musl.tar.gz")
sha256sums=('a41b64ec72d459cf90c845efc795c1e37c83f70a1f24e001065280a4bbb109c9')

package() {
	install -m 755 -D "$srcdir/bin/teip" "$pkgdir/usr/bin/teip"
	install -m 755 -D "$srcdir/man/teip.1" "$pkgdir/usr/share/man/man1/teip.1"
	if [ -d "/usr/share/zsh/functions/Completion/Linux" ]; then
		install -m 755 -D "$srcdir/completion/zsh/_teip" "$pkgdir/usr/share/zsh/functions/Completion/Linux/_teip"
	fi
}

