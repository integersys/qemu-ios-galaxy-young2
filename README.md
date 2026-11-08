# QEMU-iOS on the Samsung Galaxy Young 2

This fork of QEMU-iOS runs an iPod touch (2nd generation) on a Samsung Galaxy Young 2 under postmarketOS. The phone succesfully boots to iOS.

If you need to install postmarketOS on your Galaxy Young 2, refer to [my repository][young2-pmos].

<div align="center">
  <table>
    <tr>
      <td align="center" valign="top">
        <img width="301" height="380" alt="iOS booting on the Samsung Galaxy Young 2" src="https://github.com/user-attachments/assets/34e8adf2-5dde-4eab-93e4-cfb98f9f451a" />
        <br />
        <strong>iOS booting</strong>
      </td>
      <td align="center" valign="top">
        <img width="282" height="380" alt="iOS Home Screen on the Samsung Galaxy Young 2" src="https://github.com/user-attachments/assets/02f77659-75ec-4345-acd1-155160709fef" />
        <br />
        <strong>iOS Home Screen</strong>
      </td>
    </tr>
  </table>
</div>

## How it works

postmarketOS runs on the phone and hosts QEMU. QEMU emulates the iPod touch hardware, and iOS boots inside that. The iPod and the Young 2 both use a 320 × 480 display, so QEMU output fits the phone’s screen without scaling.

## Build and run

1. Follow the [build guide](documentation/build.md) to cross-compile `qemu-system-arm` for the phone.
2. Follow the [runtime guide](documentation/runtime.md) to prepare the iPod touch ROM files and launch the emulator. The guide uses the boot ROM, NOR image and NAND files from the [upstream iPod touch release][guest-files].

## Credits

The original iPod touch emulation comes from [devos50/qemu-ios][upstream].

[upstream]: https://github.com/devos50/qemu-ios
[young2-pmos]: https://github.com/integersys/postmarketos-young2
[guest-files]: https://github.com/devos50/qemu-ios/releases/tag/n72ap_v1
[qemu]: https://www.qemu.org/
