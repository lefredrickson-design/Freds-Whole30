# Package Name Configuration for Google Play Console

**Package Name for Android App Distribution**

---

## Primary Package Name

### Recommended Package Name
```
com.fredswhole30.mealplanner
```

**Components:**
- **Domain Reverse:** `com` (reverse of commercial domain)
- **Company/Developer:** `fredswhole30` (Fred's Whole30)
- **App Purpose:** `mealplanner` (Meal Planner)

**Full Name:** Fred's Whole30 Weekly Meal Planner

---

## Alternative Package Names (if primary unavailable)

If `com.fredswhole30.mealplanner` is taken, alternatives in order of preference:

1. `com.whole30mealplanner.app`
2. `com.fredwhole30planner.meals`
3. `com.whole30.fredmealplanner`
4. `com.fredmealplan.whole30`
5. `app.whole30.fredplanner`

---

## Package Name Rules for Google Play

✅ **Requirements Met:**
- ✅ Unique identifier for your app
- ✅ Reverse domain notation format
- ✅ Lowercase letters only
- ✅ No spaces or special characters (except periods)
- ✅ 3+ segments (com.company.app)
- ✅ Memorable and descriptive
- ✅ Related to app functionality

❌ **What NOT to do:**
- ❌ Use spaces or underscores
- ❌ Use uppercase letters
- ❌ Use numbers at beginning of segment
- ❌ Generic names (com.app, com.myapp)
- ❌ Reserved words (com.google, com.android)

---

## Google Play Console Setup

### Steps to Register Package Name

1. **Sign in to Google Play Console**
   - Go to: https://play.google.com/console
   - Sign in with your Google account

2. **Create New App**
   - Click "Create app"
   - Enter app name: "Fred's Whole30 Meal Planner"

3. **Enter Package Name**
   - Package name: `com.fredswhole30.mealplanner`
   - This cannot be changed after creation
   - Click "Create"

4. **Complete App Setup**
   - App access: Public
   - App category: Health & Fitness
   - Content rating: Complete questionnaire

5. **Upload App**
   - Create signed APK/AAB
   - Upload to internal test track first
   - Test thoroughly before production

---

## App Store Listing Details

### App Information for Play Console

**App Name:** Fred's Whole30 Weekly Meal Planner

**Short Description (50 characters max):**
```
Plan Whole30 meals with privacy protection
```

**Full Description (4000 characters max):**
```
Fred's Whole30 Weekly Meal Planner

Plan your entire Whole30 journey with confidence. This comprehensive meal planning app helps you:

✅ Plan Whole30-compliant weekly meals
✅ Generate organized shopping lists
✅ Shop via integrated Instacart (optional)
✅ Track 52 weeks of progress
✅ Access seasonal recipes by location
✅ Customize for dietary preferences

🔐 PRIVACY FIRST
Your data is protected with military-grade encryption (AES-256). We never sell your data, ever. Your privacy is guaranteed:

✅ Military-grade encryption
✅ GDPR & CCPA compliant
✅ Your data is never sold
✅ Access/download/delete anytime
✅ Full transparency

📋 COMPLETE MEAL PLANNING
✅ 50+ pre-built Whole30 recipes
✅ 25+ seasonal recipes by location
✅ Weekly meal planner templates
✅ Shopping list generator
✅ Meal prep strategies

🛒 INSTACART INTEGRATION
✅ One-click add to cart
✅ Direct Instacart checkout
✅ Track prices across stores
✅ Optional integration

📊 YEAR-ROUND TRACKING
✅ 30-day progress tracker
✅ 52-week full-year tracking
✅ Energy & mood tracking
✅ Monthly reflections
✅ Quarterly reviews
✅ Annual summary

🌍 SEASONAL AWARENESS
✅ Location-based produce guides
✅ In-season recipes
✅ Storage tips
✅ Money-saving strategies

All features include complete documentation and user guides. Your Whole30 success starts here!

Privacy Policy: See in-app
Terms of Service: See in-app
```

**Category:** Health & Fitness

**Content Rating:** Everyone (Mature audiences due to health/medical information)

---

## App Metadata

### App Icon Requirements
- **Size:** 512 x 512 pixels
- **Format:** PNG (RGB, no transparency)
- **Safe zone:** Avoid critical content in outer 12.5%

### Screenshots (Required)
- **Minimum:** 2 screenshots
- **Recommended:** 5-8 screenshots
- **Size:** 1080 x 1920 pixels (portrait)
- **Format:** PNG or JPEG

**Suggested Screenshots:**
1. Meal planning interface
2. Shopping list with Instacart integration
3. Progress tracking dashboard
4. Seasonal produce guide
5. Privacy & security features
6. Settings & customization

### Feature Graphic
- **Size:** 1024 x 500 pixels
- **Format:** PNG or JPEG
- **Format:** Landscape
- **Content:** Show app's main feature (meal planning + privacy)

---

## Privacy & Compliance Info for Play Store

### Privacy Policy URL
```
https://github.com/lefredrickson-design/Freds-Whole30/blob/main/PRIVACY-POLICY.md
```

### Data Safety Section (Required)

**Data Collected:**
- ✅ User ID (email)
- ✅ Name
- ✅ Health & fitness (meal plans, tracking)
- ✅ Sensitive info (health data)
- ✅ Location (optional, for seasonal produce)
- ✅ Device ID (for analytics)

**Data Security:**
- ✅ Data encrypted in transit
- ✅ Data encrypted at rest
- ✅ Secure HTTPS connection
- ✅ Compliant with GDPR/CCPA

**Data Sharing:**
- ✅ NOT shared with third parties
- ✅ NOT sold
- ✅ Optional Instacart integration (separate)

**Data Retention:**
- ✅ Retained until account deletion
- ✅ Deleted within 30 days of account deletion
- ✅ User can request immediate deletion

**Data Practices:**
- ✅ Privacy-first design
- ✅ Minimal data collection
- ✅ User control over data
- ✅ Transparent practices

---

## App Signing Certificate

### Create Signing Key

**Before uploading to Play Console:**

1. **Generate keystore file**
```bash
keytool -genkey -v -keystore release-key.keystore \
  -keyalg RSA -keysize 2048 -validity 10000 \
  -alias release-key
```

2. **Store keystore safely**
   - Location: Secure backup
   - Password: Strong, unique
   - Keep private: Never share

3. **Sign APK/AAB**
```bash
jarsigner -verbose -sigalg SHA1withRSA \
  -digestalg SHA1 -keystore release-key.keystore \
  app-release-unsigned.apk release-key
```

**Important:** Keep your signing key safe. Google Play will use this to verify all future updates.

---

## Release Notes Template

### Version 1.0 Release Notes
```
🎉 Welcome to Fred's Whole30 Weekly Meal Planner!

✨ NEW FEATURES:
✅ 50+ Whole30-compliant recipes
✅ Weekly meal planning templates
✅ Organized shopping lists
✅ Instacart integration (optional)
✅ 52-week progress tracking
✅ Seasonal produce guides
✅ Customizable dietary preferences

🔐 SECURITY:
✅ Military-grade AES-256 encryption
✅ GDPR & CCPA compliant
✅ Your data is never sold
✅ Complete privacy control

📊 TRACKING:
✅ 30-day progress tracker
✅ 52-week full-year tracking
✅ Energy & mood monitoring
✅ Monthly reflections
✅ Quarterly reviews

🌍 SEASONAL:
✅ Location-based recipes
✅ Seasonal produce by region
✅ Storage tips
✅ Money-saving strategies

See Privacy Policy in-app for complete information.
```

---

## Compliance Checklist for Google Play

- [ ] Package name finalized: `com.fredswhole30.mealplanner`
- [ ] App name set: "Fred's Whole30 Weekly Meal Planner"
- [ ] Short description written
- [ ] Full description written
- [ ] Category selected: Health & Fitness
- [ ] Privacy policy URL provided
- [ ] Data Safety section completed
- [ ] Age rating completed
- [ ] App icon created (512x512)
- [ ] Screenshots created (5-8)
- [ ] Feature graphic created (1024x500)
- [ ] Signing key generated and secured
- [ ] APK/AAB signed and tested
- [ ] Release notes prepared
- [ ] Contact email configured
- [ ] Support URL provided (if available)

---

## Post-Launch Considerations

### Version Updates
- Update version number for each release
- Follow semantic versioning (1.0.0, 1.1.0, 2.0.0)
- Release on beta track first, then production

### User Support
- Monitor reviews and ratings
- Respond to user feedback
- Fix bugs promptly
- Add requested features

### Marketing
- Share app launch on social media
- Include privacy features in promotion
- Highlight encryption & data protection
- Emphasize user control over data

### Maintenance
- Keep dependencies updated
- Monitor security vulnerabilities
- Test with new Android versions
- Update privacy policy as needed
- Maintain compliance certifications

---

## Final Verification

**Before submitting to Google Play:**

✅ App functionality tested thoroughly  
✅ All features working on target devices  
✅ Privacy Policy linked and accessible  
✅ Terms of Service available in-app  
✅ Data Security documentation complete  
✅ No sensitive data hardcoded  
✅ Encryption enabled for all data  
✅ HTTPS used for all network calls  
✅ No third-party tracking enabled  
✅ Permissions minimized and justified  

---

## Quick Reference

| Item | Value |
|------|-------|
| **Package Name** | `com.fredswhole30.mealplanner` |
| **App Name** | Fred's Whole30 Weekly Meal Planner |
| **Category** | Health & Fitness |
| **Version** | 1.0 (initial) |
| **Minimum SDK** | 21+ |
| **Target SDK** | 34+ |
| **Privacy Policy** | PRIVACY-POLICY.md (GitHub) |
| **Terms of Service** | TERMS-OF-SERVICE.md (GitHub) |
| **Data Security** | DATA-SECURITY.md (GitHub) |
| **Support Email** | support@whole30planner.com |

---

## Additional Resources

- **Google Play Console:** https://play.google.com/console
- **App Publishing Guide:** https://developer.android.com/distribute
- **Play Policy Center:** https://support.google.com/googleplay/android-developer
- **Android Studio:** https://developer.android.com/studio

---

**Your app is ready for Google Play!** 🚀

Once approved, users worldwide can download and enjoy your Whole30 meal planning with full privacy protection.

*Package Name:* `com.fredswhole30.mealplanner`

---

*Last Updated: July 17, 2026*
