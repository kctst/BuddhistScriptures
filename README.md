# 善恩佛經 Android APK

此 repository 僅用作《善恩佛經》Android APK 公開下載，不包含 App source。

目前正式側載版本：**v1.4.0 / code49**，package `com.jingge.app`。

正式 Google Play 用戶建議優先透過 Google Play 安裝及更新。

其他 Android 裝置可透過下載頁或 GitHub Releases 下載 APK：

下載頁：https://kctst.github.io/BuddhistScriptures/

直接下載：
https://github.com/kctst/BuddhistScriptures/releases/latest/download/BuddhistScriptures.apk

## 發佈新版（維護者）

每次出新版，Release 與下載頁必須指向同一個 APK。本機正式檔名 `善恩佛經-v<version>-code<code>.apk`；GitHub伺服器會移除中文字，沿用已發布慣例 `BuddhistScriptures-v<version>-code<code>.apk`，公開label保留中文正式名稱。既有相容asset `BuddhistScriptures.apk` 保留。

1. GitHub Releases：建立新 Release（非 Draft、非 Prerelease、設為 Latest），上傳正式名稱 APK、byte-identical `BuddhistScriptures.apk` 及 `SHA256.txt`。舊 Release 永久保留。
2. 只更新本頁／README metadata及下載連結，commit 後 push；APK/AAB不再commit。本頁fallback用既有Release latest相容redirect，既有API resolver成功後選正式帶code的APK asset（不選AAB）。

根目錄舊 `BuddhistScriptures.apk` 保留為code46歷史相容檔，不改bytes或URL；下載新版請用上述永久首頁或Release latest連結。永久首頁／QR策略不變。

兩邊 SHA-256 必須一致。下載頁及 App 內 QR Code 網址不用更改。

## code49 驗證

APK 64,957,680 bytes，SHA-256 `89CDA5D4B85ADDA34788EE54AEEC4D40A2AEBF9B47382071C1BCA6A83060AB02`。applicationId `com.jingge.app`／1.4.0／49，既有正式upload signer，apksigner v2/v3及zipalign PASS。

AAB只供Google Play，不作側載下載。code49 APK公開不等於remote policy已升49；本輪policy仍Play22/0、Huawei22/0、sideload46/0，另待Owner批准。
