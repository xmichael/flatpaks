# About
A collection of Flatpak manifest files for certain apps that are not normally included in GNU/Linux distributions.

This is useful for deploying a third-party package using something that looks like BSD Ports or Arch's PKGBUILD with a sandbox.

Of course, one would look at flathub first to see if the there is a package already available.

## Example

The following command will read the manifest file to download and build Munt32_qt from scratch on a new local repository `my-repo`:

```bash
flatpak-builder --repo=myrepo --force-clean build-dir ./net.sourceforge.munt.Munt32emu.yaml
# Enable repo
flatpak --user remote-add --no-gpg-verify my-repo ./myrepo
# run the app
flatpak run --user net.sourceforge.munt.Munt32emu
```
