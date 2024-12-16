## Mobile-Based Wallets

1. Identify and resolve intent and deeplink issues, secure webview configurations, and enforce platform guidelines.
2. Ensure encryption, file-level protection, and safeguard keys and sensitive data during storage and transmission.
3. Validate SSL/TLS configurations, enforce HTTPS, and implement certificate pinning to prevent cleartext communication or weak SSL.
4. Test session management, rate limiting, 2FA robustness, and enforce strong password policies to enhance authentication security.
5. Use secure cryptographic algorithms and protect sensitive operations against method hooking and tampering.
6. Prevent insecure direct object references (IDOR), secure hidden endpoints, and validate role-based access control (RBAC).
7. Address risks of buffer overflows, tampering, and reverse engineering using code obfuscation, anti-debugging measures, and repackaging checks.
8. Ensure production builds are free from unintended functionality, such as backdoors or debug code.
9. Protect sensitive data against screenshots, including preventing or warning about sensitive screenshots on Android/iOS and ensuring no background screenshot leaks.
10. Detect and block usage on jailbroken or rooted devices to prevent exploitation.
11. Disable custom keyboards during sensitive data entry to protect user input.
12. Use secure accessibility attributes for iOS keychain data to prevent unauthorized access.

## Desktop-Based Wallets (Electron-Based)

1. Verify the Electron and bundled Chromium versions are up-to-date to mitigate known vulnerabilities.
2. Check that the application does not load remote content unnecessarily.
3. Ensure nodeIntegration and enableRemoteModule are disabled in the Electron configuration.
4. Validate that contextIsolation, sandbox, and webSecurity are enabled.
5. Test for vulnerabilities in navigation logic, such as allowing navigation to arbitrary external web pages, and validate the security of will-navigate and new-window events.
6. Inspect preload scripts for exploitable code or unsafe use of Node.js APIs.
7. Verify that dangerous functions, such as openExternal, do not process unvalidated user input.
8. Ensure custom protocols used by the application are secured against abuse.
9. Test for remote code execution (RCE) vulnerabilities through XSS or misconfigured Electron settings.
10. Check for insecure file access, such as unauthorized reading of local files through webview or other methods.
11. Validate that IPC (Inter-Process Communication) messages are sanitized and securely handled.
12. Verify that sensitive data (e.g., mnemonic phrases or keys) is not stored in memory, files, or the clipboard without encryption or protection.
13. Assess regex and domain validation in navigation logic to prevent phishing and XSS attacks.
14. Use tools like Electronegativity or Node.js scanners to identify misconfigurations and security issues in the Electron app.
15. Validate the deployment process to ensure no debug or unnecessary code is included in the production build and third-party libraries are free of known vulnerabilities.


## Extension-Based Wallets

1. Verify that the extension's permissions and host permissions are limited to the minimum necessary.
2. Check if the extension correctly validates the origin of messages before processing.
3. Assess whether malicious websites can exploit XSS, clickjacking, or other injection vulnerabilities within the extension.
4. Verify that sensitive information is not stored unprotected in memory, files, or the codebase.
5. Analyze the manifest.json file for appropriate configurations, permissions, and web-accessible resources.
6. Test for secure communication between content scripts, background scripts, and native messaging, ensuring proper input validation and sanitization.
7. Ensure no insecure PostMessage or DOM-based communication vulnerabilities exist.
8. Test for secure storage and retrieval of sensitive data, such as mnemonic phrases or private keys.
9. Confirm the extension cannot be exploited to compromise the browser or host system.
10. Validate that the extension resists tampering, such as code modifications or unauthorized installations.
11. Test APIs for proper input validation, rate limiting, and secure data handling.
12. Assess the extension for vulnerabilities in its core components, such as content scripts, background scripts, and native binaries.




## Web-Based Wallets

1. Validate the application architecture and ensure security is incorporated into functional requirements, prototypes, and design.
2. Perform network security checks, including scanning for open ports, running services, and sniffing for data exposure or weaknesses.
3. Test for cloud misconfigurations in critical services such as IAM, S3, EC2, RDS, and Lambda.
4. Test for injection vulnerabilities, including code, SQL, XSS, LDAP, OS command, and HTML injections.
5. Validate session management, rate limiting, strong password hashing, and 2FA implementations for secure authentication.
6. Identify and mitigate sensitive data exposure risks, such as hardcoded API keys, unprotected secrets, and misconfigured S3 buckets.
7. Test for XML external entities (XXE) vulnerabilities that could lead to SSRF, file retrieval, or image upload exploitation.
8. Assess access control to prevent privilege escalation, IDOR, and multi-step process vulnerabilities.
9. Detect security misconfigurations, including verbose errors, default credentials, unnecessary services, and unpatched flaws.
10. Test for insecure deserialization vulnerabilities and improper handling of serialized data.
11. Identify and mitigate risks from components with known vulnerabilities in the application stack.
12. Ensure proper logging, secure data storage, and incident response mechanisms are in place.
13. Test APIs for broken object-level and function-level authorization, excessive data exposure, and improper asset management.
14. Check for vulnerabilities like XSS, clickjacking, open redirects, and HTML injection.
15. Verify security headers, CORS configurations, CSRF protections, and cookie attributes where applicable.
16. Validate the application against all OWASP Top 10 vulnerabilities and ensure comprehensive coverage.
17. Mitigate risks of phishing attacks and malicious JavaScript injection specific to web wallets.

