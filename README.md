# Infinirc GPU Fan Control (igfc tool)
> ⚠️ **MAINTENANCE NOTICE / 維護狀態公告**
>
> This repository is **no longer actively maintained**.
>
> 🚀 **The next-generation replacement is available here:**  
> 👉 https://github.com/Infinirc/nvfd
>
> Please use **nvfd** for all new deployments and future updates.
> This repository is kept for **historical reference only**.
>
> ---
>
> ⚠️ **本專案已停止維護**
>
> 🚀 **新版工具請使用：**  
> 👉 https://github.com/Infinirc/nvfd
>
> 本倉庫僅保留作為歷史參考，**不再接受新功能、修復或 Issue**。






Infinirc GPU Fan Control (IGFC) 是一個用於 NVIDIA GPU 的風扇控制工具。它允許用戶自定義風扇曲線，設置固定風扇速度，或使用自動模式。

Infinirc GPU Fan Control (IGFC) is a fan control tool for NVIDIA GPUs. It allows users to customize fan curves, set fixed fan speeds, or use automatic mode.


## 免責聲明 / Disclaimer

請注意：使用 Infinirc GPU Fan Control (IGFC) 軟體時，用戶需要自行承擔風險。不當使用本軟件，特別是設置不適當的風扇轉速，可能導致您的 GPU 損壞或其他硬件問題。Infinirc 不對因使用本軟件而導致的任何 GPU 故障或其他硬件損壞負責。用戶有責任謹慎使用本軟件，並密切監控 GPU 的溫度和性能。

強烈建議用戶在使用本軟件時遵循以下建議：
1. 始終保持謹慎，不要將風扇速度設置得過低或過高。
2. 定期監控 GPU 溫度，確保其處於安全範圍內。
3. 如果發現任何異常，立即停止使用本軟件並恢復默認設置。

使用本軟件即表示您同意承擔所有相關風險，並同意 Infinirc 不對任何可能發生的損壞負責。

Please note: Use of the Infinirc GPU Fan Control (IGFC) software is at your own risk. Improper use of this software, especially setting inappropriate fan speeds, may result in damage to your GPU or other hardware issues. Infinirc is not responsible for any GPU failures or other hardware damage resulting from the use of this software. It is the user's responsibility to use this software cautiously and to closely monitor their GPU's temperature and performance.

Users are strongly advised to follow these recommendations when using this software:
1. Always exercise caution and avoid setting fan speeds too low or too high.
2. Regularly monitor GPU temperatures to ensure they remain within safe ranges.
3. If any abnormalities are observed, immediately stop using the software and revert to default settings.

By using this software, you agree to assume all associated risks and agree that Infinirc will not be held responsible for any potential damage that may occur.


## 功能 / Features

- 自定義風扇曲線 / Custom fan curve
- 固定風扇速度 / Fixed fan speed
- 自動模式 / Automatic mode
- 多 GPU 支持 / Multi-GPU support
- 實時溫度監控 / Real-time temperature monitoring

## 安裝 / Installation

```
wget https://raw.githubusercontent.com/ricky-chaoju/igfc-Infinirc-Gpu-Fan-Control/refs/heads/main/igfc_install.sh && chmod +x igfc_install.sh && sudo ./igfc_install.sh
```

## 解除安裝 / Uninstallation

```
wget https://raw.githubusercontent.com/ricky-chaoju/igfc-Infinirc-Gpu-Fan-Control/main/igfc_uninstall.sh && chmod +x igfc_uninstall.sh && sudo ./igfc_uninstall.sh
```


## 使用方法 / Usage

使用 `igfc` 命令來控制您的 GPU 風扇。以下是一些常用命令：

Use the `igfc` command to control your GPU fans. Here are some common commands:

```

+----------------------------+-------------------------------------------+
| 命令 / Command             | 描述 / Description                        |
+----------------------------+-------------------------------------------+
| igfc auto                  | 設置為自動模式                            |
|                            | Set to automatic mode                     |
+----------------------------+-------------------------------------------+
| igfc curve                 | 使用自定義風扇曲線                        |
|                            | Use custom fan curve                      |
+----------------------------+-------------------------------------------+
| igfc curve <temp> <speed>  | 編輯風扇曲線                              |
|                            | Edit fan curve                            |
+----------------------------+-------------------------------------------+
| igfc curve show            | 顯示當前風扇曲線                          |
|                            | Show current fan curve                    |
+----------------------------+-------------------------------------------+
| igfc curve reset           | 還原預設風扇曲線                          |
|                            | Reset fan curve to default                |
+----------------------------+-------------------------------------------+
| igfc <speed>               | 設置所有GPU固定風扇速度（30-100）         |
|                            | Set fixed fan speed for all GPUs (30-100) |
+----------------------------+-------------------------------------------+
| igfc <gpu_index> <speed>   | 設置特定GPU固定風扇速度（30-100）         |
|                            | Set fixed fan speed for specific GPU      |
+----------------------------+-------------------------------------------+
| igfc list                  | 列出所有GPU及其編號                       |
|                            | List all GPUs and their indices           |
+----------------------------+-------------------------------------------+
| igfc status                | 顯示當前狀態                              |
|                            | Show current status                       |
+----------------------------+-------------------------------------------+
| igfc -h                    | 顯示此幫助信息                            |
|                            | Show this help message                    |
+----------------------------+-------------------------------------------+

```

## 系統要求 / System Requirements

1. NVIDIA GPU
   - 支持NVIDIA的GPU硬件
   - Supported NVIDIA GPU hardware

2. Linux 操作系統 / Linux Operating System

3. NVIDIA 驅動程序 / NVIDIA Drivers
   - 必須使用官方NVIDIA驅動，不支持系統自帶的開源驅動
   - 請從NVIDIA官方網站下載並安裝最新的驅動程序
   - Official NVIDIA drivers are required; open-source drivers included with the system are not supported
   - Please download and install the latest drivers from the official NVIDIA website

4. `nvidia-settings` 工具 / `nvidia-settings` Tool
   - 此工具將在安裝過程中自動安裝
   - 如果您的系統中尚未安裝，安裝腳本將會自動進行安裝
   - This tool will be automatically installed during the installation process
   - If it's not already installed on your system, the installation script will handle it

注意：在安裝 IGFC 之前，請確保您的系統滿足上述所有要求。特別是NVIDIA驅動程序，必須使用官方驅動以確保最佳兼容性和性能。

Note: Please ensure your system meets all the above requirements before installing IGFC. Particularly for NVIDIA drivers, official drivers must be used to ensure optimal compatibility and performance.



## 支持 / Support

如果您在使用過程中遇到任何問題，請開啟一個 issue。

If you encounter any problems while using this tool, please open an issue.
