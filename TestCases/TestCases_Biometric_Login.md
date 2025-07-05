# Test Cases – Biometric Login Feature

| TC ID  | Title                                       | Precondition                        | Steps                                                                 | Expected Result                         | Priority |
|--------|---------------------------------------------|-------------------------------------|-----------------------------------------------------------------------|------------------------------------------|----------|
| TC-01  | Enable biometric prompt                     | App installed, password login done  | Login → Accept prompt → Authenticate                                | Biometric flag enabled                  | High     |
| TC-02  | Successful biometric login                  | Biometric enabled                   | Launch app → Scan fingerprint/face                                   | User logged in                          | High     |
| TC-03  | Cancel biometric dialog                     | Biometric enabled                   | Launch app → Tap cancel on biometric prompt                          | Password login shown                    | Medium   |
| TC-04  | Biometric fails 3 times                     | Biometric enabled                   | Attempt 3 failed scans                                               | Fallback to password                    | High     |
| TC-05  | Disable biometric from settings             | Logged in user                      | Go to Settings → Turn off biometric                                  | Biometric login disabled                | Medium   |
| TC-06  | No prompt on unsupported device             | Device has no biometric hardware    | Login to app                                                         | No biometric prompt shown               | Low      |
| TC-07  | User selects \"No\" on biometric setup      | Prompt is displayed                 | Tap “No” on biometric prompt                                         | Biometric remains disabled              | Medium   |
| TC-08  | First login post-update triggers biometric  | Updated app version                 | Login with password post update                                      | Prompt displayed                        | High     |
| TC-09  | Biometric not permitted by OS               | Permissions off in device settings | Launch app                                                           | App shows fallback login                | Medium   |
| TC-10  | Error from biometric API                    | Biometric API unavailable           | Attempt to scan when API is down                                     | Error message displayed, fallback login | High     |
