# edg-l's Gentoo Overlay

Personal Gentoo overlay for my own projects and software I use that isn't in the main tree.

## Packages

| Package | Description |
|---------|-------------|
| `app-crypt/fidorium` | FIDO2/CTAP2 authenticator daemon backed by TPM2 |

## Usage

Add the overlay with `eselect-repository` (recommended):

```bash
eselect repository add edg-l git https://github.com/edg-l/gentoo-overlay
```

Or manually create `/etc/portage/repos.conf/edg-l.conf`:

```ini
[edg-l]
location = /var/db/repos/edg-l
sync-type = git
sync-uri = https://github.com/edg-l/gentoo-overlay
auto-sync = yes
```

Then sync and install:

```bash
emerge --sync edg-l
emerge app-crypt/fidorium
```

## License

The ebuild and overlay infrastructure are licensed under the AGPL-3.0.
Packages retain their own upstream licenses.
