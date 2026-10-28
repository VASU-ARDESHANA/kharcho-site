# Privacy Policy for Kharcho

**Last updated:** October 28, 2026  
**Developer:** VASU ARDESHANA  
**Email:** [developer.vatech@gmail.com](mailto:developer.vatech@gmail.com)  
**Location:** India 🇮🇳  

---

## Introduction

**Kharcho** ("we", "us", "Kharcho") is a personal expense, loan, budget, and group split tracking app built and operated by **VASU ARDESHANA**, an independent developer based in India.

We built Kharcho with one core principle that everything else flows from: **your money data belongs to you.** We store it solely to run Kharcho for you, and nobody else ever gets a copy.

This Privacy Policy explains, in plain and transparent language, what data Kharcho handles, where it lives, and what control you have over it. If anything here is unclear, please email us directly at [developer.vatech@gmail.com](mailto:developer.vatech@gmail.com).

---

## 1. The Short Version

- **Your personal finance data** — your expenses, income, monthly budgets, loan contacts, loan transactions, EMIs, categories, split groups, and custom payment method names — lives with your Kharcho account on our secure cloud database powered by Appwrite. It is stored solely so that signing in on any Android device brings all your records back.
- **No one at Kharcho reads, accesses, or analyzes your personal entries.**
- **We never sell, rent, monetize, or share your data with advertisers or third parties — ever.**
- **We do not train AI models on your financial records.**
- **Offline First:** A complete working copy lives in a sandboxed local database on your phone so Kharcho is instantaneous and works without an internet connection.
- **You can delete everything we hold about you** at any time, directly inside the app or by emailing us.

---

## 2. Data We Handle

### 2.1 Data You Provide Directly & App Features
- **Your Name, Email Address & Phone Number:** Provided during registration or login so Kharcho can identify your account, secure sessions, deliver password recovery, and allow group members to identify you in shared split groups.
- **Expense Records:** Amount, title, category, payment method (e.g. Cash, UPI, Card), transaction date, and optional notes.
- **Shared Split Groups & Group Expenses:** When you create or join a shared split group, your chosen group nickname, registered phone number, and expenses, notes, and settlements created in that group are shared with other members of that specific group to facilitate group ledger calculations and debt resolution. Group data is strictly restricted to participants of that group and is never public.
- **Micro-Savings (Spare Change):** Calculated round-up amounts and your all-time virtual piggy savings total stored with your account.
- **Loan & Lending Records:** Contact names, phone numbers, amounts borrowed or lent, transaction history, due dates, and settlement notes.
- **EMI & Budget Data:** Loan amounts, interest rates, tenure in months, computed installment schedules, and monthly category budget limits.
- **Voice Expense Dictation (Microphone):** If you use the Voice Expense feature, audio is captured exclusively while you hold or tap the microphone to convert your spoken words (Gujarati, Hindi, or English) into an expense entry via Android's on-device speech recognition service. Raw audio is never stored on disk or uploaded to our servers.
- **Smart Receipt, UPI Screenshot & QR Code Scanning (Camera & ML Kit):** If you take a receipt photo, pick a UPI payment screenshot, or scan a split group QR code, text and code recognition runs 100% locally on your device via Google ML Kit / ZXing. Payment screenshots and camera feeds are processed transiently in memory and are never uploaded to any server or cloud storage.
- **Contact Picker (Optional):** When creating or selecting a borrower/lender in the Loan manager, you may tap "Pick from Contacts" to select a contact name and phone number. Kharcho only reads the specific contact you select and never uploads or scans your entire address book.
- **Location (Optional):** If you tap the map location pin for an expense, Kharcho saves the coordinates and place name to show where you spent your money. We never track your location in the background.

### 2.2 Third-Party Services & Advertising Disclosures
- **Google AdMob:** Kharcho displays non-intrusive advertisements provided by Google Mobile Ads (AdMob) to support free app maintenance. Google AdMob may collect and process pseudonymous identifiers such as the Google Advertising ID (AAID), IP address, and coarse device diagnostic data for ad serving, frequency capping, and fraud prevention. You can reset or opt out of personalized advertising at any time in **Android Settings → Google → Ads**.
- **Firebase Cloud Messaging (FCM):** Used to deliver push notifications, group expense updates (via group topics), and background data sync pings to your device token.
- **What We Do NOT Collect:** We do NOT collect bank account numbers, full debit/credit card numbers, CVVs, UPI PINs, netbanking passwords, or OTPs. Kharcho does not connect to bank accounts or payment gateways.
- **No Biometric Harvesting:** Biometric screen unlock (Fingerprint / Face) is processed 100% locally by Android's hardware Keystore and never transmitted.

---

## 3. Where Your Data Lives

1. **On your phone:** In private, sandboxed app storage using local SQLite and encrypted preferences. This ensures the app opens immediately, operates offline, and preserves your battery.
2. **On our secure cloud backend (Appwrite):** All cloud records are transmitted over industry-standard HTTPS / TLS 1.3 encryption and stored in secure cloud databases. This allows you to restore your complete financial history whenever you change or reset your phone.
3. **If you uninstall Kharcho:** The local copy on your device is deleted by Android. Your cloud data remains safely attached to your account so you can log back in. Deleting your account permanently erases both.

---

## 4. Notifications & Reminders

- **Daily Habit Streak Reminders:** Local reminders (e.g., reminding you at 9:00 PM to log your daily expenses) are scheduled directly on your phone using Android's native `AlarmManager`. These alarms operate completely offline without server interaction.
- **Loan Due Alerts:** Alerts for upcoming loan due dates are scheduled locally on your device.
- **Firebase Cloud Messaging (FCM):** We use Google FCM solely to send silent data sync pings and important account notifications to your device token. Firebase is used for notification delivery only — no Firebase Analytics tracking is used.

You can turn off notifications at any time in **Profile → Notifications** or in **Android Settings → Apps → Kharcho → Notifications**.

---

## 5. Security & Anti-Cloning Protection

- **Encrypted Transmission:** All communication between Kharcho and our Appwrite backend is enforced over HTTPS with TLS 1.3 encryption.
- **Screen Protection:** You can enable "Hide Balances" in Profile Settings to mask sensitive numbers on the dashboard.
- **App Integrity:** Kharcho includes automated anti-cloning security to prevent unauthorized execution in untrusted virtual environments, protecting your financial data against memory tampering.

---

## 6. Your Rights & Data Deletion (DPDP & GDPR Compliant)

You have full ownership of your data at all times:

1. **Access & View:** Every record Kharcho stores is visible to you inside the app.
2. **Edit & Modify:** You can edit or change any expense, loan, EMI, or category at any time.
3. **Export:** You can generate and export clean PDF reports of your expenses and loan records directly from the app.
4. **Complete Data Deletion:**
   - You can request full account and data deletion by sending an email from your registered address to:
     **[developer.vatech@gmail.com](mailto:developer.vatech@gmail.com)** with the subject line `Data Deletion Request - Kharcho`.
   - Once verified, your account and all associated records (profile, expenses, loans, EMIs, and attachments) will be permanently purged from our servers within 30 days.

---

## 7. Children's Privacy

Kharcho is not intended for use by children under the age of 13. We do not knowingly collect personal information from children. If you believe a child has provided us with personal information, please notify us at [developer.vatech@gmail.com](mailto:developer.vatech@gmail.com) and we will promptly delete it.

---

## 8. Changes to This Policy

If we update this Privacy Policy, we will update the "Last updated" date at the top and notify users within the app. Changes will not apply retroactively to data collected prior to the update.

---

## 9. Contact Us

For privacy questions, data requests, or feedback:

- **Developer:** VASU ARDESHANA  
- **Email:** [developer.vatech@gmail.com](mailto:developer.vatech@gmail.com)  
- **Country:** India 🇮🇳
