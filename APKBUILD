
pkgname=firmware-xiaomi-kenzo
pkgver=2
pkgrel=0
pkgdesc="Firmware for Xiaomi Redmi Note 3 Pro"
url="https://github.com/Kiciuk/proprietary_firmware_kenzo"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
_commit="89e0772d837d030d10af1c4c0cf459af6d0dc446"
source="https://github.com/Kiciuk/proprietary_firmware_kenzo/archive/$_commit.zip"
builddir="$srcdir/proprietary_firmware_kenzo-$_commit"

_fwdir="/lib/firmware/postmarketos"

package() {
	# parent package is empty
	mkdir -p "$pkgdir"

	# modem firmware
	install -Dm644 modem/mba.mbn -t "$pkgdir/$_fwdir"
	install -Dm644 modem/modem.* -t "$pkgdir/$_fwdir"

	# WiFi/BT firmware
	install -Dm644 apnhlos/wcnss.* -t "$pkgdir/$_fwdir"
	install -Dm644 firmware/wlan/prima/WCNSS_qcom_wlan_nv.bin -t "$pkgdir/$_fwdir"/wlan/prima

	# ADSP firmware
	install -Dm644 modem/adsp.* -t "$pkgdir/$_fwdir"

}

sha512sums="
ba6fb633e7dd0db24d7ef0011f8aad600364acc8f7e4f4edbae6f16b98d0ec686fbfe765e032fc8b78e2ce67a310c799f1eea6724add540f1357fde8b184b376  89e0772d837d030d10af1c4c0cf459af6d0dc446.zip
"
