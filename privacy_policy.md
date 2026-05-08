# Privacy Policy / 隐私政策

> ⚠️ 这是基于 Whisker 实际数据实践写的政策。提交前请：
> 1. 转 HTML 托管到一个公开 URL（GitHub Pages / Notion 公开页 / 自建站都行），App Store Connect 需要 URL
> 2. 如果上架欧盟，建议让律师审一遍 GDPR 条款
> 3. 如果未来加入服务端组件，必须更新本文件并在 App 内提示用户

---

## English

# Privacy Policy

**Effective Date:** May 7, 2026

Whisker ("we", "us", "the app") is a local-first pet health record for iOS. This Privacy Policy explains, in plain language, what data Whisker handles, where it lives, and what we do — and do not — do with it.

**Short version:** We do not collect any personal data. We do not have a server. We cannot read your records, because they never leave your device unencrypted.

## 1. Data Whisker stores on your device

When you use Whisker, you may enter information about your pets, including:
- Pet name, species, breed, birth date, microchip ID, allergies, medical conditions, photos
- Vaccine, deworming, medication, weight, vet-visit records and dates
- Scanned documents (lab reports, prescriptions, invoices) and the OCR text extracted from them
- Veterinarian contact details you choose to save

All of the above is stored inside the iOS application sandbox in a database encrypted with 256-bit AES (SQLCipher). The encryption key is generated on first launch and stored in the iOS Keychain on your device. The key never leaves your device.

## 2. Data we collect

None.

We do not have user accounts. We do not have a server. We do not run analytics SDKs (no Firebase Analytics, no Mixpanel, no Sentry, no Crashlytics, no advertising IDs). We do not track app opens, feature usage, errors, or any other behavior.

## 3. Permissions Whisker requests

Whisker may ask for the following iOS permissions. Each one is used locally and never transmitted off your device:

- **Camera** — to scan paper documents like lab reports and prescriptions. Image processing (Vision OCR) runs entirely on your iPhone.
- **Photo Library** — only when you pick an existing image to attach to a pet record.
- **Face ID / Touch ID** — to lock the app, if you enable biometric unlock in Settings. Whisker uses Apple's `LocalAuthentication` API; no biometric data is ever read or stored by us.
- **Apple Health** — read-only access to your step count and outdoor walking time, used to plot exercise correlations next to your dog's weight curve. We never write to HealthKit. The data stays in HealthKit; we read it on demand.
- **Local Network** — only if you enable Family Sharing. Used to discover other Whisker devices on your Wi-Fi via Apple's MultipeerConnectivity framework. Records sync peer-to-peer between paired devices and never traverse a server we control.

## 4. In-App Purchases

Whisker offers optional Premium subscriptions and a one-time lifetime purchase. All purchases are processed by Apple via the App Store. Whisker never sees, transmits, or stores your payment details. Purchase receipts are validated locally on your device.

## 5. On-device AI

Whisker uses Apple's on-device machine learning for two features:
- **Vision OCR** to convert scanned paper into text.
- **Apple Foundation Models** (iOS 26+, on Apple Intelligence-capable devices) to extract structured lab values from messy OCR text.

Both run entirely on your iPhone. No image, no text, and no extracted value is ever sent to a remote server by Whisker.

## 6. Backups

If you create a backup using the in-app feature, the resulting file:
- Is encrypted with AES-256-GCM using a key derived from your passphrase or 12-word recovery phrase
- Is saved to whatever destination you choose (Files app, AirDrop, etc.)
- Is never sent to us or to any third party

We have no ability to recover your backup if you lose your passphrase or recovery phrase.

## 7. Children's privacy

Whisker is not directed at children under 13. We do not knowingly collect any personal information from children — and indeed we do not knowingly collect personal information from anyone.

## 8. Your rights

Because we hold no personal data, requests to access, correct, export or delete data should be directed to your own device. You can:
- Export your records via the in-app backup feature
- Delete all records by uninstalling the app (the encrypted database is removed with the app sandbox)
- Reset onboarding state by deleting and reinstalling

If you are in the EU/UK (GDPR) or California (CCPA), please note: we are not a "data controller" or "business" handling your personal information, because we do not collect or process your data on any system we operate.

## 9. Changes to this policy

If we ever change Whisker's architecture in a way that involves collecting or transmitting your data — for example by adding a sync server — we will update this Privacy Policy and present the change in the app before the new behavior takes effect.

## 10. Contact

Questions about this policy: shadeless@126.com

---

## 简体中文

# 隐私政策

**生效日期：** 2026年5月7日

Whisker（"我们"、"本应用"）是一款 iOS 端的本地优先宠物健康档案工具。本隐私政策用通俗的方式说明 Whisker 会处理哪些数据、数据存在哪里、以及我们会做什么、不会做什么。

**一句话总结：** 我们不收集任何个人数据。我们没有服务器。你的记录从来不会以未加密形式离开你的设备，所以我们读不到。

## 1. Whisker 保存在你设备上的数据

使用 Whisker 时，你可能录入以下信息：
- 宠物姓名、物种、品种、生日、芯片号、过敏源、慢性病、照片
- 疫苗、驱虫、用药、体重、看诊记录及时间
- 扫描文件（化验单、处方、发票）以及从中识别出的文字
- 你保存的兽医联系方式

以上所有内容都保存在 iOS 应用沙盒内的数据库中，使用 256 位 AES（SQLCipher）加密。加密密钥在首次启动时生成并保存在本机 iOS Keychain 中，**永不离开你的设备**。

## 2. 我们收集的数据

无。

我们没有用户账号、没有服务器，没有任何统计 SDK（无 Firebase Analytics、Mixpanel、Sentry、Crashlytics、广告 ID）。我们不追踪应用打开、功能使用、崩溃、或任何其它行为。

## 3. Whisker 请求的系统权限

Whisker 可能请求以下 iOS 权限。每一项都仅在本机使用，**绝不会**传输到设备之外：

- **相机** —— 用于扫描化验单、处方等纸质文档。图像识别（Vision OCR）完全在你的 iPhone 上运行。
- **相册** —— 仅在你主动选择已有图片附到宠物档案时才会读取。
- **Face ID / Touch ID** —— 当你在设置里开启"应用锁"时使用。我们调用的是 Apple 的 `LocalAuthentication` API，从不读取或存储任何生物识别数据。
- **Apple 健康** —— 只读权限，读取每日步数与户外行走时长，用来在你狗狗的体重曲线旁绘制运动趋势对照。我们从不向 HealthKit 写入数据；数据存放在 HealthKit 中，我们按需读取。
- **本地网络** —— 仅在你启用"家庭共享"时使用。基于 Apple MultipeerConnectivity 框架，在同一 Wi-Fi 下发现其它 Whisker 设备。配对设备之间点对点同步，**不经过任何由我们控制的服务器**。

## 4. 应用内购买

Whisker 提供可选的 Premium 订阅与一次性终身买断。所有购买由 Apple 通过 App Store 处理，Whisker 看不到、不会传输、也不会保存你的支付信息。订阅凭据在你的设备上本地校验。

## 5. 设备端 AI

Whisker 使用 Apple 的设备端机器学习实现两个功能：
- **Vision OCR**：把扫描的纸质内容识别成文字
- **Apple Foundation Models**（iOS 26+，需 Apple Intelligence 兼容机型）：从杂乱的 OCR 文本中提取结构化体检指标

两者都完全在你的 iPhone 上运行。Whisker 不会把任何图像、文本或识别结果发送到远程服务器。

## 6. 备份

如果你使用应用内的备份功能，生成的备份文件：
- 使用 AES-256-GCM 加密，密钥由你的口令或 12 词助记词派生
- 保存到你自己选择的位置（"文件" App、AirDrop 等）
- 永远不会被发送给我们或任何第三方

如果你丢失了口令或助记词，我们没有任何方式可以替你恢复。

## 7. 儿童隐私

Whisker 不面向 13 岁以下儿童。我们不会有意收集儿童的个人信息——事实上我们不会有意收集任何人的个人信息。

## 8. 你的权利

由于我们不持有你的任何个人数据，关于"访问、更正、导出、删除数据"的请求应在你自己的设备上完成：
- 通过应用内的备份功能导出全部记录
- 卸载应用即可删除全部记录（加密数据库随应用沙盒一并删除）
- 卸载后重装即可重置 onboarding 状态

如果你在欧盟/英国（适用 GDPR）或加州（适用 CCPA）：我们既不是你个人信息的"数据控制者"，也不是 CCPA 定义的"商业实体"，因为我们没有在任何由我们运营的系统中收集或处理你的数据。

## 9. 政策变更

如果未来 Whisker 的架构发生变化，涉及收集或传输你的数据（例如新增同步服务器），我们会更新本隐私政策，并在应用内提示你，待你确认后新行为方可生效。

## 10. 联系我们

关于本政策的问题：shadeless@126.com
