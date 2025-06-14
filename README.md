# WAHideRoot+Bootloader
<a id="开始"></a>
隐藏引导加载程序状态和Root权限的WhatsApp指南。目前本指南仅适用于Magisk root管理器。
开发中：
1. 适用于KernelSU的WhatsApp和WhatsApp Business隐藏指南
2. 适用于WhatsApp Business的隐藏指南

--- 

## 📌 **目录**  
[要求](#要求)  
1. [安装](#安装)  
   - 1.1 [修改Magisk设置](#修改Magisk设置)  
   - 1.2 [安装模块](#安装模块)  
2. [配置](#配置)  
   - 2.1 [模块配置](#模块配置)  
   - 2.2 [应用配置](#应用配置)

[方法限制](#方法限制)  

---

<a id="要求"></a>
## 📋 **要求**  
- Magisk：您的设备必须已安装Magisk
- Root权限：此方法需要root权限  
- WhatsApp：WhatsApp版本不得高于2.25.6.71
    - 必须下载此版本：[`WhatsApp Messenger 2.25.6.71`](https://www.apkmirror.com/wp-content/themes/APKMirror/download.php?id=8640717&key=61f8fe84b570a713ca0a7b260a98475d68a416a9&forcebaseapk=true)。新版无法使用此方法！

---

<a id="安装"></a>
## ⚙️ **安装**  
<a id="修改Magisk设置"></a>
### 1.1 修改Magisk设置
   - 打开Magisk Manager
   - 进入"设置"，禁用"Zygisk"和"DenyList"
   - 打开"配置DenyList"，勾选Google Play服务应用，点击应用图标并启用所有开关。对WhatsApp应用执行相同操作
   - 返回"设置"并点击"隐藏Magisk应用"。将应用名称改为除"Magisk"外的任意名称

<a id="安装模块"></a>
### 1.2 安装模块
   - 下载以下模块到您的设备： 
     - [`Zygisk Next`](https://github.com/Dr-TSNG/ZygiskNext/releases)
     - [`LSPosed v1.10.1`](https://github.com/JingMatrix/LSPosed/releases)
     - [`Play Integrity Fix`](https://mmrl.dev/repository/aptoftisk/playintegrityfix)
     - [`TrickyStore`](https://github.com/5ec1cff/TrickyStore/releases)
     - [`TrickyAddon`](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/tag/v3.9)
     - [`Shamiko`](https://github.com/LSPosed/LSPosed.github.io/releases)
   - 返回Magisk Manager主页面
   - 进入"模块"部分并选择"从存储安装"
   - 选择并安装下载的模块
   - 所有模块成功安装后重启设备

---

<a id="配置"></a>
## ⚙️ **配置**  
<a id="模块配置"></a>
### 2.1 模块配置
   - 重启后打开Magisk Manager
   - 进入"模块"部分
   - 找到"Play Integrity Fix"模块并点击模块下的"Action"按钮。等待过程完成，然后点击右下角的"Close"
   - 找到"Tricky Store"模块并点击模块下的"Action"按钮。等待WebUI加载并授予应用root权限
   - 在打开的应用中打开菜单(右上角三点)并选择"全选"，然后点击蓝色"保存"按钮
   - 再次打开菜单并选择"安装安全补丁"
   - 在打开的窗口中：
     - 启用"高级模式"
     - 在"System"字段输入"prop"
     - 在"Boot"字段输入日期"2025-05-05"
     - 在"Vendor"字段输入日期"2025-05-05"
     - 点击"保存"按钮
   - 下载文件：[`keybox.zip`](https://github.com/user-attachments/files/20700522/keybox.zip)并解压其内容
   - 在Tricky Addon应用中打开菜单并选择"安装自定义Keybox"，然后选择文件"keybox.xml"

<a id="应用配置"></a>
### 2.2 应用配置
   - 下载文件到设备：[treble_arm64_bgN-KeyAttestation.zip](https://github.com/user-attachments/files/20734091/treble_arm64_bgN-KeyAttestation.zip)
   - 将存档内容解压到任意文件夹
   - 安装应用：[Key Attestation](https://github.com/vvb2060/KeyAttestation/releases)
   - 在Key Attestation应用中：
     1. 打开菜单(右上角三点)
     2. 选择"从文件加载"
     3. 指定解压后的文件"treble_arm64_bgN-KeyAttestation.p7b"
   - 安装[Play Integrity API Checker](https://play.google.com/store/apps/details?id=gr.nikolasspyr.integritycheck)
   - 运行检查("CHECK"按钮)

   **预期结果：**
   ✅ MEETS_BASIC_INTEGRITY  
   ✅ MEETS_DEVICE_INTEGRITY  
   ✅ MEETS_STRONG_INTEGRITY  

---

<a id="方法限制"></a>
## ⚠️ **方法限制**  
1. **WhatsApp更新**：
   - 您可以更新WhatsApp到最新版本，但：
   - 尝试添加新账号时会出现验证错误
   - 解决方案：需要重新安装2.25.6.71版本

2. **退出账号**：
   - 如果您退出当前账号：
   - WhatsApp将重新检查系统完整性
   - 需要将版本回退到2.25.6.71

3. **建议**：
   - 非必要不要退出账号
   - 保存所需版本(2.25.6.71)的APK以防故障
   - 在Play商店中禁用自动更新

4. **重要**：
   ```diff
   + 此方法仅适用于2.25.6.71版本
   - 新版WhatsApp会检测绕过行为
