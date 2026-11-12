# err Android distribution

Public distribution for the **err** Android app. The application source
repository is private; this repository only hosts release artifacts and the
ZapStore metadata.

- Website: <https://err.tokyo>
- Downloads: see the [Releases](https://github.com/1l0/err-releases/releases)
  tab.
- ZapStore: <https://zapstore.dev/apps/tokyo.err.app>

Each APK is signed with the same release certificate used for the ZapStore
listing. Do not install builds from other sources.

## Camera and QR scanning

err uses the camera only to scan a pairing QR code in the encrypted QR sync
flow. It does not take photos or record video. The scanner is the Flutter
`mobile_scanner` plugin, which uses ML Kit barcode scanning
(`com.google.mlkit`). Decoding runs on the device; camera frames are not sent
anywhere.
