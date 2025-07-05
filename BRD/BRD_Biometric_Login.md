# Business Requirements Document (BRD)

## 1. Document Control

- **Version**: 1.0  
- **Created by**: Rishu Singh  
- **Reviewed by**: Product Owner, QA Lead, Dev Lead  
- **Approved by**: Product Steering Committee  
- **Date**: July 2025  

---

## 2. Executive Summary

This document outlines the need to introduce biometric authentication (Face ID/Fingerprint) into our mobile banking app.  
The primary objective is to enhance customer convenience and security by allowing faster login access and reducing dependency on passwords.

---

## 3. Purpose

To define the high-level business requirements for implementing biometric login for mobile banking customers.

---

## 4. Business Objectives

- Increase login speed by 25%  
- Reduce password reset requests by 40%  
- Improve customer satisfaction (CSAT) by 15%  
- Achieve biometric login adoption by 70% of active users within 3 months

---

## 5. Project Scope

### In Scope:
- Biometric login for mobile apps (Android and iOS)  
- Device-native Face ID/Fingerprint integration  
- Enable/disable option for biometric login in app settings  
- Support for fallback to password login  

### Out of Scope:
- Biometric login for web portal  
- Biometric-based transaction approvals  
- Support for older, non-biometric devices  

---

## 6. Stakeholders

| Role               | Name           | Responsibility                              |
|--------------------|----------------|----------------------------------------------|
| Business Analyst   | Rishu Singh    | Documenting requirements and process flows   |
| Product Owner      | Aarti Mehta    | Feature prioritization and approval          |
| QA Lead            | Sneha Sharma   | Test planning and execution oversight        |
| Development Lead   | Ravi Kumar     | System architecture and implementation       |
| Compliance Officer | Sanjay Iyer    | Ensuring regulatory and legal compliance     |

---

## 7. Business Requirements

| BR ID  | Description                                                                 |
|--------|------------------------------------------------------------------------------|
| BR-01  | System must prompt users to enable biometric login on first login after update |
| BR-02  | Users must be able to enable/disable biometric login from app settings       |
| BR-03  | App must use device-native biometric API for authentication                  |
| BR-04  | App must fallback to password login if biometric fails                       |
| BR-05  | Biometric credentials must not be stored in the backend                      |

---

## 8. Current vs Future State

### Current State:
- Login only through password/PIN  
- Higher password reset requests  

### Future State:
- Login using Face ID/Fingerprint  
- Faster, secure access to app  

---

## 9. Assumptions

- Devices are running Android 12+ or iOS 15+  
- User has biometric enabled on their phone  

---

## 10. Constraints

- Regulatory compliance with GDPR, RBI guidelines  
- Device compatibility limitations  

---

## 11. Risks

- Biometric failure rate on older devices  
- Security concerns regarding spoofing  

---

## 12. Dependencies

- Mobile OS APIs  
- DevOps for app update rollout  
- App Store/Play Store approvals  

---

## 13. Glossary

- **Biometric**: Fingerprint/Face ID authentication  
- **Native API**: Platform-provided libraries (e.g., Apple FaceID framework)  
