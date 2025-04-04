## Disclaimer

Disabling SIP will reduce the security of the system and make iOS apps in App Store and Apple Pay unusable.

## Install

### Prerequisites

- SIP debugging restrictions are disabled (via `csrutil enable --without debug` command in recovery mode).
- For Apple Intelligence: A non-China Apple ID signed in, region set to the United States, and language set to English (US).
- For Xcode Predictive Code Completion: Xcode is installed and run at least once.

> [!NOTE]  
> No need to install Xcode if you only want to use Apple Intelligence.

### Method 2: Manually

```shell
sudo curl https://raw.githubusercontent.com/Soohti/eligibilityd-debug/master/eligibilityd-debug.sh -o /usr/local/bin/eligibilityd-debug
sudo chmod +x /usr/local/bin/eligibilityd-debug
sudo curl https://raw.githubusercontent.com/Soohti/eligibilityd-debug/master/cat.soohti.eligibilityd-debug.plist -o /Library/LaunchDaemons/cat.soohti.eligibilityd-debug.plist
sudo launchctl load -w /Library/LaunchDaemons/cat.soohti.eligibilityd-debug.plist
```

## Uninstall

### If Installed Manually

```shell
sudo launchctl unload -w /Library/LaunchDaemons/cat.soohti.eligibilityd-debug.plist
sudo rm /Library/LaunchDaemons/cat.soohti.eligibilityd-debug.plist
sudo rm /usr/local/bin/eligibilityd-debug
```

## Acknowledgement

Thanks for those who make this possible together: [Kyle-Ye](https://github.com/Kyle-Ye), [Cyandev](https://twitter.com/unixzii), [Lakr233](https://twitter.com/Lakr233), [Sou1gh0st](https://twitter.com/Sou1gh0st), Yuriko.

## License

MIT License
