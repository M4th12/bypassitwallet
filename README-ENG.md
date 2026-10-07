# Guide to restoring IT-Wallet functionality on devices with an unlocked bootloader or a custom ROM

⚠️ Warning: this guide is not guaranteed to work 100% on all devices or ROMs. ⚠️

Tested on a Poco F2 Pro with LineageOS 23.2, working as of 07/10/2026.

Since June 2025, Google has changed how device integrity is verified. Devices running Android 13 or higher may fail this fix more easily.

## Requirements

- **Magisk**, **KernelSU-Next** or **Apatch** installed

## Required modules

- [ReZygisk](https://github.com/PerformanC/ReZygisk/releases)
- [Play Integrity Fix Inject](https://github.com/osm0sis/PlayIntegrityFork/releases)
- [Specter](https://github.com/dpejoh/specter/releases)

## Optional

- [HMA-OSS](https://github.com/frknkrc44/HMA-OSS/releases)

## Steps

- Install the modules in the order listed above, then reboot.

- After rebooting, open your root manager and go to the modules section. On the Play Integrity Fix module, tap the "Action" button. A web interface will open.

<img width="1080" height="1884" alt="image" src="https://github.com/user-attachments/assets/48279c74-b44a-4119-a530-bd83133f5f52" />

- Everything should now be working. If all went well, you should see this:

<img width="869" height="762" alt="image" src="https://github.com/user-attachments/assets/32297705-f1c0-4bc8-bc22-d915afc949d4" />

## FAQ

- With Google's new integrity verification method, many phones may no longer pass this fix.

- For the best chances, check that your ROM is signed with private keys, doesn't have banned kernel names, has SELinux set to Enforcing, and has encrypted storage.
