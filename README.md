# 善恩佛經 Android APK

此 repository 僅用作《善恩佛經》Android APK 公開下載，不包含 App source。

目前正式側載版本：**v1.4.1 / code69**，package `com.jingge.app`。

正式 Google Play 用戶建議優先透過 Google Play 安裝及更新。

其他 Android 裝置可透過下載頁或 GitHub Releases 下載 APK：

下載頁：https://kctst.github.io/BuddhistScriptures/

直接下載：
https://github.com/kctst/BuddhistScriptures/releases/latest/download/BuddhistScriptures.apk

## 發佈新版（維護者）

每次出新版，Release 與下載頁必須指向同一個 APK。本機正式檔名 `善恩佛經-v<version>-code<code>.apk`；GitHub伺服器會移除中文字，沿用已發布慣例 `BuddhistScriptures-v<version>-code<code>.apk`，公開label保留中文正式名稱。既有相容asset `BuddhistScriptures.apk` 保留。

1. GitHub Releases：建立新 Release（非 Draft、非 Prerelease、設為 Latest），上傳正式名稱 APK、byte-identical `BuddhistScriptures.apk` 及 `SHA256.txt`。舊 Release 永久保留。
2. 只更新本頁／README metadata及下載連結，commit 後 push；APK/AAB不再commit。本頁fallback用既有Release latest相容redirect，既有API resolver成功後選正式帶code的APK asset（不選AAB）。
3. 同一次工作更新 `update-policy.json`（永久規則）：只將 `channels.sideload.latestVersionCode` 改成該版 code，`minimumSupportedVersionCode` 維持 0（強制更新須另行明確批准）；`googlePlay`／`huawei` 不因 GitHub 發布而改。Release 公開並驗證下載後先改，push 後等 Pages built，再讀返 https://kctst.github.io/BuddhistScriptures/update-policy.json 核對與本機一致。App 靠此檔得知有新版，漏做會令舊版側載用戶收唔到更新提示。本 repo 冇設 git 身份：commit 用 `git -c user.name=<AI 名> -c user.email=<noreply 地址>`，唔好冒用其他 AI 身份。
4. Google Play 新版 production `completed` 且 100% 推出後，同樣要升 `googlePlay.latestVersionCode`（永久規則，唔使再問）：喺 app repo 跑 `node tools/update_policy.mjs --sync-play --publish`（Play API 核實；只升 googlePlay，minimum 維持 0；HANDOVER.md 有 `PLAY-POLICY-HOLD` 煞車時唔會升；Huawei 要擁有人確認先改）。

根目錄舊 `BuddhistScriptures.apk` 保留為code46歷史相容檔，不改bytes或URL；下載新版請用上述永久首頁或Release latest連結。永久首頁／QR策略不變。

兩邊 SHA-256 必須一致。下載頁及 App 內 QR Code 網址不用更改。

## code69 驗證

APK 64,996,781 bytes，SHA-256 `DD19E1F8F0E6F52AA3AF21F958DC8B2EFD601F02102573DCB1BA527C52E545CD`。applicationId `com.jingge.app`／1.4.1／69，既有正式upload signer，apksigner v2/v3及zipalign PASS。

AAB只供Google Play，不作側載下載。sideload remote policy 已升為 69/0（Owner 2026-10-08 永久規則：每次 GitHub 側載發版同次升 policy，令舊版側載用戶收到更新提示）；Play51/0、Huawei22/0 維持不變，各商店渠道由Owner確認實際可下載後才逐個提高；所有 minimum 仍為 0。
