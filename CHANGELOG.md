# 📜 Kharcho - Release Notes & Changelog

All notable changes, new features, UI improvements, and architectural updates for Kharcho are documented in this file.

---

## 🚀 [v1.0.6] - October 2026

### ✨ Major Improvements & Architecture Fixes
- **Split Expense Correction & Deletion**:
  - Added support for deleting erroneous split expenses locally and on cloud servers.
  - Automatically recalculates all members' dynamic balances and total group spend in real time.
- **Robust Pending Member Isolation**:
  - Filtered out pending members from group expense split chips, payer selector, and settlement dialogs.
  - Restricted action permissions (FAB, settlements) for users whose join requests are pending admin review, with informative status badges.
- **Paise Division Precision**:
  - Implemented remainder-distribution algorithm to eliminate 1-paisa division drift when splitting odd amounts among members.
- **Unauthenticated Deep Link QR Recovery**:
  - Google Lens / camera QR scans by logged-out users safely preserve the invite code and route to authentication, automatically launching the join sheet once signed in.
- **Offline Cache Fallbacks**:
  - Hardened Expense and Loan queries with resilient `LocalDataCache` disk cache fallbacks when offline or on unstable networks.
- **Onboarding Cold-Sync**:
  - Seamlessly routes approved accounts through `DataSyncActivity` to prime local caches.
- **Online-First Release Notes**:
  - Integrated GitHub live markdown viewer for release notes and changelog with offline HTML fallback.
  - Removed intrusive startup popups from main dashboard in favor of on-demand viewing in Profile.

---

## 👥 [v1.0.5] - October 2026

### ✨ Group Splits & Governance
- **Custom Group Nicknames**:
  - Set custom nicknames when creating, joining, or managing split groups without altering global account names.
  - Edit your nickname directly from the group member list with instant local and cloud synchronization.
- **Deep Link & QR Code Invites**:
  - Google Lens / camera scan-friendly QR codes with `https://kharcho.app/join?code=XYZ` and `kharcho://join?code=XYZ` deep link intent filters.
  - One-tap invite code clipboard copy and native Android share sheet integration.
- **Group Governance & Permissions**:
  - Admin approval requirement (`requiresApproval`) for new member join requests.
  - Leave Group functionality with settled-debt validation (cannot leave with non-zero balance).
  - Archive / Close and Delete Group controls for group admins.
- **Group Activity Audit Log**:
  - Real-time activity timeline tracking expense creations, payments, settlements, and member changes.
  - Pull-to-refresh synchronization with secure cloud backend.
- **Online-First Legal Policies**:
  - Linked Privacy Policy and Terms & Conditions directly to GitHub repositories with offline HTML asset fallbacks.

---

## 🚀 [v1.0.4] - October 2026

### ✨ Major Features
- **Quick Settings Notification Tile (`QuickLogTile`)**:
  - Pull down the Android notification shade to access the "Quick Log" tile.
  - Tap once from anywhere (even when Kharcho is closed) to instantly open the Quick Type expense bottom sheet.
  - Full support for Android 14+ (`UPSIDE_DOWN_CAKE`) with `PendingIntent` and backward compatibility on older versions.

- **Dedicated Category Budgets & Categories Screen**:
  - Brand new dedicated management screen (`CategoryBudgetsFragment`) accessible from Profile and Home.
  - Set target spending limits per category (Groceries, Dining, Fuel, Rent, Shopping, etc.).
  - Flexible custom sections (Personal, Household, Other, Bills, Travel, etc.).
  - Over-allocation warning banner: Automatically alerts you when category allocations exceed your overall monthly budget.
  - Dedicated Monthly Budget editing in Profile with centered Material dialog.
  - Synced with cloud database and offline-first disk cache.

- **Daily Logging Streak (Gamification)**:
  - "🔥 X-Day Streak" badge displayed directly on the Dashboard and Profile header.
  - Real-time habit streak tracker that counts consecutive days of logging expenses.
  - Interactive streak status popup showing whether today's expense has been logged (`✅ Logged today!` or `⏳ Pending`).

- **Spending Story (Monthly Rewind / Wrapped)**:
  - Spotify-Wrapped style visual spending story for each month.
  - 5 interactive slides:
    1. **Monthly Spend Overview**: Total spend, expense count, and daily average.
    2. **#1 Category Champion**: Top spending category, emoji icon, and % of total monthly budget.
    3. **Peak Spending Day**: Date of highest expenditure and the title of the largest single purchase.
    4. **Top Merchant / Store**: Most frequently visited merchant and total spent.
    5. **Gullak & Health Score**: Spare change savings and Financial Health score out of 100.
  - Integrated sharing sheet to share your monthly rewind on WhatsApp, Telegram, or social media.
  - Accessible directly via the "✨ View Spending Story" button on the Dashboard and from Profile reports.

### 🎨 UI & UX Refinements
- **Material 3 Center Dialogs**:
  - Converted Budget setup and Quick Loan transactions from bottom sheets into clean, centered Material 3 dialogs.
  - Soft-input pan adjustments ensuring keyboards never overlap bottom navigation or form inputs.
- **Zero Avatars & Offline Emojis**:
  - Completely purged all external avatar services in favor of native Unicode emojis (🛒, 🍔, ⛽, etc.) and letter badges.
  - Zero network overhead and 100% offline icon support.
- **In-App What's New & Changelog Viewer**:
  - Automatic release dialog shown on first app launch after an update.
  - Clickable version label in Profile to review release notes and changelog at any time.
- **Join Group Sheet Keyboard Fix**:
  - Wrapped `JoinGroupBottomSheet` in a scrollable view and fixed inset padding so the code input and buttons remain visible when the keyboard is open.
- **Loan Person Page Bottom Bar Optimization**:
  - Removed excessive bottom padding under the Gave/Got buttons, making the bottom card compact and maximizing screen real-estate for the transaction ledger.
- **Dashboard Quick Type Button**:
  - Added a dedicated 1-tap "⌨️ Quick Type" shortcut in the Dashboard header right next to the streak badge.

### 🐛 Bug Fixes & Sync Architecture
- **GPay & UPI Payment Share Integration**:
  - Added `ACTION_SEND` intent filters for both payment receipts (images) and payment confirmation texts. Kharcho now appears in the Android system share sheet directly from Google Pay, PhonePe, and Paytm.
- **Smart Receipt OCR Amount Extraction**:
  - Redesigned amount recognition to strictly isolate the payment amount (with `₹` symbol priority) and reject 10-18 digit UPI Reference Numbers, UTRs, and Order IDs.
- **Cloud Messaging Topic Subscribers & Push Notifications**:
  - Automatically subscribed users to group broadcast channels when creating, joining, or re-logging into groups.
  - Triggered push notifications to all group members on new member joins and new group expenses.
- **Split Group Member Count & Total Synchronization**:
  - Prevented empty cloud query responses from wiping out local members and totals, eliminating the "0 members • Total: ₹0.00" sync glitch.

---

## 🛠️ [v1.0.3] - October 2026

### Added
- **Gullak (Spare Change Savings)**:
  - Automatic round-up of every logged expense to the nearest ₹10.
  - Virtual savings piggy bank displayed on the Dashboard and Profile.
- **Financial Health Score (0-100)**:
  - Algorithmic score evaluating spending ratios, debt-to-income balance, and budget discipline.
- **Smart Biometric Lock & Auto-Relock**:
  - Fingerprint and Face Unlock security for private financial records.
  - Timed relock protection masking widget balances when locked.
- **Home Screen App Widgets**:
  - 2x2 Streak Widget, 2x2 Health Score Widget, 4x2 Financial Glance Widget, and 4x2 Category Pie Chart Widget.

---

## 📦 [v1.0.2] - September 2026

### Added
- **Natural Language Quick Type**:
  - Fast text logging (e.g. `chai 40 auto 120 groceries 850`) parsed instantly into itemized expense rows.
- **Split Expenses with Friends**:
  - Group splits, settled vs owed balance tracking, and shareable settlement links.
- **EMI & Debt Installment Tracker**:
  - Loan payoff schedules, monthly installment reminders, and interest tracking.

---

## 🏁 [v1.0.1] - September 2026

### Added
- Multi-section expense ledger (Household, Personal, Other).
- Payment method tagging (UPI, Bank Account, Credit Card, Cash).
- Local-first encryption for user credentials and financial records.
- PDF and CSV monthly statement generation.

---

## 🌟 [v1.0.0] - August 2026
- Initial release of Kharcho Expense Tracker with secure cloud sync.
