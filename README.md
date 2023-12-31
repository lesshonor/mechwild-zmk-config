# MechWild's User Config Repo (WIP)

(If you're reading this, fork at your own risk. There *will* be rebasing until this repo gets closer to "done".)

## Instructions

### Brand new to ZMK?

1. You will need to [sign up for a GitHub account](https://github.com/signup), and [fork this repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository) so you can edit it.
2. Navigate to the **Actions** tab and click the "I understand my workflows, go ahead and run them" button to enable builds.
   ![Actions tab with "I understand my workflows" button](https://i.imgur.com/B7cTAE6.png)
3. (**TODO:** Genericized instructions.)
4. After committing your changes, your firmware will begin compiling. Assuming there are no typos or other problems, it will eventually be [downloadable from the Actions tab](https://zmk.dev/docs/user-setup#installing-the-firmware).
5. [Flash the firmware](https://zmk.dev/docs/user-setup#flashing-uf2-files) that matches the board and/or shield you're using, e.g. `bb40-pillbug-zmk.uf2` for a PillBug.

### Already have a ZMK user config repo?

The keymaps here may still be useful, but you probably want to [add the `mechwild-zmk-keyboards` ZMK module](https://github.com/lesshonor/mechwild-zmk-keyboards) to your existing `west` manifest instead.

## Common Questions/Problems

### TODO

- Decide what information is important and stable/permanent enough to be linked here since users may never receive updates to this file
- Definitely link back to the module repo for specific keyboard or feature caveats as those WILL change

### There was an error and the build didn't finish.

#### There is probably an error in your keymap.

Carefully double-check the last changes you made. ZMK syntax is very different from QMK syntax. Note that when editing keymaps, each ZMK code is generally preceded by a reference categorizing what that code does.

For example: the letter "Z" is categorized as a **k**ey **p**ress. To add the letter "Z" to a keymap, it must be written `&kp Z`.

You may wish to try [nickcoutsos's in-browser keymap editor](https://nickcoutsos.github.io/keymap-editor), which provides a GUI for editing keymap files in your browser. (Bear in mind that you will still need to compile and flash the resultant firmware; this utility does not change your keymap on the fly à la VIA/Vial/Remap.)

### After disconnecting the keyboard from Bluetooth, it won't reconnect.

#### Forget the Bluetooth connection on both the keyboard and the host, then try re-pairing.

If you don't remember which profile on the keyboard was used to connect to a specific host, you may have to clear them all. [See ZMK's documentation for more information on how to do this.](https://zmk.dev/docs/behaviors/bluetooth#bluetooth-pairing-and-profiles).

As a last resort, try flashing the `settings_reset` firmware for your board; this will force-clear everything.

## Further Troubleshooting Resources

- [ZMK's troubleshooting page](https://zmk.dev/docs/troubleshooting)
- Stop by #keyboard-help in [MechWild's Discord](https://discord.gg/nfxHnsm)
- Ask the ZMK experts in [ZMK's Discord](https://zmk.dev/community/discord/invite)
