# Scrip Privacy Policy

- Applies to: Scrip 1.0.0
- Effective date: 2026-07-31
- Language: English (简体中文版本：`PrivacyPolicy.zh-CN.md`)

Scrip ("the App") respects and protects your privacy. This policy explains how the App handles information related to you. Please read it carefully before use.

---

## 1. Core Principles

- **Local-first**: the App is a local-first tool. All content data you enter is stored only on your device.
- **No server accounts**: the App neither offers nor requires account registration, and does not upload your data to our servers.
- **No tracking**: the App does not integrate any third-party analytics, advertising, or tracking SDKs, and does not collect location data or device identifiers for tracking.

---

## 2. How We Handle Information

### 2.1 Content You Enter

The info, URLs, templates, categories, separators, replacement values, and similar content you create in the App are stored on your device in a local database (SQLite). We cannot access this content.

### 2.2 Data Sharing Between the App and the Keyboard

So that the custom keyboard can display your content, the App writes your data as a **read-only snapshot** into a shared App Group container, after your authorization, for the keyboard extension to read.

- This shared area exists only locally on your device.
- The keyboard extension **only reads** the shared data and **does not record or upload** anything you type on the keyboard.
- When the interface is locked, the App clears the plaintext content data from the shared area.

### 2.3 Biometrics (Face ID / Touch ID)

The App uses the system-provided biometrics for on-device unlocking and authorization.

- Authentication is performed entirely by the system on your device.
- The App does not obtain, store, or upload your biometric data.

### 2.4 Network Access (URL Processing)

When you enable **URL Auto-Processing** and add a URL, the App **visits the URL you entered** in the background to fetch the page title and metadata and generate a snapshot.

- This network access only targets **URLs you entered yourself**.
- The App does not send your personal information to any third party as a result, and does not use it to track or analyze your behavior.
- If you prefer no network access, you can disable this feature in **Settings → URL**.

### 2.5 Usage Statistics

The App records privacy-free usage counters locally (such as number of app opens, entries added/deleted, keyboard insertions and characters, and statistics start/update times).

- These statistics are stored only on your device for your own reference.
- The statistics contain **no** location, device identifiers, input content, or any other private information.

### 2.6 Clipboard and Camera/Photos

- If you enable **Allow Full Access** for the keyboard, the keyboard can read the clipboard to assist input; such data is used only for the current operation and is not retained or uploaded.
- If you use text recognition (OCR) when entering info, the image is processed on-device only and is not uploaded.

---

## 3. Storage and Security

- Your data is stored locally on the device and protected by the device's own security mechanisms.
- The App further reduces the risk of others viewing your data through biometrics and interface locking.
- Please keep your device secure and back up important data promptly.

---

## 4. Information Sharing and Disclosure

- The App does not sell, rent, or otherwise provide your personal information to third parties.
- Unless explicitly required by law, the App does not disclose your data; and because the data resides only on your device, we generally have no means to access it.

---

## 5. Children's Privacy

The App does not collect any personal information from children, nor does it provide an account system that requires personal information.

---

## 6. Your Rights

Because the data resides entirely on your device, you have full control over your data:

- You may add, edit, or delete content in the App at any time.
- Uninstalling the App removes the related data stored on your device.

---

## 7. Policy Updates

This policy may be updated as features evolve. Significant changes will be communicated through in-app notices or documentation updates, and the updated policy takes effect on the date it is published.

---

## 8. Contact Us

If you have any questions about this Privacy Policy, you can contact us through the contact information provided on the App's distribution channel.
