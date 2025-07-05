# Use Case Document – Biometric Login

## 1. Use Case ID
UC-01

---

## 2. Use Case Name
Enable Biometric Login

---

## 3. Actor(s)
- Retail Banking Customer

---

## 4. Description
This use case describes how a mobile banking user can enable biometric authentication (Face ID or Fingerprint) after logging in with a password.

---

## 5. Preconditions
- The user has installed the latest version of the mobile banking app
- The user has logged in using a valid password
- The device supports biometric authentication (Face ID / Fingerprint)
- Biometric is enabled in the device settings

---

## 6. Main Flow (Basic Scenario)
| Step | Description                                                                 |
|------|-----------------------------------------------------------------------------|
| 1    | User logs in using a valid password                                         |
| 2    | System detects biometric support on the device                              |
| 3    | App prompts: “Would you like to enable biometric login?”                    |
| 4    | User selects “Yes”                                                          |
| 5    | Device shows native biometric authentication prompt                         |
| 6    | User successfully authenticates using Face ID or Fingerprint                |
| 7    | App stores biometric login preference locally (secure storage)              |
| 8    | User is redirected to the home/dashboard screen                             |

---

## 7. Alternate Flows
### A1: User Selects “No”
- App stores biometric preference as disabled
- App continues to use password login

### A2: Biometric Authentication Fails
- User is allowed 3 attempts
- After 3 failures, fallback to password login is triggered

---

## 8. Postconditions
- Biometric login is successfully enabled for future sessions
- User can disable it anytime from app settings

---

## 9. Exceptions
- Device does not support biometric → no prompt shown
- System error during biometric setup → user shown an error message and fallback to password login

---

## 10. Notes
- This feature is for mobile apps only (iOS and Android)
- No biometric data is stored on the device or server — only the preference flag is saved

---

## 11. Related Documents
- [BRD/BRD_Biometric_Login.md](../BRD/BRD_Biometric_Login.md)
- [FRD/FRD_Biometric_Login.md](../FRD/FRD_Biometric_Login.md)
