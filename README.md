# UEF

<key>IOKitPersonalities</key>
<dict>
    <key>VoodooHDA</key>
    <dict>
        <key>IOClass</key>
        <string>VoodooHDA</string>
        <key>IOMatchCategory</key>
        <string>audio</string>
        <key>CFBundleIdentifier</key>
        <string>org.voodoo.driver.VoodooHDA</string>
        <key>IOProviderClass</key>
        <string>AppleHDAController</string>
        <key>HDAConfigDefault</key>
        <array>
            <dict>
                <key>func-group</key>
                <integer>1</integer>
                <key>codec</key>
                <data>EjkuZw==</data> <!-- Base64 of 0x10ec0897 -->
                <key>layout</key>
                <data>BRQ=</data> <!-- Base64 of 69 (layout ID 69) -->
                <key>device</key>
                <array>
                    <dict>
                        <key>node</key>
                        <integer>0x14</integer> <!-- Speaker -->
                        <key>codec</key>
                        <data>EjkuZw==</data>
                    </dict>
                    <dict>
                        <key>node</key>
                        <integer>0x21</integer> <!-- Headphone -->
                        <key>codec</key>
                        <data>EjkuZw==</data>
                    </dict>
                </array>
            </dict>
        </array>
        <key>Platforms</key>
        <string>HDA</string>
        <key>SampleRate</key>
        <integer>44100</integer>
        <key>BitDepth</key>
        <integer>16</integer>
        <key>InputGain</key>
        <real>0.0</real>
    </dict>
</dict>