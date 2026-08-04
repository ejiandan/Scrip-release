# Scrip User Manual

- Applies to: Scrip 1.0.0
- Requires: iOS 15.0 or later
- Language: English (简体中文版本：`UserManual.zh-CN.md`)

---

## 1. What is Scrip

Scrip is a local-first tool for managing structured information and frequently used text, paired with a custom system keyboard. You can organize your commonly used **Info**, **URLs**, and **Templates** into categories, then insert them into the input field of any app with a single tap — no more repetitive copy and paste.

- Design philosophy: built from the smallest details, guided by simplicity; gather every thought, compose with a tap.
- All your data is stored locally on your device and never uploaded to any server.

---

## 2. Core Concepts

### 2.1 Category

Scrip organizes content into three kinds of categories:

| Category | Purpose | Example |
| --- | --- | --- |
| Info | Structured field data | Recipient, address, ZIP, phone, email |
| URL | Frequently used links | Homepage, admin panel, docs |
| Template | Templated text with placeholders | Support reply templates, greetings |

You can add, rename, delete, and reorder categories in **Settings → Category Management**.

### 2.2 Entry

Each category contains a number of **entries**. An entry is one group of content (for example, a full set of address fields, one URL, or one template). It has a name so you can find and insert it quickly.

### 2.3 Separator

When creating an **Info** entry, Scrip splits a block of text into multiple fields using the **separator** you choose (newline, comma, vertical bar, etc.). Common separators can be managed in **Settings → Separator Management**.

### 2.4 Replacement Value

A **Template** entry may contain placeholders (such as `%SCRIP1%`, `%SCRIP2%`). Before inserting a template from the keyboard, you can pick a **replacement value** for each placeholder, and Scrip substitutes it automatically on output. Replacement values are managed in **Settings → Replacement Value Management**.

---

## 3. Getting Started

### 3.1 Add Content

1. Tap **Add** at the bottom center of the home screen.
2. Choose a category (Info / URL / Template).
3. Enter content by category:
   - **Info**: paste or type a block of text and choose a separator to split it into fields.
   - **URL**: enter a URL; if **URL Auto-Processing** is enabled, the title, metadata, and a page snapshot are fetched in the background.
   - **Template**: enter templated text and insert placeholders for later substitution.
4. Give it a name and save.

### 3.2 Find and Manage

- **Search**: the search box at the top center of the home screen performs full-text search across entry names and content.
- **Filter / Sort**: available at the bottom left and right of the home screen.
- **Edit / Delete**: swipe an entry in the list to edit or delete it.

---

## 4. Enable and Use the Scrip Keyboard

Due to iOS security restrictions, the app cannot enable the keyboard for you — you need to turn it on once in system settings.

### 4.1 Enable the Keyboard

1. Open the **Usage Guide** and tap **Open System Settings**.
2. Go to **Keyboards → Keyboards → Add New Keyboard…**.
3. Select **Scrip** from the list to add it.
4. To use features such as reading the clipboard, open **Scrip** and turn on **Allow Full Access**.

### 4.2 Bring Up and Insert

1. Tap any input field to bring up the keyboard.
2. Long-press the globe icon 🌐 at the bottom-left, or tap it repeatedly, to switch to the **Scrip** keyboard.
3. Switch categories along the top, then tap an entry to insert its content at the cursor.
4. For templates with placeholders, choose replacement values above the entry first, then tap to output.

### 4.3 Common Keyboard Actions

- **Tap to insert**: tap any entry content to insert it into the target field.
- **Undo / Redo**: undo or redo the most recent tap insertion.
- **Backspace**: tap to delete one character; press and hold for continuous deletion, just like the system keyboard.
- **Font scaling**: use **+ / −** to adjust the overall text size inside the keyboard (remembered across sessions).
- **Open Scrip / Manage replacement values**: shortcuts inside the keyboard let you jump back to the main app to manage content.

---

## 5. Security and Unlocking

Scrip protects your data with the device's biometrics (Face ID / Touch ID):

- When the device supports biometrics and data exists, the app UI requires authentication after moving to the background, locking the screen, or a cold launch.
- Before the keyboard shows data in a **third-party app** for the first time, you must authorize it via biometrics in the main app. Authorization uses a one-time ticket, so switching to another app or reopening requires re-authorization.
- When the keyboard is invoked **inside the Scrip app** (app in the foreground and unlocked), no repeated authentication is needed.
- **Settings → Security** offers **Unlock and Sync with Face ID** and **Lock Now**.

> Biometric authentication happens entirely on your device. Scrip never stores or uploads your biometric data.

---

## 6. URL Processing

- Enable **URL Auto-Processing** in **Settings → URL**.
- Once enabled, adding a URL causes Scrip to **visit the URL you entered** in the background to fetch the page title and metadata and generate a snapshot for easier recognition and browsing.
- You can track progress in **URL Tasks** from the main menu.

> This is the only scenario in which Scrip actively accesses the network, and it only visits URLs you entered yourself — with no tracking or third-party analytics.

---

## 7. Usage Statistics

The **Statistics** item in the main menu shows privacy-free usage counters to help you understand your own usage:

- Number of app opens
- Number of entries added (one addition counts as one)
- Number of entries deleted
- Number of keyboard insertions (tapping an entry and writing it to the target counts as one)
- Number of characters inserted via the keyboard
- Statistics start time and last update time

> Statistics contain no location, device identifiers, input content, or any other private information — only usage counts.

---

## 8. Settings Overview

| Group | Item | Description |
| --- | --- | --- |
| General | Appearance | System / Light / Dark |
| General | Language | System / English / 简体中文 / 繁體中文 / 日本語 / 한국어 / Español / Deutsch / Français (the interface refreshes instantly after switching) |
| General | Category Management | Add, rename, delete, reorder categories |
| Info | Separator Management | Manage common separators |
| URL | URL Auto-Processing | Fetch title and more in the background when adding a URL |
| Template | Replacement Value Management | Manage placeholder replacement values |
| Security | Unlock & Sync with Face ID / Lock Now | Biometrics and manual locking |

---

## 9. Data and Privacy

- All content data is stored locally on the device (SQLite database).
- The main app and the keyboard share a **read-only** data snapshot via an App Group; the keyboard does not record what you type.
- Scrip does not integrate any third-party analytics, advertising, or tracking SDKs, and does not collect location data.
- See the *Privacy Policy* (`PrivacyPolicy.en.md`) and the *User Agreement* (`UserAgreement.en.md`) for details.

---

## 10. FAQ

**Q: I can't switch to the Scrip keyboard.**
Make sure you added **Scrip** in **System Settings → Keyboards**, and enable **Allow Full Access** if you need clipboard reading.

**Q: The keyboard shows no content and asks me to unlock.**
Return to the main Scrip app and complete a Face ID authorization once, then try again. No repeated authentication is needed when the keyboard is invoked inside the Scrip app.

**Q: The URL title never appears.**
Make sure **URL Auto-Processing** is enabled and you have network connectivity. Check progress in **URL Tasks**.

**Q: Is my data synced to the cloud?**
No. Scrip is a local-first app, and your data stays on your device.
