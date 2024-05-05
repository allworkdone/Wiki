![Installation Guide For Project Elixir](https://i.imgur.com/42LxtAl.png)

### Installation Guide For Project Elixir on //DevcieNameHere (Devicecodenamehere)//

> [!CAUTION]
>
> - Your warranty is void. Or valid, probably?
> - Project Elixir is not responsible for any damage you made to your device. You have been warned!

> [!Warning]
>
> - We are not responsible for anything that may happen to your phone by installing custom ROMs.
> - We are not responsible for anything that may happen to your phone by installing any kernels.
> - You do it at your own risk and take the responsibility upon yourself
> - You are not to blame Project Elixir or its respected developers for any of your loss.

> [!Tip] > **Basic Notes for all users:**
>
> - The provided instructions are for Project Elixir based on Android 14.
> - These will only work if you follow every section and step precisely
> - Do not continue after something fails! Contact in support group for help
> - The device must have an unlocked bootloader & has Platform Tools installed in pc.
> - If you are moving from any other Android version to Android 14, it is necessary to do CLEAN FLASH (Format Data)
> - Take a backup for safe side (If you are coming from older Android version or doing a clean flash)
> - For any queries or help related to Elixir, join our support group : [Tap Here](https://telegram.me/Elixir_Discussion)

### Step 1: Download Required Files

1. Download the latest Android platform tools for Windows from the link below:

   - **Platform Tools Link (Windows)**: [platform-tools-latest-windows.zip](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)

2. Download the Recovery from the link below:

   - **Recovery Link [ For Android 14 ]:** [Recovery](https://t.me/RealmeGTNeo2_Updates/725)

3. Download the Project Elixir ROM for from a reliable source.
   - **Project Elixir ROM Link**: [DOWNLOAD](https://projectelixiros.com/download)

### Step 2: Install ADB and Boot into Fastboot Mode

1. Make sure you have ADB (Android Debug Bridge) installed on your computer.
2. Extract the downloaded platform-tools zip file on your computer.
3. Connect your device to your computer using a USB cable.
4. Open a command prompt (Windows) or terminal (macOS and Linux) on your computer.
5. Navigate to the location where you extracted the platform-tools.
6. Enter the following command to check if your device is connected and detected by ADB:

```
adb devices
```

> [!Important]
> If your device is listed, proceed to the next step. If not, make sure your device is connected properly and that USB debugging is enabled in the developer options. 7. Now, reboot your device into Fastboot Mode using the following command:

```
adb reboot bootloader
```

### Step 3: Flash Recovery using Fastboot

1. Once your device is in Fastboot Mode, use the following command to check if Fastboot still detects your device:

```
fastboot devices
```

> [!Note]
> If your device is listed, you are ready and If you don’t get any output or an error:
>
> - **On Windows:** Download [latest fastboot driver](https://xdaforums.com/t/official-tool-windows-adb-fastboot-and-drivers-15-seconds-adb-installer-v1-4-3.2588979/) and copy the folder into your desktop, then go again in Device Manager, locate your device, right-click on your device and choose "Update driver", choose "Browse my computer for driver software", then “Browse…” and select the folder you copied in your desktop. Click “ok” and then on “next”.
> - **on Linux or macOS:** If you see no permissions fastboot try running fastboot as root. When the output is empty, check your USB cable and port!

2. Download the Recovery ZIP (`.img` file will be in zip) from the link provided in Step 1.
3. Place the downloaded Recovery image (`.img` file) in the same location as the platform-tools folder on your computer.
4. Now, flash the Recovery using the following command:

```
fastboot flash recovery recovery_file_name.img
```

> [!Important]
> Replace `recovery_file_name.img` with the actual name of the Recovery image you downloaded if needed. 5. After flashing the recovery, use the following command to reboot your Recovery:

```
fastboot reboot recovery
```

6. Your device will reboot with Recovery installed.
   > [!Note]
   > If your recovery does not show the logo, then you have ccidentally booted into the wrong recovery. Please start at the top of this section!

### Step 4: Flash Project Elixir ROM

1. Download the Elixir installation package that you would like to install
2. If you are not in recovery, reboot into recovery: hold `Volume Down + Volume Up + Power`
3. Now tap Factory Reset, then Format data / factory reset and continue with the formatting process.
   > [!Warning]
   > This will remove encryption and **will delete all files stored** in the internal storage, as well as format your cache partition (if you have one).
4. Return to the main menu
5. Sideload the `Elixir.zip` package
   > [!CAUTION]
   > Do not reboot before you read/followed the rest of the instructions!
6. On the device, select “Apply Update”, then “Apply from ADB” to begin sideload.
7. On the host machine, sideload the package using:

```
adb -d sideload <filename.zip>
```

8. After the package is installed, recovery will inform you that reboot to recovery is required to install add-ons.
9. In case you want to do that, please select “Yes,” otherwise “No”.

> [!Tip]
> Normally, adb will report `Total xfer: 1.00x`, but in some cases, even if the process succeeds the output will stop at 47% and report `Total xfer: 0.98x` or `adb: failed to read command: Success`. In some cases it will report `adb: failed to read command: No error` or `adb: failed to read command: Undefined error: 0` which is also fine.

10. **All set!**

- Once you have installed everything successfully, you can now reboot your device into the OS for the first time!
- Click the back arrow in the top left of the screen, then “Reboot system now”.

> [!Important] > **May Required Files:**
>
> - Android 14 Recovery Link : [Tap here for link](https://t.me/RealmeGTNeo2_Updates/725)
> - Any Extra File link if required : [Tap Here for link](https://sourceforge.net/projects/project-elixir/files/fourteen)

<br>

> [!Note]
> **Notes specific to device build**
>
> - Gapps is already included in zip no need to flash additionally
> - First boot usually takes no longer than 15 minutes, depending on the device. If it takes longer, you may have missed a step.
> - If you are coming from PORTs then you need to Format Data and flash latest firmware [depending on the device]
> - If you are coming from Android 12 or 13 to Android 14 then clean flash is compulsory and format data.
> - If you are encrypted do format Data before flashing build to avoid bugs.

<br>

> [!Tip] > **Donate**: [Do consider donating or buying us a coffee](https://projectelixiros.com/donate)
