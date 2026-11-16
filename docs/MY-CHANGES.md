# My changes (zezo20234/couch)

* **Ports.** The Ports button (top right of the home, next to the moon) opens a menu of the TV's
  HDMI ports. Pick one to switch to it. **Rename ports** opens Home settings, Ports, where each port
  can be given a name you know ("PlayStation 5", "Soundbar"). Names are kept on the TV. If the TV
  doesn't list its inputs, four stand-in ports (HDMI 1 to 4) show instead; picking one opens the
  TV's own input list. "Use the TV's own names" undoes every rename.
* **Delete this launcher.** Home settings, About, the red button at the bottom. Press OK twice, then
  confirm in Android's own remove screen. The TV's own home comes back.
* **Updates.** Home settings, Updates, "Check for updates now" reads the newest release of
  https://github.com/zezo20234/couch/releases and offers "Update to ..." when it is newer. Android asks
  before it installs. Settings stay.
* **Releases.** `.github/workflows/build.yml` builds the TV home on every push and, on the main
  branch, publishes `couch-tv-home.apk` as a release (tag `v0.12.<run number>`). Every release is
  signed with the key in `.github/signing/couch.keystore.b64` so a TV can update from the one before.
  Do not rename `couch-tv-home.apk`: the Update button looks for that name.

An APK already on the TV that was signed with a different key (the original project's releases, or a
test build from another computer) can't be updated by these releases. Remove it first (Settings, Apps)
and install the first release from this repo.
