# Test Plan – Biometric Login Feature

## 1. Objective

To validate the biometric login feature on Android and iOS mobile apps for functionality, performance, error handling, and device compatibility.

---

## 2. Scope

### In Scope:
- Enable biometric login after password login
- Login using Face ID or Fingerprint
- Disable biometric from settings
- Fallback to password login

### Out of Scope:
- Biometric for transaction approval
- Biometric login on web portal

---

## 3. Test Strategy / Approach

- **Testing Types**: Functional, UI, Compatibility, Negative, Regression  
- **Technique**: Manual testing  
- **Tools**: JIRA (tracking), BrowserStack (device testing), Firebase (logs)

---

## 4. Resources

- **QA Engineer**: Sneha Sharma  
- **BA (Review)**: Rishu Singh  
- **Developer**: Ravi Kumar  
- **Test Environment**: QA builds on Android/iOS staging servers

---

## 5. Schedule

| Activity               | Start Date | End Date   |
|------------------------|------------|------------|
| Test Planning          | July 6     | July 8     |
| Test Case Design       | July 9     | July 11    |
| Test Execution         | July 12    | July 16    |
| Bug Fixing & Retesting | July 17    | July 19    |
| Final QA Sign-off      | July 20    | July 21    |

---

## 6. Test Deliverables

- Test Plan  
- Test Cases (in .md and .xlsx)  
- Test Summary Report  
- Defect Log  
- QA Sign-off Report

---

## 7. Risk Management

| Risk                                | Mitigation Strategy                           |
|-------------------------------------|-----------------------------------------------|
| Device-specific biometric failure   | Test across various models/OS versions        |
| Biometric not supported on emulator| Use BrowserStack or physical devices          |
| User rejects biometric permissions  | Provide fallback and track logs               |

---

## 8. Entry Criteria

- Requirements are signed off  
- Test environment is ready  
- Test cases are reviewed and approved  
- Biometric-capable devices available

---

## 9. Exit Criteria

- 95–100% test cases executed  
- No P1/P2 bugs open  
- QA sign-off completed

---

## 10. Test Environment

- **Devices**: iPhone 13/14, Samsung S22, Pixel 6  
- **OS**: iOS 15–17, Android 12–14  
- **App Version**: 6.5+ (staging)  
