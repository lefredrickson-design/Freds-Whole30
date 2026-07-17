# Data Security & Encryption Guide

Complete guide to how your data is protected in the Whole30 Weekly Meal Planner.

---

## Table of Contents

1. [Overview](#overview)
2. [Encryption Standards](#encryption-standards)
3. [Local Storage Security](#local-storage-security)
4. [Server Security](#server-security)
5. [Password Protection](#password-protection)
6. [Data Transmission](#data-transmission)
7. [Access Controls](#access-controls)
8. [Backup Security](#backup-security)
9. [Instacart Integration Security](#instacart-integration-security)
10. [Security Incidents](#security-incidents)
11. [User Responsibilities](#user-responsibilities)
12. [Compliance](#compliance)

---

# Overview

## What We Protect

**Your personal data is protected by multiple layers of security:**

### Level 1: Encryption
- All data encrypted at rest (stored)
- All data encrypted in transit (sent)
- Military-grade encryption standards

### Level 2: Access Control
- Only authorized personnel have access
- Multi-factor authentication required
- Role-based access control (RBAC)
- Audit logging of all access

### Level 3: Infrastructure
- Secure servers with firewalls
- DDoS protection
- Intrusion detection systems
- Regular security patches

### Level 4: Monitoring
- 24/7 security monitoring
- Automated threat detection
- Regular penetration testing
- Vulnerability scanning

---

# Encryption Standards

## Data At Rest (Stored Data)

### AES-256 Encryption
**What it is:** Advanced Encryption Standard with 256-bit keys  
**Strength:** Military-grade, used by NSA  
**Used for:** All sensitive stored data

**Data encrypted:**
- ✅ Passwords
- ✅ Instacart account email (if provided)
- ✅ Delivery address
- ✅ Health tracking information
- ✅ Sensitive preferences

**Not encrypted (doesn't need it):**
- ❌ Email address (needed for login)
- ❌ Username (needed for login)
- ❌ Meal plan names (not sensitive)
- ❌ Recipe names (not sensitive)

### Encryption Keys
- ✅ Keys stored separately from data
- ✅ Keys rotated regularly (annually)
- ✅ Key derivation functions used (PBKDF2)
- ✅ Salted hashes (16+ character salts)
- ❌ No hardcoded keys in code

---

## Data In Transit (Sent Data)

### TLS 1.3 Encryption
**What it is:** Transport Layer Security, latest version  
**Where used:** All data sent between app and servers  
**Strength:** Can't be intercepted without cryptographic key

**Protected channels:**
- ✅ Login/authentication
- ✅ User data upload
- ✅ Meal plan syncing
- ✅ Instacart integration
- ✅ All API calls

### Certificate Pinning
- ✅ App verifies server certificate
- ✅ Prevents man-in-the-middle attacks
- ✅ Updated with each app release

### Forward Secrecy
- ✅ Each session has unique encryption key
- ✅ Past conversations can't be decrypted
- ✅ Future conversations safe if current key compromised

---

# Local Storage Security

## What's Stored on Your Device

### Local Encrypted Storage

**Data stored locally on your device:**
- Meal plans
- Shopping lists
- Preferences
- Health tracking notes
- Instacart delivery address (optional)

**Security measures:**
- ✅ Encrypted locally on your device
- ✅ Requires device password to access
- ✅ Deleted when you uninstall app
- ✅ Not accessible to other apps

### Platform-Specific Security

**iOS/macOS:**
- Uses Apple Keychain for credentials
- Encrypted by iOS/macOS encryption
- Biometric authentication available
- Isolated from other apps

**Android:**
- Uses Android Keystore for credentials
- Hardware-backed encryption (if available)
- Biometric authentication available
- Isolated from other apps

**Web:**
- Uses browser's secure storage
- LocalStorage encrypted
- SessionStorage for temporary data
- CORS protection enabled

### Device-Level Security

**Your device provides:**
- Operating system encryption (full disk)
- File system permissions
- App sandboxing
- Secure boot

**You should:**
- ✅ Keep your device updated
- ✅ Use device passcode/biometrics
- ✅ Enable automatic lock
- ✅ Don't jailbreak/root device
- ✅ Use reputable antivirus software

---

# Server Security

## Infrastructure Protection

### Network Security
- **Firewalls:** Block unauthorized access
- **WAF:** Web Application Firewall
- **DDoS Protection:** Prevents attacks
- **IDS/IPS:** Intrusion detection/prevention
- **VPC:** Isolated network environment

### Server Hardening
- **OS Patches:** Latest security updates
- **Service Minimization:** Only necessary services
- **Port Filtering:** Only needed ports open
- **SSH Keys:** No password SSH access
- **SELinux/AppArmor:** Mandatory access control

### Database Security
- **Encryption:** AES-256 at rest
- **Backups:** Encrypted backups
- **Access Control:** Least privilege access
- **Audit Logging:** All database access logged
- **SQL Injection Prevention:** Parameterized queries

---

# Password Protection

## How Passwords Are Stored

### NOT Stored in Plain Text
❌ We never store passwords you can read  
❌ We never store passwords in our database  
❌ We never store passwords in logs  

### Stored as Bcrypt Hashes
✅ One-way hashing function  
✅ Can't be reversed to get original password  
✅ Each password salted (random + password hashed)  
✅ Work factor prevents brute-force attacks  

### Hashing Process
```
Your Password → Add Salt → Hash with Bcrypt → Store Hash
```

**Example:**
```
Original: "MySecurePassword123!"
Salt: (random 16+ characters)
Stored: $2b$12$a7b9d2e4... (64 characters, can't be reversed)
```

### Password Requirements
- Minimum 12 characters
- Must include uppercase letter
- Must include lowercase letter
- Must include number
- Must include special character

**Examples of strong passwords:**
- ✅ MyWhole30Plan!2024
- ✅ Eat$Real$Food#30
- ✅ Gr@ssF3d-Beef!Success
- ✅ CompliantEating@2024

**Not allowed:**
- ❌ password123 (too simple)
- ❌ whole30 (only letters)
- ❌ 12345678 (only numbers)
- ❌ Your name or email

---

## Password Reset Security

### Secure Reset Process

1. **User requests reset**
   - You click "Forgot Password"
   - Enter your email address
   
2. **Token generated**
   - Unique reset token created
   - Token valid for 1 hour only
   - Token can only be used once
   - Different token each time

3. **Email sent securely**
   - Reset link sent to your email
   - Only you can access your email
   - Link can't be guessed
   
4. **New password set**
   - Follow link from email
   - Create new password
   - Old password invalidated
   - Old sessions logged out

### Security Features
- ✅ Token is cryptographically random
- ✅ Token expires after 1 hour
- ✅ Token can only be used once
- ✅ Reset requires access to email
- ✅ Old password immediately invalid
- ✅ All sessions terminated
- ✅ Reset logged and auditable

---

## Two-Factor Authentication (2FA)

### Optional but Recommended

**Available methods:**
- ✅ Authenticator app (Google Authenticator, Authy)
- ✅ SMS text message
- ✅ Email code (backup)

### How it works

1. **Sign in with password**
   - Enter username/email
   - Enter password
   
2. **Enter second factor**
   - Authenticator app code (changes every 30 sec)
   - SMS code (sent to your phone)
   - Email code (sent to your email)
   
3. **Access granted**
   - Only with both password AND second factor

### Why it matters
- ✅ Even if password is guessed, attacker needs 2FA code
- ✅ SMS/email codes are sent only to you
- ✅ Authenticator codes can't be intercepted
- ✅ Makes account extremely difficult to hack

---

# Data Transmission

## HTTPS/TLS Security

### What Happens When You Send Data

```
Your Device → HTTPS Encrypted → Our Servers
↓
Encryption happens automatically
↓
Data can't be intercepted even if WiFi is hacked
```

### Protection During Transmission

✅ **Encryption in Transit**
- All data encrypted end-to-end
- Uses TLS 1.3 protocol
- 256-bit encryption keys

✅ **Certificate Validation**
- Your app verifies we are who we claim to be
- Prevents man-in-the-middle attacks
- Certificates renewed regularly

✅ **Session Management**
- Each session gets unique token
- Sessions expire after inactivity
- Sessions can't be hijacked

### Public WiFi Warning

**On public WiFi:**
- ✅ Your data is still encrypted
- ✅ HTTPS protects data in transit
- ✅ Hacker can't see your password
- ✅ Hacker can't see your health data

**But remember:**
- ⚠️ WiFi provider can see you're using the app
- ⚠️ Device may expose other unencrypted data
- ✅ Your app data remains private

---

# Access Controls

## Who Has Access to Your Data

### Principle of Least Privilege

**Only authorized personnel can access:**
- Developers (code only, not user data)
- Database administrators (backup/maintenance only)
- Security team (audit logs only)
- Support staff (only with your permission)

**No one has:**
- ❌ Full access to all user data
- ❌ Plaintext password access
- ❌ Unlogged access
- ❌ Permanent access (revoked when they leave)

### Role-Based Access Control (RBAC)

| Role | Access | Reason |
|------|--------|--------|
| Developer | Code & architecture | Build/maintain app |
| DBA | Database structure | Backups, maintenance |
| Security | Audit logs | Monitor access |
| Support | Limited user data | Help with issues (with consent) |
| Management | Metrics only | Business decisions |
| Marketing | Anonymized stats | Growth tracking |

### Audit Logging

**Everything is logged:**
- ✅ Who accessed data
- ✅ When they accessed it
- ✅ What data they accessed
- ✅ What they did with it

**Logs are:**
- ✅ Encrypted
- ✅ Immutable (can't be changed)
- ✅ Retained for 1 year
- ✅ Reviewed regularly

---

# Backup Security

## How We Backup Your Data

### Automated Backups
- ✅ Daily encrypted backups
- ✅ Separate from production systems
- ✅ Stored in secure facility
- ✅ Tested monthly for recovery

### Backup Encryption
- ✅ Backups encrypted with AES-256
- ✅ Different encryption key than production
- ✅ Keys stored separately
- ✅ Key rotation annually

### Backup Retention
- ✅ 30-day retention (rolling daily)
- ✅ Can recover data from past 30 days
- ✅ After 30 days, permanently deleted
- ✅ Deleted data unrecoverable

### Backup Access
- ❌ No one can browse backups casually
- ✅ Only recovered in emergency
- ✅ Recovery requires multi-person approval
- ✅ Recovery is fully logged and audited

---

# Instacart Integration Security

## How We Protect Instacart Data

### What We Store
**From Instacart connection:**
- ✅ Your Instacart account email (encrypted)
- ✅ Your delivery address (encrypted, optional)
- ✅ Your preferred store

**What we DON'T store:**
- ❌ Your Instacart password (never)
- ❌ Your payment information (never)
- ❌ Your order history (never)
- ❌ Your payment method details (never)

### Authentication Method
- ✅ OAuth 2.0 (industry standard)
- ✅ No password ever shared with us
- ✅ Token-based authentication
- ✅ Tokens refresh automatically
- ✅ Tokens can be revoked anytime

### Token Security
- ✅ Tokens are cryptographically random
- ✅ Tokens are encrypted in storage
- ✅ Tokens have expiration times
- ✅ Tokens are scoped to specific permissions
- ✅ Tokens can be revoked

### Unlinking Instacart
When you unlink:
- ✅ Token immediately revoked
- ✅ Stored data deleted within 24 hours
- ✅ Access removed from Instacart
- ✅ Can relink anytime

### Instacart's Security
When you use Instacart:
- ✅ Instacart's terms apply to their data
- ✅ Your payment info goes to Instacart
- ✅ Their security is separate
- ✅ Read their privacy policy: instacart.com/privacy

---

# Security Incidents

## In Case of a Data Breach

### Our Response

**Within 24 hours:**
- [ ] Breach contained
- [ ] Systems secured
- [ ] Investigation launched
- [ ] Evidence preserved

**Within 72 hours:**
- [ ] You are notified
- [ ] Full details provided
- [ ] Guidance given
- [ ] Support offered

**Within 30 days:**
- [ ] Investigation completed
- [ ] Report published
- [ ] Improvements implemented
- [ ] Lessons learned

### What We'll Tell You

In breach notification, we'll explain:
- ✅ What happened
- ✅ When it happened
- ✅ What data was affected
- ✅ What you should do
- ✅ Who to contact
- ✅ Support resources available

### What We'll Do

**Immediate:**
- Patch vulnerabilities
- Secure all systems
- Revoke compromised credentials
- Isolate affected systems

**Short-term:**
- Enhanced monitoring
- Increased logging
- Temporary access restrictions
- Additional backups

**Long-term:**
- Security audit by third-party
- Improved controls
- Staff training
- Infrastructure upgrades

### Your Free Support

If breach affects you:
- ✅ Credit monitoring (12 months, free)
- ✅ Identity theft protection (24 months, free)
- ✅ Priority support (free, unlimited)
- ✅ Password reset help (free)

---

# User Responsibilities

## What You Should Do

### Password Security
- ✅ Create strong, unique password
- ✅ Don't share password with anyone
- ✅ Change password if you suspect compromise
- ✅ Use password manager to store securely
- ✅ Don't use same password as other sites

### Device Security
- ✅ Keep device updated
- ✅ Use device passcode/biometrics
- ✅ Set automatic lock (5-10 minutes)
- ✅ Use antivirus software
- ✅ Don't jailbreak/root device

### Account Management
- ✅ Check login activity regularly
- ✅ Log out on shared devices
- ✅ Review connected apps/services
- ✅ Update account info if it changes
- ✅ Enable 2FA (highly recommended)

### Network Security
- ✅ Don't use unsecured public WiFi
- ✅ Use VPN on public networks (optional)
- ✅ Be cautious of phishing emails
- ✅ Verify website URL before entering password
- ✅ Don't share account over insecure channels

### Data Protection
- ✅ Don't share sensitive data via email
- ✅ Be careful what you log (health data)
- ✅ Don't take screenshots of sensitive data
- ✅ Review permissions you've granted
- ✅ Delete account if you no longer use it

---

# Compliance

## Security Standards We Meet

### OWASP Top 10
- ✅ Injection prevention
- ✅ Authentication & session management
- ✅ Sensitive data protection
- ✅ XML external entities (XXE) prevention
- ✅ Broken access control prevention
- ✅ Security misconfiguration prevention
- ✅ Cross-site scripting (XSS) prevention
- ✅ Insecure deserialization prevention
- ✅ Using components with known vulnerabilities prevention
- ✅ Insufficient logging & monitoring prevention

### NIST Cybersecurity Framework
- ✅ Identify
- ✅ Protect
- ✅ Detect
- ✅ Respond
- ✅ Recover

### ISO 27001
- ✅ Information security management system
- ✅ Access control
- ✅ Cryptography
- ✅ Incident management
- ✅ Compliance

### GDPR Compliance
- ✅ Data minimization
- ✅ Purpose limitation
- ✅ Storage limitation
- ✅ Data subject rights
- ✅ Data processing agreements

### HIPAA-Aligned (Not fully HIPAA, but aligned)
- ✅ Encryption standards
- ✅ Access controls
- ✅ Audit logging
- ✅ Incident response
- ✅ Data integrity

---

## Regular Security Testing

### Penetration Testing
- ✅ Quarterly external penetration tests
- ✅ Red team exercises (annually)
- ✅ Staff security awareness training (semi-annually)

### Vulnerability Scanning
- ✅ Daily automated scanning
- ✅ Weekly vulnerability assessments
- ✅ Monthly code reviews
- ✅ Annual full security audit

### Compliance Audits
- ✅ Quarterly internal audits
- ✅ Annual third-party audit
- ✅ Continuous compliance monitoring

---

# Contact Security Team

**Security Issues:**
Email: security@whole30planner.com

**Vulnerability Disclosure:**
Please report security issues privately, not on social media or public forums.

**We promise:**
- ✅ Acknowledge receipt within 24 hours
- ✅ Investigate immediately
- ✅ Fix within 30 days
- ✅ Thank you publicly (if you want)
- ✅ Bug bounty (if applicable)

---

# Summary

**Your data is protected by:**

✅ **Encryption:** Military-grade AES-256  
✅ **Transmission:** TLS 1.3 end-to-end  
✅ **Storage:** Encrypted at rest  
✅ **Access:** Strictly limited & logged  
✅ **Passwords:** Bcrypt hashed, salted  
✅ **Monitoring:** 24/7 security team  
✅ **Compliance:** OWASP, NIST, ISO, GDPR  
✅ **Backups:** Encrypted & tested  
✅ **Incident Response:** 72-hour notification  
✅ **Support:** Free protection if breached  

**Your privacy and security are our top priority.**

---

*Last Updated: July 17, 2026*  
*Questions? security@whole30planner.com*
