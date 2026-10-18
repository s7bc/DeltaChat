# Delta Chat 2.62.41.1 — Custom Build

## What's new compared with Delta Chat 2.62.0

This document describes the additions in **Delta Chat 2.62.41.1**, our modified build based on the upstream **2.62.0** release.


### 1. Email accounts and IMAP folders

- **IMAP folder selection:** choose the folder to be monitored for each configured email account/relay, rather than being limited to a predetermined folder.
- The setting allows the user to control which incoming messages Delta Chat processes.

### 2. Message formatting

- **Markdown rendering** in messages.
- **Mathematical expressions** rendered using KaTeX.
- Improvements to multiline-message handling, including preservation of line breaks in the Android interface.

### 3. Images

- An **Original Quality** option for sending images without the application's normal quality reduction.
- The option is displayed first in the image-quality choices, with a simplified label.

### 4. Contacts and invitations

- Add a contact by **QR code** or by **email address**.
- Enter or paste **multiple email addresses** at once; addresses are extracted even when separated by spaces, newlines, or other non-email characters.
- **Manual invitation** controls: invitations can be sent explicitly rather than automatically when an address is entered.

### 5. Encryption and plain email

- A **forced-encryption setting per email account/relay**.
- Support for sending and receiving ordinary **unencrypted email when permitted by the selected settings**, instead of requiring encryption for every message.
- Encryption requirements remain explicit so that users can distinguish protected conversations from plain email.

### 6. Pinned messages

- A pinned-message banner **overlaid at the top of the conversation**, with chat messages scrolling beneath it rather than being replaced by an opaque, separate panel.
- A **three-line preview** of the pinned message.
- **Image thumbnails** in the preview when a pinned message contains an image, instead of a generic image icon.
- A **Pinned Messages** list for reviewing pinned items.
- Selecting a banner or list entry navigates to the **original message in the conversation**.
- Support for managing pins, including unpinning messages.

### 7. vCard contact import and export

- **Profile context menu:** import contacts from one `.vcf` file or export all contacts belonging to the selected profile into one `.vcf` file.
- **Individual contact context menu:** **Export Contact** appears below **View Profile**.
- **Group context menu:** **Export Contacts** writes the group participants into a single `.vcf` file, excluding the current user and duplicate entries.
- Standard file-open and file-save dialogs are used.
- vCard processing uses **existing Delta Chat core functionality**; no changes to the core contact-import or identity-merging algorithms were introduced for this feature.

**Important:** importing a vCard is not a blanket overwrite-by-email operation. Matching and updating follow the core's existing rules, including handling of cryptographic identities and key material. Importing contacts does not guarantee that every previous verification or invitation state will be restored.

## Platforms

| Platform | Version | Notes |
| --- | --- | --- |
| Windows | 2.62.41.1 | Desktop application; installer and portable packaging are build targets. |
| Linux | 2.62.41.1 | Desktop application; Debian 12 `.deb` and AppImage are build targets. |
| Android | 2.62.41.1 | Android-specific UI adaptations; targets include ARMv7, ARM64 and x86. |


## Scope and compatibility

- Changes are intended to remain compatible with the corresponding Delta Chat 2.62-based data and protocols.
- The vCard functionality is implemented at the user-interface level using pre-existing core APIs; it does **not** redefine how the core matches contacts or stores cryptographic keys.
- Available features may vary with platform and the exact build revision. Check the built application before treating this list as a verified release checklist.



You can donate to the development of an improved version of Delta Chat

bitcoin:BC1QMXNGJMRAQXJ5LY7UAMRC4C7Z7DEJUE3RRQZGCD

<img width="340" height="340" alt="изображение" src="https://github.com/user-attachments/assets/88b54ddf-35dc-4da1-8402-831dbbfa49f0" />
