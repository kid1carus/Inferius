# Inferius
Inferius (and it's sister tool, Restituere), is a tool to create and restore custom IPSWs for 64-bit devices using Firmware Bundles, similarly to xpwn for 32-bit devices.
Due to how the tool is built, this could be used for many different applications, but currently it's main use is for downgrading devices to previous iOS versions.
*Note: All custom IPSWs restored with Inferius will require you to boot your device via a computer every time your device is turned off.*

Inferius is Latin for 'below', and Restituere is Latin for 'restore'.

## Requirements
- A macOS system.
- `ldid` from [Homebrew](https://brew.sh/).
- A 64bit device compatible with checkm8.
- A firmware bundle for the device you are wanting to restore and the version you are wanting to downgrade to.
- A brain.

## Disclaimer
- I take **NO** reponsibility for any loss of data, issues with your device, or anything else if you use Inferius. You accept those risks when you use this tool.

## IMPORTANT NOTE
- When restoring custom IPSWs, **please** use custom IPSWs that were freshly created with Inferius. Older IPSWs made with Inferius can cause a brick, due to Inferius needing to download the LLB and iBoot from a signed firmware, and place them into the custom IPSW.

## Usage

```
usage: ./inferius.py -d 'device' -i 'iOS Version' -f 'IPSW' [-v]

Inferius - Create custom IPSWs for your 64bit iOS device!

optional arguments:
  -h, --help            show this help message and exit
  -d DEVICE, --device DEVICE
                        Your device identifier (e.g. iPhone10,2)
  -i VERSION, --version VERSION
                        The version of your stock IPSW
  -f IPSW, --ipsw IPSW  Path to stock IPSW
  -v, --verbose         Print verbose output for debugging
  ```

```
usage: ./restituere.py -d 'device' -i 'iOS version' -f 'IPSW' [-v]

Restituere - Restore custom IPSWs onto your 64bit iOS device!

optional arguments:
  -h, --help            show this help message and exit
  -d DEVICE, --device DEVICE
                        Your device identifier (e.g. iPhone10,2)
  -i VERSION, --version VERSION
                        The version of your custom IPSW
  -f IPSW, --ipsw IPSW  Path to custom IPSW
  -v, --verbose         Print verbose output for debugging
  -u, --update          Keep data while restoring (EXPERIMENTAL)  
```
- Inferius is used to create a custom IPSW, and Restituere is used for restoring a custom IPSW.
## FAQ

### What's the use for this?
- The main use is for downgrading to older iOS versions.


### How do I create my own Firmware Bundles?
- There is a guide for creating your own Firmware Bundles in the [wiki](https://github.com/marijuanARM/Inferius/wiki/Creating-your-own-Firmware-Bundles).

### How can I contribute my own Firmware Bundles?
- Make a [Pull Request](https://github.com/marijuanARM/Inferius/compare)!
- Please make sure that the custom IPSW that your Firmware Bundle creates is usable before PRing.

### I have an issue with this tool or need help creating a Firmware Bundle, where can I go for help?
- Join my [discord](https://discord.gg/fAngssA), and I'll be happy to help in `#inferius-help`!

### How do I boot my device after restoring?
- Use either [PyBoot](https://github.com/MatthewPierson/PyBoot) or [ra1nsn0w](https://github.com/tihmstar/ra1nsn0w).

### Can I request Firmware Bundles to be made?
- Absolutely! Just ask in `#inferius-help` in my [discord](https://discord.gg/fAngssA), and I or someone else will get to it whenever we can.

### Can you downgrade to any version, regardless of SEP compatibility?
-  No, you are still limited to versions compatible with your current installed SEP version, unfortunately. Hopefully that may change in the future with the amazing work the checkra1n team is doing.

### Is this an untethered restore?
- No, any custom IPSWs restored will still require you to boot manually with a computer, using either [PyBoot](https://github.com/MatthewPierson/PyBoot) or [ra1nsn0w](https://github.com/tihmstar/ra1nsn0w).

## Credits
- [NotHereForTheDong](https://github.com/NotHereForTheDong) for beta testing & contributing bundles.
- [Renaitare](https://twitter.com/Renaitare) for beta testing.
- [Chibibowa](https://twitter.com/Chibibowa) for beta testing.
- [Moses](https://twitter.com/MosesBuckwalter) for beta testing.
- [Matty](https://twitter.com/mosk_i) for his special build of futurerestore that allows restoring of custom IPSWs.
