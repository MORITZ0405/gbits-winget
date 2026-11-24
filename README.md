# gbits-winget

Hält das winget-Paket [`MT-Media.gbits`](https://github.com/microsoft/winget-pkgs/tree/master/manifests/m/MT-Media/gbits) aktuell.

Die Action `.github/workflows/winget.yml` schaut stündlich auf `https://gbits.eu/api/win/version`.
Liegt dort ein neuerer Windows-Installer als in winget, reicht sie per `wingetcreate update` einen
Pull Request bei microsoft/winget-pkgs ein. Installer-Adresse: `https://gbits.eu/download/gbits-setup-<Version>.exe`.

Secret `WINGET_TOKEN`: klassischer GitHub-Token mit Scope `public_repo`.
Das Repo ist öffentlich, weil GitHub Actions dort kostenlos sind.
