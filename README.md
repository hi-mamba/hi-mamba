# 道生一 DAOSI 安装包（手动发布）

下载页：https://hi-mamba.github.io/hi-mamba/daosi/

本分支只放安装包，每次更新会整体覆盖（不保留历史）。配置 `PUBLISH_TOKEN` 后，CI 会改为自动发布到 Release `daosi-latest`。

| 文件 | 平台 | 来源 |
|---|---|---|
| DAOSI-Android-debug.apk | Android 8.0+ | daosi@37ad9c8 debug 构建 |
| DAOSI-Windows.msi | Windows 10/11 x64 | daosi@37ad9c8 |
| DAOSI-macOS.dmg | macOS 12+（未公证） | daosi@3058089 CI Build Desktop & iOS #2 |
| DAOSI-iOS-unsigned.ipa | iOS 16+（未签名，需自行签名） | daosi@3058089 CI Build Desktop & iOS #2 |
