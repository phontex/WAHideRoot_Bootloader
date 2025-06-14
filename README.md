# WAHideRoot+Bootloader
<a id="start"></a>
Guide for hiding bootloader status and Root permissions from WhatsApp. Currently this guide is only for Magisk root manager.
In development:
1. Guide for hiding bootloader status and Root permissions from WhatsApp and WhatsApp Business for KernelSU root manager.
2. Guide for hiding bootloader status and Root permissions from WhatsApp Business.

---

## 📌 **Table of Contents**  
[Requirements](#requirements)  
1. [Installation](#installation)  
   - 1.1 [Changing Magisk settings](#changing-magisk-settings)  
   - 1.2 [Installing modules](#installing-modules)  
2. [Configuration](#configuration)  
   - 2.1 [Configuring modules](#configuring-modules)  
   - 2.2 [Configuring apps](#configuring-apps)

[Method limitations](#limitations)  

---

<a id="requirements"></a>
## 📋 **Requirements**  
- Magisk: must be installed on your device
- Root permissions: required for this method  
- WhatsApp: version must not be higher than 2.25.6.71
    - REQUIRED to download this version: [`WhatsApp Messenger 2.25.6.71`](https://www.apkmirror.com/wp-content/themes/APKMirror/download.php?id=8640717&key=61f8fe84b570a713ca0a7b260a98475d68a416a9&forcebaseapk=true). WILL NOT WORK with newer versions!

---

<a id="installation"></a>
## ⚙️ **Installation**  
<a id="changing-magisk-settings"></a>
### 1.1 Changing Magisk settings
   - Open Magisk Manager
   - Go to "Settings", disable "Zygisk" and "DenyList"
   - Open "Configure DenyList", check "Google Play Services" app, tap the app icon and enable all switches. Do the same for "WhatsApp" app
   - Return to "Settings" and tap "Hide Magisk app". Change the app name to anything except "Magisk"

<a id="installing-modules"></a>
### 1.2 Installing modules
   - Download these modules to your device: 
     - [`Zygisk Next`](https://github.com/Dr-TSNG/ZygiskNext/releases)
     - [`LSPosed v1.10.1`](https://github.com/JingMatrix/LSPosed/releases)
     - [`Play Integrity Fix`](https://mmrl.dev/repository/aptoftisk/playintegrityfix)
     - [`TrickyStore`](https://github.com/5ec1cff/TrickyStore/releases)
     - [`TrickyAddon`](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/tag/v3.9)
     - [`Shamiko`](https://github.com/LSPosed/LSPosed.github.io/releases)
   - Return to Magisk Manager main page
   - Go to "Modules" section and select "Install from storage"
   - Select and install downloaded modules
   - After successful installation of all modules, reboot your device

---

<a id="configuration"></a>
## ⚙️ **Configuration**  
<a id="configuring-modules"></a>
### 2.1 Configuring modules
   - After reboot open Magisk Manager
   - Go to "Modules" section
   - Find "Play Integrity Fix" module and tap "Action" button under the module. Wait for process completion, then tap "Close" in bottom right corner
   - Find "Tricky Store" module and tap "Action" button under the module. Wait for WebUI to load and grant the app root access
   - In the opened app open menu (three dots in top right corner) and select "Select all", then tap blue "Save" button
   - Open menu again and select "Install Security Patch"
   - In opened window:
     - Activate "Advanced mode"
     - In "System" field enter "prop"
     - In "Boot" field enter date "2025-05-05"
     - In "Vendor" field enter date "2025-05-05"
     - Tap "Save" button
   - Download file: [`keybox.zip`](https://github.com/user-attachments/files/20700522/keybox.zip) and extract its contents
   - In Tricky Addon app open menu and select "Install custom Keybox", then select file "keybox.xml"

<a id="configuring-apps"></a>
### 2.2 Configuring apps
   - Download file to your device: [`treble_arm64_bgN-KeyAttestation.zip`](https://github.com/user-attachments/files/20734091/treble_arm64_bgN-KeyAttestation.zip)
   - Extract archive contents to any folder
   - Install app: [`Key Attestation`](https://github.com/vvb2060/KeyAttestation/releases)
   - In Key Attestation app:
     1. Open menu (three dots in top right corner)
     2. Select "Load from file"
     3. Specify extracted file "treble_arm64_bgN-KeyAttestation.p7b"
   - Install [`Play Integrity API Checker`](https://play.google.com/store/apps/details?id=gr.nikolasspyr.integritycheck)
   - Run check ("CHECK" button)

   **Expected result:**
   ✅ MEETS_BASIC_INTEGRITY  
   ✅ MEETS_DEVICE_INTEGRITY  
   ✅ MEETS_STRONG_INTEGRITY  

---

<a id="limitations"></a>
## ⚠️ **Method limitations**  
1. **WhatsApp update**:
   - You can update WhatsApp to latest version, but:
   - When trying to add new account, verification error will appear
   - Solution: need to install version "2.25.6.71" again

2. **Account logout**:
   - If you log out from current account:
   - WhatsApp will start checking system integrity again
   - Will need to downgrade to version "2.25.6.71" again

3. **Recommendations**:
   - Don't log out from account unnecessarily
   - Save APK of required version ("2.25.6.71") for emergencies
   - Disable automatic updates in "Play Store"

4. **Important**:
   ```diff
   + Method works ONLY with version "2.25.6.71"
   - New WhatsApp versions detect bypass attempts
