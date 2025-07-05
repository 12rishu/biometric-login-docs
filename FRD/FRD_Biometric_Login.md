# Functional Requirements Document (FRD)

## 1. Document Control

- **Version**: 1.0  
- **Created by**: Rishu Singh  
- **Reviewed by**: QA Lead, Dev Lead, Product Owner  
- **Date**: July 2025  

---

## 2. Purpose

To define how the biometric login feature will work within the mobile banking application, detailing system behaviors, data inputs, and functional flows.

---

## 3. Scope

### In Scope:
- Setup and use of biometric login on Android and iOS apps  
- Native API integration (Face ID / Fingerprint)  
- Enabling/disabling biometric in settings  
- Fallback to password login

### Out of Scope:
- Web-based biometric login  
- Biometric authentication for transactions

---

## 4. Assumptions

- Devices support biometric hardware and OS API  
- User has enabled biometric settings on device  

---

## 5. Functional Requirements

| FR ID   | Description                                                                 | Priority |
|---------|-----------------------------------------------------------------------------|----------|
| FR-01   | App shall prompt the user to enable biometric login after successful password login | High     |
| FR-02   | App shall authenticate using native biometric APIs (Face ID / Fingerprint)  | High     |
| FR-03   | Users shall be able to enable or disable biometric login from settings      | Medium   |
| FR-04   | On biometric failure, the app shall fallback to password login              | High     |
| FR-05   | No biometric data shall be stored on app or backend servers                 | Critical |

---

## 6. User Interface Requirements

- **Prompt**: “Would you like to enable Face ID/Fingerprint login?” after password login  
- **Settings Option**: Toggle in profile/settings → “Use biometric login”  
- **Fallback Screen**: Password field with “Forgot Password?” link shown on biometric failure

---

## 7. Data Requirements

- Secure storage of biometric preference (yes/no) in encrypted local device storage  
- No actual biometric data will be handled by the app

---

## 8. Error Handling

| Scenario                                | Expected Behavior                        |
|-----------------------------------------|-------------------------------------------|
| Biometric hardware not available        | Show message: “Biometric not supported”   |
| Biometric authentication fails 3 times  | Fallback to password login                |
| User cancels biometric prompt           | Stay on login screen with password option |

---

## 9. Dependencies

- Android/iOS biometric APIs  
- Secure keychain storage / Android Keystore  
- Mobile device hardware compatibility  
- App version ≥ 6.5

---

## 10. Non-Functional Requirements

- App must respond to biometric login in ≤ 3 seconds  
- Secure storage using platform encryption  
- Compliance with GDPR and local regulations

---

## 11. Glossary

- **Face ID / Fingerprint**: Device-level biometric security feature  
- **Fallback**: Alternate login method (password) if biometric fails  
- **Native API**: Operating system–provided biometric interface  
