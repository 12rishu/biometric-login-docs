# User Story Document – Biometric Login

## Epic: Biometric Authentication for Mobile Banking

This epic covers the implementation of biometric authentication (Face ID and Fingerprint) in the mobile banking app to improve login speed, security, and user experience.

---

## User Story ID
US-01

---

## Title
Enable biometric login for mobile banking users

---

## User Story

**As a** mobile banking customer,  
**I want** to log in using Face ID or Fingerprint,  
**So that** I can securely and quickly access my account without typing my password every time.

---

## Acceptance Criteria

- ✅ Biometric prompt is shown after successful password login on supported devices
- ✅ User can opt in or opt out of biometric login during setup
- ✅ Biometric login can be enabled or disabled later from settings
- ✅ Biometric authentication uses device-native Face ID or Fingerprint APIs
- ✅ On biometric failure (3 attempts), app falls back to password login
- ✅ Biometric preference is stored securely on the device, not in the backend

---

## Additional Scenarios

### Scenario 1: First-time login after update  
**Given** the user logs in with a password,  
**When** biometric is supported and enabled on device,  
**Then** app prompts: “Would you like to enable biometric login?”

### Scenario 2: Biometric disabled by user  
**Given** biometric was previously enabled,  
**When** the user disables it from settings,  
**Then** future logins revert to password login.

---

## Business Value

- Reduces login time by ~25%  
- Increases app adoption and retention  
- Aligns with 2025 security standards and user expectations

---

## Related Use Case

- [UseCases/UseCase_Biometric_Login.md](../UseCases/UseCase_Biometric_Login.md)

---

## Notes

- Applies to mobile platforms only (Android 12+, iOS 15+)  
- No actual biometric data is stored in the app — only a preference flag  
- This feature does not cover biometric-based transaction approvals
