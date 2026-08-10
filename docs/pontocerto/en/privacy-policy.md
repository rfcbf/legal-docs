# Privacy Policy for PontoCerto

**Effective date:** August 10, 2026
**Last updated:** August 10, 2026

PontoCerto is a personal work time-tracking and hours-calculation app developed by Renato Ferraz ("developer," "we"). This Privacy Policy explains what data the app handles, where it is stored, and how you can control it.

By using PontoCerto, you agree to the practices described here. If you do not agree, do not use the app.

---

## 1. Quick summary

- PontoCerto **has no server of its own**. There is no developer-operated backend receiving, processing, or storing your data.
- Your clock-in/out records, schedules, cycles, and alarms stay **on your device** (Core Data) and, if iCloud sync is enabled, are synced **exclusively through your own personal iCloud account** (CloudKit — private container `iCloud.br.com.renatoferraz.pontocerto`) to keep your iPhone, iPad, Mac, Apple Watch, and Widget in sync.
- The developer **has no access** to this data. It travels only between your own devices through Apple's infrastructure, protected by your personal iCloud account.
- **We do not use** third-party SDKs, analytics, tracking, or advertising.
- **We do not sell, rent, or share** data with anyone, because we never receive it in the first place.

---

## 2. Data handled by the app

### Data you enter

- Clock-in/clock-out times, entered manually or via alarm.
- Work schedule, monthly cycle, holiday, and break configuration.
- Alarm and notification preferences.

### Data collected automatically by the system (not by the developer)

- The app uses AlarmKit and local iOS/watchOS notifications to trigger schedule alerts — this scheduling data stays within your own device's operating system.
- No advertising identifier, aggregated usage data, or telemetry is collected.

### What the app does NOT collect

- No account creation required (sign-in relies solely on the Apple ID already configured on your device, for iCloud use).
- We do not collect email, name, location, contacts, photos, health data, or any personal identifier beyond what CloudKit itself requires, which is managed by Apple.
- We do not track you across other apps or websites.

---

## 3. How data is stored and synced

- **Local storage:** Core Data, within the protected storage of iOS/iPadOS/macOS/watchOS itself.
- **Sync:** CloudKit, using your iCloud account's **private container**. This means synced data only ever exists within the space of your own Apple ID — the same mechanism used by apps like Reminders or Notes.
- **Widget and Apple Watch:** read the same data through a local App Group (`group.br.com.renatoferraz.pontocerto`) and the private CloudKit container — nothing leaves your own Apple ecosystem.
- The developer does not operate, access, or have any technical means to access the contents of your private CloudKit container.

---

## 4. Data sharing

We do not share data with third parties, because we never receive it. The only "party" involved in storage and sync, besides your own device, is Apple's infrastructure (iCloud/CloudKit), governed by [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

We may disclose information only if required by law or a valid court order — which, in practice, is not technically possible for data that never passes through the developer.

---

## 5. Security

- On-device data follows the standard encryption of iOS/macOS/watchOS.
- Data synced via CloudKit follows Apple's own encryption in transit and at rest.
- No storage method is 100% secure, but since there is no developer-operated server involved, the risk surface is limited to your own device and Apple account — whose security is your responsibility (strong password, two-factor authentication).

---

## 6. Your rights and control (GDPR / general)

Because the app never sends data to developer-operated servers, your control over your data is, in practice, total and direct:

- **Access and export:** all your data is visible in the app itself, at any time.
- **Correction:** you can edit any record directly in the app.
- **Deletion:** deleting the app or the records within it removes the data from your device; turning off iCloud sync for the app (device Settings > [your name] > iCloud) removes the data from CloudKit.
- **Portability:** your data lives in your own iCloud account, fully under your control, independent of the developer.

Since we are not the controller of a central database, there is no data of ours to delete upon request — deletion happens directly through you, in the app or in your Apple ID settings.

If you are located in the European Economic Area, note that the developer does not act as a data controller for your personal data in the sense of the GDPR, since no personal data is transmitted to or processed by the developer's own systems.

---

## 7. Children

PontoCerto is not directed at children. It is a work-schedule tracking app intended for users who are 18 or older, or of legal working age in their jurisdiction.

---

## 8. Changes to this policy

We may update this Privacy Policy as the app gains new features that change how data is handled. The "Last updated" date at the top will be revised, and material changes will be communicated within the app.

---

## 9. Contact

Questions about this Privacy Policy:

- **Email:** renatodesenv@icloud.com
- **Developer:** Renato Ferraz
