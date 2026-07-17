# Fred's Whole30 Weekly Meal Planner

A comprehensive meal planning tool for the Whole30 program, designed to help you stay compliant while enjoying delicious, nourishing meals—with enterprise-grade privacy and security protection.

## 🔒 Your Privacy & Security Matter

**Your data is protected and remains 100% private to you and the app only.**

- ✅ **Military-Grade Encryption:** AES-256 encryption for all sensitive data
- ✅ **Never Sold:** Your data is never sold to third parties, period
- ✅ **GDPR Compliant:** Full compliance with international privacy laws
- ✅ **Your Control:** Access, download, or delete your data anytime
- ✅ **Transparent:** Complete security documentation included

**Read our privacy commitments:**
- 📋 **PRIVACY-POLICY.md** - Your data rights and protections
- 🔐 **DATA-SECURITY.md** - How we encrypt and protect your information
- ⚖️ **TERMS-OF-SERVICE.md** - Legal terms and your responsibilities

---

## What is Whole30?

Whole30 is a 30-day elimination diet that helps you identify how different foods affect your body. It focuses on:
- **Whole foods**: Meat, seafood, eggs, vegetables, fruit, and healthy fats
- **No grains, legumes, dairy, sugar, or alcohol**
- Eating real food prepared at home

---

## About This Planner

This meal planner helps you:
- ✅ Plan weekly meals that are Whole30-compliant
- ✅ Keep track of breakfast, lunch, dinner, and snacks
- ✅ Generate organized shopping lists
- ✅ Manage ingredient combinations for efficiency
- ✅ Track meals across your 30-day (or 52-week) journey
- ✅ Customize meals based on your dietary preferences
- ✅ Shop at your preferred frequency (1x, 2x, or 3x per week)
- ✅ Order directly through Instacart integration
- ✅ Track seasonal produce and recipes
- ✅ Monitor energy, mood, and digestion for a full year

---

## 🛡️ Security & Privacy Features

### Your Data is Private
- ✅ All data encrypted (AES-256 at rest, TLS 1.3 in transit)
- ✅ Passwords hashed with Bcrypt (never stored plaintext)
- ✅ Local storage on your device
- ✅ No cookies tracking you across websites
- ✅ No analytics following you

### Your Data is Yours
- ✅ Download your data anytime
- ✅ Delete your account anytime (all data removed)
- ✅ Control what's collected
- ✅ Opt-out of optional features
- ✅ Export to use elsewhere

### Never Shared
- ✅ No selling to advertisers
- ✅ No sharing with data brokers
- ✅ No selling to health companies
- ✅ No sharing with employers
- ✅ No renting to marketing firms

**See PRIVACY-POLICY.md for complete details on what we collect, how we use it, and your rights.**

---

## How to Use

### Step 1: Understand Your Privacy
1. Read **PRIVACY-POLICY.md** - Know how your data is protected
2. Read **TERMS-OF-SERVICE.md** - Understand the legal agreement
3. Read **DATA-SECURITY.md** - Learn about encryption and security

### Step 2: Customize Your Preferences
1. Edit `dietary-preferences.json` to exclude foods you don't want to eat
2. Edit `shopping-preferences.json` to choose your shopping frequency (1x, 2x, or 3x weekly)
3. Edit `location-settings.json` to set your region for seasonal produce
4. Read `CUSTOMIZATION-GUIDE.md` for detailed help

### Step 3: Choose Your Meals
Browse the **meals.json** file for pre-approved Whole30 recipes, or add your own based on your excluded foods.

### Step 4: Fill Out Your Weekly Plan
Use the **weekly-planner-template.md** to plan your meals for the week. Copy the template and fill it with your chosen meals.

### Step 5: Generate Your Shopping List
1. Read `SHOPPING-FREQUENCY-GUIDE.md` to understand your shopping strategy
2. Use the **shopping-list.md** or **shopping-list-instacart.md** template to organize ingredients
3. Follow the split by shopping trip (e.g., "Sunday" vs "Wednesday" vs "Friday")
4. (Optional) Use Instacart integration for one-click ordering

### Step 6: Prep & Execute
Follow the **meal-prep-guide.md** for Sunday prep strategy and save time all week!

### Step 7: Track Your Progress
- Use **30-day-tracker.md** to log daily energy, sleep, cravings, and compliance
- Use **seasonal-tracker.md** for year-round tracking (52 weeks + monthly + quarterly + annual reviews)

---

## Repository Structure

```
Freds-Whole30/
├── README.md                              # This file
├── PRIVACY-POLICY.md                      # 🔐 Your privacy rights
├── DATA-SECURITY.md                       # 🔒 How we protect your data
├── TERMS-OF-SERVICE.md                    # ⚖️ Legal terms
│
├── dietary-preferences.json               # Customize excluded foods
├── CUSTOMIZATION-GUIDE.md                 # How to exclude foods
├── shopping-preferences.json              # Choose 1x, 2x, or 3x shopping
├── SHOPPING-FREQUENCY-GUIDE.md            # Detailed shopping strategies
├── location-settings.json                 # Your location for seasonal produce
│
├── weekly-planner-template.md             # Copy for each week
├── 30-day-tracker.md                      # Track your 30 days
├── seasonal-tracker.md                    # Track full 52 weeks + annual review
│
├── meals.json                             # Recipe database (50+ recipes)
├── seasonal-recipes.json                  # Seasonal recipes (25+)
├── seasonal-produce-guide.md              # Seasonal produce by location
│
├── shopping-list.md                       # Shopping list template
├── shopping-list-instacart.md             # Shopping list with Instacart links
├── meal-prep-guide.md                     # Meal prep strategies
│
├── instacart-integration.md               # Instacart setup guide
├── instacart-config.json                  # Instacart configuration
├── instacart-user-guide.md                # Step-by-step Instacart instructions
│
└── weeks/                                 # (Optional) Completed weekly plans
    ├── week-1.md
    ├── week-2.md
    └── ...
```

---

## Whole30 Rules at a Glance

### ✅ Approved Foods
- Meat, poultry, seafood (all cuts)
- Eggs
- All vegetables (including starchy like potatoes)
- Fruit
- Nuts, seeds, and nut butters (except peanuts)
- Ghee, coconut oil, avocado oil
- Cooking fats from approved animals

### ❌ Not Allowed
- Grains (wheat, corn, rice, oats, etc.)
- Legumes (beans, lentils, peanuts, soy)
- Dairy (milk, cheese, yogurt)
- Sugar & sweeteners (except small amounts of honey for cooking)
- Alcohol
- Processed foods

---

## Key Features

### 🔐 Privacy-First Design
- Military-grade encryption
- No data sold or shared
- Your data stays on your device
- GDPR & CCPA compliant
- Complete transparency

### 🎯 Customizable
- Exclude foods you don't want in your plan
- Modify recipes to fit your preferences
- Easy to use JSON configuration files
- Dietary preference management

### 🛒 Flexible Shopping with Instacart Integration
- Choose to shop 1x, 2x, or 3x per week
- One-click add items to Instacart cart
- Track prices across multiple stores
- First trip buys all shelf-stable items
- Subsequent trips refresh fresh items only
- Clear guidance on what to buy each trip

### 📋 Complete Planning Tools
- 50+ pre-built Whole30-compliant recipes
- 25+ seasonal recipes by location
- Weekly meal planner template
- Organized shopping lists
- Detailed meal prep guide
- Instacart integration for online ordering

### 🌍 Seasonal Awareness
- Location-based seasonal produce guides
- 8 regions supported (US, Canada, Europe, Australia)
- In-season recipes for spring, summer, fall, winter
- Money-saving seasonal shopping strategies
- Storage tips for seasonal items

### 📊 Progress Tracking
- 30-day daily tracker
- 52-week full-year tracker
- Energy and sleep tracking
- Symptom monitoring
- Monthly reflections
- Quarterly reviews
- Annual summary with insights
- Reintroduction planning guide

---

## Tips for Success

1. **Prep ahead**: Dedicate a few hours on Sunday for meal prep
2. **Keep it simple**: You don't need complex recipes—simple is best
3. **Read labels**: Many "healthy" foods contain sneaky non-compliant ingredients
4. **Stay hydrated**: Drink plenty of water throughout the day
5. **Plan for eating out**: When dining out, ask for modifications (protein + veggies + fat)
6. **Customize your plan**: Use the preference files to exclude foods you don't enjoy
7. **Pick your shopping frequency**: Choose 1x, 2x, or 3x weekly based on your schedule
8. **Track your journey**: Use the 30-day or 52-week tracker to monitor your progress
9. **Understand your data**: Read PRIVACY-POLICY.md to know how your data is protected
10. **Use Instacart**: One-click ordering saves time and keeps you on track

---

## Shopping Frequency Options

### 🛍️ 1x Per Week (Sunday)
- Best for: Busy schedules, good meal prep skills
- Buy: All shelf-stable items + 7 days fresh
- Pro: Fewer store trips, better for bulk buying
- Con: Some produce less fresh by end of week

### 🛍️ 2x Per Week (Sunday + Wednesday) ⭐ **RECOMMENDED**
- Best for: Most people - the sweet spot!
- Buy: All pantry Sunday + 4 days fresh, then Wednesday 3 days fresh only
- Pro: Balance of convenience and freshness
- Con: Two trips, but Wednesday is quick

### 🛍️ 3x Per Week (Sunday + Wednesday + Friday)
- Best for: Fresh produce lovers, flexible schedules
- Buy: All pantry Sunday + 3 days fresh, then Wednesday & Friday refresh trips
- Pro: Maximum freshness, flexibility
- Con: Three store trips per week

See `SHOPPING-FREQUENCY-GUIDE.md` for detailed instructions for each frequency.

---

## Instacart Integration

### Easy One-Click Ordering

1. ✅ Plan your meals
2. ✅ Generate shopping list
3. ✅ Click "Add to Instacart" for items
4. ✅ Complete checkout on Instacart
5. ✅ Track delivery in real-time

### How Instacart Integration Works

- **Optional:** You choose to link or not
- **Secure:** No passwords stored, OAuth tokens only
- **Private:** Instacart data handled separately
- **Easy:** Direct links to add items
- **Safe:** Payment info stays with Instacart

**See instacart-user-guide.md for complete step-by-step instructions.**

---

## Your Data Privacy & Security

### We Protect Your Information With:

| Protection | What It Means |
|-----------|--------------|
| **AES-256 Encryption** | Military-grade encryption for stored data |
| **TLS 1.3 HTTPS** | Bank-level security for data in transit |
| **Bcrypt Hashing** | Passwords can't be reversed if hacked |
| **No Password Storage** | We never store your password in plain text |
| **Encrypted Backups** | Even backup data is encrypted |
| **Limited Access** | Only necessary staff can access systems |
| **Audit Logging** | Every access is logged and monitored |
| **Regular Testing** | Quarterly penetration tests |
| **24/7 Monitoring** | Security team watches 24/7 |
| **Incident Response** | Breach notification within 72 hours |

### Your Rights

- ✅ **See your data**: Download everything anytime
- ✅ **Control your data**: Decide what's collected
- ✅ **Delete your data**: Permanent deletion, no recovery
- ✅ **Export your data**: Take it with you to another app
- ✅ **Opt-out**: Disable optional tracking
- ✅ **Change privacy settings**: Control your experience

**See DATA-SECURITY.md for technical details on encryption and security measures.**

---

## Getting Started Checklist

Before your first week of Whole30:

- [ ] I've read this README
- [ ] I've read PRIVACY-POLICY.md (understand my privacy rights)
- [ ] I've read DATA-SECURITY.md (understand how my data is protected)
- [ ] I've read TERMS-OF-SERVICE.md (understand legal agreement)
- [ ] I've updated `dietary-preferences.json` with my food exclusions
- [ ] I've added any allergies to `dietary-preferences.json`
- [ ] I've chosen my shopping frequency in `shopping-preferences.json`
- [ ] I've set my location in `location-settings.json`
- [ ] I've read `SHOPPING-FREQUENCY-GUIDE.md`
- [ ] I've reviewed `meals.json` for recipes I like
- [ ] I've copied `weekly-planner-template.md` for Week 1
- [ ] I've planned my meals for Week 1
- [ ] I've created my shopping list using `shopping-list.md` or `shopping-list-instacart.md`
- [ ] I've read `meal-prep-guide.md` for prep strategies
- [ ] I've printed or downloaded `30-day-tracker.md` and `seasonal-tracker.md`
- [ ] I'm ready to start!

---

## Whole30 Resources

- [Official Whole30 Website](https://whole30.com)
- [Whole30 Program Rules](https://whole30.com/whole30-program-rules)
- [Whole30 Approved Foods List](https://whole30.com/downloads)
- [Whole30 Frequently Asked Questions](https://whole30.com/faq)

---

## Troubleshooting & Common Questions

**Q: Is my personal information safe?**  
A: Yes! Your data is encrypted with military-grade AES-256 encryption, never sold, and protected by GDPR/CCPA standards. See PRIVACY-POLICY.md for complete details.

**Q: Can I modify recipes?**  
A: Absolutely! Use the `CUSTOMIZATION-GUIDE.md` to swap out ingredients you don't like.

**Q: How do I handle restaurant meals?**  
A: Order grilled protein + vegetables + healthy fat. Ask for no grains/sugar/dairy.

**Q: What if I slip up?**  
A: The official Whole30 rules say you start over, but focus on compliance going forward. Don't beat yourself up!

**Q: How do I know what to eat for snacks?**  
A: Check `meals.json` for approved snack options, or eat leftover meals from previous days.

**Q: Can I do Whole30 while traveling?**  
A: Yes! Plan ahead, pack approved snacks, and research restaurant options at your destination.

**Q: What's the reintroduction phase?**  
A: After Day 30, you systematically add back foods to identify what bothers you. See `30-day-tracker.md` for the reintroduction guide.

**Q: How does Instacart integration work?**  
A: Optional! Link your Instacart account, add items to cart with one click, and complete checkout on Instacart. See `instacart-user-guide.md` for step-by-step instructions.

**Q: Is my Instacart data safe?**  
A: Yes! We use OAuth tokens (never store passwords), all data is encrypted, and Instacart's security is separate from ours. See `DATA-SECURITY.md` for technical details.

**Q: What if I have privacy concerns?**  
A: Contact us at privacy@whole30planner.com. We're happy to explain how we protect your information. All policies are transparent and public.

---

## Getting Help

### For Different Topics:

| Topic | File |
|-------|------|
| Customizing meals | `CUSTOMIZATION-GUIDE.md` |
| Shopping strategy | `SHOPPING-FREQUENCY-GUIDE.md` |
| Meal prep | `meal-prep-guide.md` |
| Tracking progress | `30-day-tracker.md` or `seasonal-tracker.md` |
| **Your privacy** | **`PRIVACY-POLICY.md`** |
| **Data security** | **`DATA-SECURITY.md`** |
| **Legal terms** | **`TERMS-OF-SERVICE.md`** |
| Instacart setup | `instacart-integration.md` |
| Instacart step-by-step | `instacart-user-guide.md` |
| Seasonal meals | `seasonal-recipes.json` |
| Seasonal produce | `seasonal-produce-guide.md` |
| Full-year tracking | `seasonal-tracker.md` |

---

## Legal & Privacy

**Your privacy and data protection are non-negotiable.**

- 📋 **PRIVACY-POLICY.md** - Comprehensive privacy policy (GDPR/CCPA compliant)
- 🔐 **DATA-SECURITY.md** - Technical security documentation
- ⚖️ **TERMS-OF-SERVICE.md** - Legal terms and medical disclaimer

**Key promises:**
- ✅ Your data is never sold
- ✅ Your data is encrypted
- ✅ Your data is yours to delete
- ✅ We comply with all privacy laws
- ✅ We're transparent about everything

---

## 🎉 You've Got This!

You have everything you need to succeed on your Whole30 journey. The combination of customizable preferences, flexible shopping options, detailed meal planning, comprehensive tracking, **and enterprise-grade privacy protection** will set you up for success.

**Remember:** 
- This is about learning how different foods affect your body
- Be kind to yourself, stay compliant, and trust the process
- Your data is safe, private, and protected
- We're here to support your journey

---

**Happy cooking! 🍗 🥦 🥑**

---

**Questions?** Refer to the specific guide files:
- Privacy concerns? → `PRIVACY-POLICY.md`
- Data security? → `DATA-SECURITY.md`
- Legal questions? → `TERMS-OF-SERVICE.md`
- Customizing meals? → `CUSTOMIZATION-GUIDE.md`
- Shopping strategy? → `SHOPPING-FREQUENCY-GUIDE.md`
- Meal prep? → `meal-prep-guide.md`
- Tracking progress? → `30-day-tracker.md` or `seasonal-tracker.md`
- Instacart help? → `instacart-user-guide.md`

---

*Your privacy is not negotiable. We protect it like our own.*

**Last Updated:** July 17, 2026
