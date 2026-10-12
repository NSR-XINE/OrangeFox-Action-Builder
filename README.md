# OrangeFox Action Builder
Compile custom OrangeFox Recovery using GitHub Actions.

## How to Use
1. Fork or use this repository.
2. Go to the **Actions** tab > select **OrangeFox - Build MIUI / HyperOS** (or **OrangeFox - Build AOSP**) > click **Run workflow**.
3. Fill or confirm the workflow inputs:
   - **MANIFEST_BRANCH**: `14.1` (supports `14.1`, `12.1`, `11.0`, `16.0`)
   - **DEVICE_TREE**: `https://github.com/uke-resources/device_xiaomi_uke-ofox`
   - **DEVICE_TREE_BRANCH**: `fox_14.1`
   - **DEVICE_PATH**: `device/xiaomi/uke`
   - **DEVICE_NAME**: `uke`
   - **BUILD_TARGET**: `recovery` (or `boot`, `vendorboot`)
4. Click **Run workflow**. The finished recovery `.img` and flashable `.zip` will be published directly under **Releases**.

## Features & Improvements
- Supports **fox_14.1** (Android 14) and **fox_16.0** via the official OrangeFox sync tool.
- Pre-configured defaults for **Xiaomi Pad 7 (`uke`)**.
- Automatic workspace cleanup (`slimhub_actions` + `.repo` pruning) to prevent "out of disk space" errors on GitHub Actions runners.
- Uploads `OrangeFox*.img`, `OrangeFox*.zip`, and `recovery.img` directly to GitHub Releases.
