# Instacart Integration Guide

Complete guide for integrating Instacart with your Whole30 Weekly Meal Planner.

## Overview

This integration allows you to:
- ✅ Select items from your shopping list
- ✅ Add them directly to Instacart cart
- ✅ Compare prices across stores
- ✅ Track order history
- ✅ Save favorite items for quick reordering
- ✅ One-click ordering for recurring Whole30 staples

---

## Prerequisites

### What You Need
1. **Instacart Account** (free to create at instacart.com)
2. **Valid delivery/pickup address** in a supported area
3. **Payment method** on file with Instacart
4. **Updated location-settings.json** with your Instacart store preference

### Supported Areas
Instacart operates in most major US cities and some Canadian cities. Check coverage at:
https://www.instacart.com/

---

## Setup Instructions

### Step 1: Create/Update Your Instacart Account

1. Go to https://www.instacart.com
2. Sign up or log in
3. Add your delivery address
4. Verify payment method
5. Choose your preferred store(s)

**Popular Stores on Instacart:**
- Whole Foods
- Kroger
- Safeway
- Trader Joe's
- Costco
- Target
- Sprouts

### Step 2: Update Your Configuration

Edit `instacart-config.json` with your details:

```json
{
  "instacart": {
    "email": "your-email@example.com",
    "preferredStore": "Whole Foods",
    "deliveryZipCode": "12345",
    "savePaymentMethod": true,
    "autoAddToCart": false,
    "notes": "Update with your actual Instacart details"
  }
}
```

### Step 3: Enable Instacart Links

In `location-settings.json`, update:
```json
{
  "instacartIntegration": {
    "enabled": true,
    "preferredStore": "Whole Foods",
    "autoMatch": true,
    "notes": "When enabled, shopping lists will include Instacart links"
  }
}
```

### Step 4: Generate Your Shopping List

1. Copy `weekly-planner-template.md` and complete your weekly meal plan
2. Use `shopping-list-instacart.md` to organize ingredients
3. Check boxes next to items you want to order
4. Click "Add to Instacart" for each item or use "Add All to Instacart"

---

## How It Works

### Three Integration Levels

#### Level 1: Manual Selection (Easiest)
- Browse your shopping list
- Click checkboxes next to items
- Click "Add to Instacart" button
- Items open Instacart in new tab
- You complete checkout manually

**Best for:** Beginners, occasional shoppers

#### Level 2: Smart Matching (Recommended)
- System suggests Instacart products
- You verify/adjust quantities
- One-click add to cart
- Prices display in real-time
- Saves your favorite products

**Best for:** Regular shoppers, time-conscious users

#### Level 3: Full Automation (Advanced)
- Recurring orders enabled
- Favorite items pre-selected
- Auto-add to cart when threshold met
- 1-click checkout (requires saved payment)
- Scheduled delivery

**Best for:** Frequent Whole30 shoppers, convenience priority

---

## Understanding Instacart Integration

### What the Integration Does
- ✅ Links your shopping list items to Instacart products
- ✅ Shows real-time pricing from your selected store
- ✅ Allows one-click adding to cart
- ✅ Tracks order history
- ✅ Suggests substitutions if items unavailable
- ✅ Saves delivery preferences

### What It Does NOT Do
- ❌ Automatically charge your payment method (you must complete checkout)
- ❌ Access your personal Instacart data beyond what you authorize
- ❌ Share shopping data with third parties
- ❌ Modify your Instacart account without permission
- ❌ Require you to use Instacart (always optional)

---

## Security & Privacy

### Your Data
- **Shopping list:** Stored locally on your device
- **Instacart login:** Never stored in this system
- **Payment info:** Stored only on Instacart servers
- **Order history:** Optional - only if you enable tracking

### Safe Practices
1. ✅ Use strong, unique password for Instacart
2. ✅ Enable two-factor authentication on Instacart account
3. ✅ Review orders before confirming
4. ✅ Check delivery address before checkout
5. ✅ Report suspicious activity to Instacart
6. ✅ Log out after shopping sessions on shared devices

### Privacy Notice
This meal planner does NOT:
- Collect your Instacart login credentials
- Access your Instacart account without authorization
- Share data with Instacart or any third party
- Store payment information
- Track purchases beyond what you voluntarily log

---

## Step-by-Step: Adding Items to Instacart

### Method 1: Direct Link (Easiest)

1. Open `shopping-list-instacart.md`
2. Find your item
3. Click the "Add to Instacart" button
4. Browser opens Instacart product page
5. Verify quantity and add to cart
6. Continue shopping or checkout

**Example Item:**
```
☐ Organic Chicken Breast (2 lbs)
   [Add to Instacart] | [View Price] | [Add Alternatives]
```

### Method 2: Store Search (If link unavailable)

1. Go to instacart.com
2. Sign in to your account
3. Search for item name
4. Verify brand and quantity
5. Add to cart
6. Continue shopping

### Method 3: Smart Matching (Premium)

1. Enable smart matching in `instacart-config.json`
2. System suggests matching products
3. Review suggestions
4. Click to add to cart or customize
5. Confirm quantities
6. Items added to your Instacart cart

---

## Common Issues & Solutions

### "Item Not Found on Instacart"

**Reason:** Not all items are available on all stores

**Solution:**
- [ ] Try a different store
- [ ] Search for brand alternative
- [ ] Use substitution suggestion feature
- [ ] Check item availability in your zip code
- [ ] Try "Add Alternatives" to see similar products

### "Price Seems High"

**Reason:** Instacart adds service fees and markups

**Reason:** Store may have premium pricing

**Solution:**
- [ ] Compare with in-store prices
- [ ] Check multiple stores (Instacart shows options)
- [ ] Look for sales/promotions on Instacart
- [ ] Order larger quantities for better deals
- [ ] Use Instacart promotions ($10 off first order, etc.)

### "Delivery Address Not Available"

**Reason:** Your area may not be covered

**Solution:**
- [ ] Check coverage on instacart.com
- [ ] Try nearby zip codes
- [ ] Check if Instacart operates in your city
- [ ] Consider pickup option instead of delivery
- [ ] Contact Instacart support

### "Quantities Don't Match"

**Reason:** Instacart may not sell exact quantities you need

**Solution:**
- [ ] Round up to nearest available size
- [ ] Order multiple packages
- [ ] Check if bulk sizes available
- [ ] Use substitution feature
- [ ] Buy extras for freezing

### "Link Opens Wrong Page"

**Reason:** Instacart product pages may vary by store

**Solution:**
- [ ] Manually search for item name
- [ ] Verify store selection in config
- [ ] Try different store option
- [ ] Copy product name and search in app
- [ ] Clear browser cache and try again

---

## Store-Specific Tips

### Whole Foods
- ✅ Best selection of Whole30 items
- ✅ High quality meat and produce
- ✅ Organic options abundant
- ⚠️ Premium pricing
- 💡 Use Prime membership discount

### Kroger / Safeway
- ✅ Good variety of Whole30 staples
- ✅ Regular sales and promotions
- ✅ Loyalty program savings
- 💡 Check weekly ads before ordering

### Trader Joe's
- ✅ Excellent compliant items
- ✅ Competitive pricing
- ✅ High quality meat
- ⚠️ Limited selection (small store)
- 💡 Know what you want - items vary

### Sprouts Farmers Market
- ✅ Great produce selection
- ✅ Organic options
- ✅ Competitive pricing
- 💡 Perfect for farmers market feel

### Costco
- ✅ Bulk buying saves money
- ⚠️ Minimum order requirements
- 💡 Requires Costco membership
- 💡 Great for items you freeze

---

## Pro Tips for Instacart Ordering

### Save Money
1. **Check multiple stores** - Prices vary significantly
2. **Look for sales** - Instacart shows promotions
3. **Buy bulk** - Larger packages often cheaper per unit
4. **Use promotions** - First-time user discount, seasonal offers
5. **Track spending** - Note prices for future comparison

### Optimize Delivery
1. **Combine orders** - Fewer deliveries = more efficient
2. **Order off-peak** - Midweek orders may arrive faster
3. **Use pickup** - Often faster and saves delivery fees
4. **Set delivery window** - Narrow windows have better availability
5. **Schedule ahead** - Plan orders 1-2 days in advance

### Quality Control
1. **Check item freshness** - Review "best by" dates
2. **Specify substitutions** - Tell shopper your preferences
3. **Track orders** - Monitor shopper's selections in real-time
4. **Rate/review** - Help Instacart improve quality
5. **Report issues** - Missing/damaged items = refund/credit

### Shopping Strategy
1. **Create recurring list** - Save time on repeat items
2. **Note seasonal items** - Update list with seasonal produce
3. **Group by section** - Organize list like store layout
4. **Include quantities** - "2 lbs chicken" not just "chicken"
5. **Add notes** - "Organic preferred" or "Red apples only"

---

## Tracking Your Orders

### Order History
Update `instacart-config.json` to track:
- Order dates and totals
- Items frequently purchased
- Favorite stores and shoppers
- Spending trends
- Substitutions used

### Example Tracking:
```json
{
  "orderHistory": {
    "orderId": "12345",
    "date": "2026-07-17",
    "store": "Whole Foods",
    "total": "$87.50",
    "items": 23,
    "delivered": true,
    "deliveryTime": "10:30 AM - 11:00 AM"
  }
}
```

---

## Integrating with Your Meal Plan

### Workflow

1. **Plan meals** using `weekly-planner-template.md`
2. **Create shopping list** using `shopping-list-instacart.md`
3. **Select items** you want to order via Instacart
4. **Add to Instacart** using links or manual search
5. **Review order** before checkout
6. **Confirm delivery** time and address
7. **Track shopper** real-time
8. **Rate experience** and note substitutions

### Seasonal Ordering
- **Spring:** Fresh greens, asparagus, peas, strawberries
- **Summer:** Tomatoes, berries, zucchini, corn
- **Fall:** Squash, root veggies, apples, kale
- **Winter:** Citrus, stored root veggies, hardy greens

Use `seasonal-produce-guide.md` to know what's in season!

---

## Troubleshooting & Support

### Common Questions

**Q: Is my payment information safe?**
A: Yes. Payment info is stored only on Instacart's secure servers, never in this meal planner.

**Q: Can I use Instacart without this system?**
A: Yes! This system just adds convenience. You can always shop Instacart directly.

**Q: What if an item is unavailable?**
A: Instacart will notify you and suggest alternatives you can accept/reject.

**Q: Can I schedule recurring orders?**
A: Yes, through Instacart's "Saved Carts" or "Recurring Orders" feature.

**Q: How much does Instacart cost?**
A: Service fees (~$3.99-5.99) + delivery/markup. Check their pricing.

### Getting Help

**For this meal planner:**
- Check README.md for general issues
- See CUSTOMIZATION-GUIDE.md for meal planning questions
- Review SHOPPING-FREQUENCY-GUIDE.md for shopping strategy

**For Instacart issues:**
- Visit help.instacart.com
- Contact Instacart customer support
- Check your Instacart account settings
- Review app FAQs

---

## Advanced Features (Coming Soon)

- 📱 Mobile app integration
- 🤖 AI-powered price optimization
- 📊 Spending analytics dashboard
- 🔄 Automatic reordering for staples
- 💳 Multi-store price comparison
- 📦 Delivery scheduling automation
- 📲 SMS/email order updates

---

## Getting Started Checklist

- [ ] Created/logged into Instacart account
- [ ] Added delivery address
- [ ] Verified payment method
- [ ] Selected preferred store(s)
- [ ] Updated `instacart-config.json`
- [ ] Updated `location-settings.json`
- [ ] Created weekly meal plan
- [ ] Generated shopping list with Instacart links
- [ ] Added first items to Instacart cart
- [ ] Completed first order
- [ ] Tracked delivery and rated experience

---

## Ready to Order! 🛒

You're all set to use Instacart with your Whole30 meal planner!

**Next steps:**
1. Plan your week with `weekly-planner-template.md`
2. Generate your shopping list with `shopping-list-instacart.md`
3. Click "Add to Instacart" for your items
4. Complete checkout on Instacart
5. Track your delivery
6. Enjoy your Whole30 meals!

Happy shopping! 🥬🍗🥑

---

**Questions?** See `instacart-user-guide.md` for detailed step-by-step instructions with screenshots.
