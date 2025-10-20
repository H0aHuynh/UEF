# UEF

# 1. Tạo script load kext
sudo tee /Library/LaunchDaemons/com.apple.AppleHDA.load.plist > /dev/null << EOF
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>com.apple.AppleHDA.load</string>
    <key>ProgramArguments</key>
    <array>
        <string>/usr/sbin/kextload</string>
        <string>/Library/Extensions/AppleHDA.kext</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
    <key>KeepAlive</key>
    <false/>
</dict>
</plist>
EOF

# 2. Fix quyền
sudo chown root:wheel /Library/LaunchDaemons/com.apple.AppleHDA.load.plist
sudo chmod 644 /Library/LaunchDaemons/com.apple.AppleHDA.load.plist

# 3. Load daemon
sudo launchctl load /Library/LaunchDaemons/com.apple.AppleHDA.load.plist

# 4. Test
sudo launchctl start com.apple.AppleHDA.load