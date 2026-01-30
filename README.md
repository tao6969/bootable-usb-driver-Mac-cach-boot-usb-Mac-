 pkgutil --expand-f /Volumes/Install\ macOS/InstallOS.pkg /tmp/Sierra

       cd /tmp/Sierra
      
       hdiutil attach /private/tmp/Sierra/InstallOS.pkg/InstallESD.dmg -noverify -nobrowse -mountpoint /Volumes/esd

        sudo asr restore -source /Volumes/esd/BaseSystem.dmg -target /Volumes/MyVolume -noprompt -noverify -erase

            diskutil rename OS\ X\ Base\ System Install\ Sierra

         rm -r /Volumes/Install\ Sierra/System/Installation/Packages

       cp -rp /Volumes/esd/Packages /Volumes/Install\ Sierra/System/Installation

            cp -rp /Volumes/esd/BaseSystem.chunklist /Volumes/Install\ Sierra/

             cp -rp /Volumes/esd/BaseSystem.dmg /Volumes/Install\ Sierra/

           hdiutil detach /Volumes/esd

        sudo bless --folder /Volumes/Install\ Sierra/System/Library/CoreServices --label Install\ Sierra

           cp /Volumes/Install\ Sierra/Install\ macOS\ Sierra.app/Contents/Resources/InstallAssistant.icns 
        
            Volumes/Install\ Sierra/.VolumeIcon.icns

             cd "$HOME"

           rm -r /tmp/Sierra
           sau do lay thong tin tu file tep va file usb coppy anh tu file tep sang usb
