# CalcJuros Privacy Policy

**Effective date:** October 27, 2026
**Last updated:** October 27, 2026

CalcJuros is a financial calculator for iPhone, iPad and Apple Watch, developed by Renato Ferraz ("developer", "we"). This Privacy Policy explains what data the app handles, where it is stored and how you can control it.

By using CalcJuros, you agree to the practices described here. If you do not agree, do not use the app.

---

## 1. Quick summary

- The app **does not require an account**. Your calculations, clients, checks, loans and profile stay **on your device** and sync **through your own iCloud account** (CloudKit, private container `iCloud.br.renatoferrazdf.calcjuros`). The developer **has no access** to this data.
- Sign-in with an old account (Firebase, by Google) exists **only to import** data from previous versions of the app.
- The app includes **UAPPKit**, the developer's own component that shows About, What's New, Roadmap and Feedback. Some profile data goes to UAPP to identify you in these features (section 4).
- Subscriptions are sold and charged by **Apple**. We do not receive your payment details.
- We **do not sell or rent** your data, do not show ads and do not track you across other companies' apps.

---

## 2. Data handled by the app

### Data that stays only on your devices and in your iCloud

- **Calculations** you save, with the values you entered and the results.
- **Profile:** the name, photo, email and mobile number you choose to fill in.
- **Clients, checks and loans** you add, which may include other people's names, addresses, phone numbers, CPF (Brazilian tax ID), notes, amounts, dates and installments.
- **Preferences:** favorites, language, reminder times and app lock settings.
- Encrypted **backups**, saved on the device or wherever you choose to export them.

### Data sent to UAPP

- **When you open the app with a profile:** the profile identifier, email and name, so that suggestions, votes and replies in Feedback and Roadmap are linked to you.
- **When you send a suggestion, comment or vote:** the text, any images you attach and your author identification (name, email, mobile number and profile photo).
- **When you open UAPPKit screens:** the app requests the information from the UAPP server, stating which app and language. As with any internet access, the server receives the connection's IP address.

### Data handled by Google (Firebase), only for people importing old data

- **When you sign in with your old account** (email and password, Google or Apple): Firebase Authentication confirms the account, and the app reads from Firestore that account's calculations, clients, checks and card providers to copy them to your iCloud. The app records on the old server that the import was completed.
- **Firebase Analytics:** the app includes the Firebase Analytics SDK, which records technical events (for example, a completed import) and may collect an app instance identifier, device and usage data, in aggregate. This data is not used for advertising.

### Other services the app queries

- **Central Bank of Brazil:** inflation adjustment and compared returns fetch public index series (IPCA, INPC, IGP-M, Selic, CDI) from the Central Bank API. No personal data is sent.
- **Salary tables:** INSS and income tax tables are read from a developer database hosted by Supabase. No personal data is sent.
- **Connectivity check:** to know whether there is internet, the app makes simple requests to public Google addresses. No personal data is sent.

In these requests, as with any internet access, the servers receive the connection's IP address.

### Data handled by Apple

- **Purchases and subscriptions:** made through the App Store. Apple processes the payment; the app only receives the subscription confirmation and the purchase receipt, which is also used to recognize people who bought a previous version.
- **Notifications:** due date reminders are scheduled on the device itself.
- **Face ID and Touch ID:** verification is done by the system; the app only learns whether it succeeded. The lock PIN stays on the device.
- **Camera and photos:** used only when you scan a boleto barcode or choose your profile photo. Boleto images are not stored.

### What the app does NOT collect

- Location, address book contacts, health data, browsing history or advertising identifier.
- Your calculations, clients, checks and loans never go to UAPP or to the developer.

---

## 3. How data is stored and synced

- **Local storage:** Core Data, in the protected storage of iOS, iPadOS and watchOS.
- **Sync:** CloudKit, in your iCloud account's **private container**, the same mechanism used by apps such as Reminders and Notes. Some preferences use iCloud key-value storage.
- **Widgets and Apple Watch:** read the same data through a local app group and the connection between iPhone and watch.
- The developer does not operate, access or have any technical means to access the content of your private CloudKit container.

---

## 4. Data sharing

UAPP is the developer's own platform for receiving suggestions, publishing news and keeping the apps' roadmaps. Data sent to it is stored on UAPP servers, hosted by Supabase, and used only to:

- show your suggestion or comment on the CalcJuros Roadmap, with your name and photo as the author;
- reply to you and let you know about the progress of your suggestion.

Suggestions, comments and votes published on the Roadmap can be seen by other people who use the app, along with the author's name and photo. Do not include sensitive data in these texts. This data is also handled under the [UAPP Privacy Policy](https://uapp.renatoferraz.net/politica-de-privacidade).

Google (Firebase) handles the data described in section 2 under the [Google Privacy Policy](https://policies.google.com/privacy). Apple takes part in storage (iCloud) and purchases (App Store), governed by the [Apple Privacy Policy](https://www.apple.com/legal/privacy/).

Other than that, we do not share data with third parties. We may disclose information if required by law or a valid court order.

---

## 5. Third-party data you add

The client data you add (such as names, phone numbers, addresses and CPF) stays only on your device and in your iCloud. Regarding that data, **you are the controller** under the LGPD: you decide what to add, how to use it and when to delete it. The developer neither accesses nor uses this data. When you send a payment request through WhatsApp or a message, the content leaves your device through the app you choose.

---

## 6. Security

- Data on the device follows the standard encryption of iOS, iPadOS and watchOS, and the app can be locked with a PIN, Face ID or Touch ID.
- Backups created by the app are encrypted.
- Data synced through CloudKit follows Apple's encryption in transit and at rest.
- Communication with UAPP, Firebase and the other APIs uses encrypted connections (HTTPS).
- No storage method is 100% secure. Protect your Apple account with a strong password and two-factor authentication.

---

## 7. Your rights and control (LGPD)

- **Access and correction:** your calculations, clients and profile are visible and editable in the app.
- **Export:** a backup file creates a copy of your data that you can keep or move to another device.
- **Deleting app data:** in Settings, deleting your profile removes the profile, clients, checks and calculations from this device and from your iCloud. Deleting items in the app or uninstalling it also removes data from the device.
- **Deleting UAPP and old account data:** to delete suggestions and comments you sent, or your old account's data on Firebase, write to the email below. Requests are handled within the period set by the LGPD.
- **Revoking permissions:** camera, photos, notifications and Face ID can be turned off at any time in the system Settings.

For questions about the processing of personal data under Brazil's General Data Protection Law (LGPD, Law No. 13,709/2018), contact us at the email below.

---

## 8. Children

CalcJuros is not directed at children. It is an app for financial calculations and client book tracking, intended for people aged 18 or older.

---

## 9. Changes to this policy

We may update this Privacy Policy when the app gains features that change how data is handled. The "Last updated" date at the top will be revised, and relevant changes will be announced in the app.

---

## 10. Contact

Questions about this Privacy Policy:

- **Email:** renatodesenv@icloud.com
- **Developer:** Renato Ferraz

[Versão em português](../politica-privacidade.md)
