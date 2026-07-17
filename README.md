# Fred's Whole30 Weekly Meal Planner

A comprehensive meal planning tool for the Whole30 program, designed to help you stay compliant while enjoying delicious, nourishing meals.

## What is Whole30?

Whole30 is a 30-day elimination diet that helps you identify how different foods affect your body. It focuses on:
- **Whole foods**: Meat, seafood, eggs, vegetables, fruit, and healthy fats
- **No grains, legumes, dairy, sugar, or alcohol**
- Eating real food prepared at home

## About This Planner

This meal planner helps you:
- ✅ Plan weekly meals that are Whole30-compliant
- ✅ Keep track of breakfast, lunch, dinner, and snacks
- ✅ Generate organized shopping lists
- ✅ Manage ingredient combinations for efficiency
- ✅ Track meals across your 30-day journey
- ✅ Customize meals based on your dietary preferences
- ✅ Shop at your preferred frequency (1x, 2x, or 3x per week)

## How to Use

### Step 1: Customize Your Preferences
1. Edit `dietary-preferences.json` to exclude foods you don't want to eat
2. Edit `shopping-preferences.json` to choose your shopping frequency (1x, 2x, or 3x weekly)
3. Read `CUSTOMIZATION-GUIDE.md` for detailed help

### Step 2: Choose Your Meals
Browse the **meals.json** file for pre-approved Whole30 recipes, or add your own based on your excluded foods.

### Step 3: Fill Out Your Weekly Plan
Use the **weekly-planner-template.md** to plan your meals for the week. Copy the template and fill it with your chosen meals.

### Step 4: Generate Your Shopping List
1. Read `SHOPPING-FREQUENCY-GUIDE.md` to understand your shopping strategy
2. Use the **shopping-list.md** template to organize all ingredients needed
3. Follow the split by shopping trip (e.g., "Sunday" vs "Wednesday" vs "Friday")

### Step 5: Prep & Execute
Follow the **meal-prep-guide.md** for Sunday prep strategy and save time all week!

### Step 6: Track Your Progress
Use **30-day-tracker.md** to log daily energy, sleep, cravings, and compliance.

## Repository Structure

```
Freds-Whole30/
├── README.md                          # This file
├── dietary-preferences.json           # Customize excluded foods
├── CUSTOMIZATION-GUIDE.md             # How to exclude foods
├── shopping-preferences.json          # Choose 1x, 2x, or 3x shopping
├── SHOPPING-FREQUENCY-GUIDE.md        # Detailed shopping strategies
├── weekly-planner-template.md         # Copy for each week
├── 30-day-tracker.md                  # Track your 30 days
├── meals.json                         # Recipe database
├── shopping-list.md                   # Shopping list template
├── meal-prep-guide.md                 # Meal prep strategies
└── weeks/                             # (Optional) Completed weekly plans
    ├── week-1.md
    ├── week-2.md
    └── ...
```

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

## Key Features

### 🎯 Customizable
- Exclude foods you don't want in your plan
- Modify recipes to fit your preferences
- Easy to use JSON configuration files

### 🛒 Flexible Shopping
- Choose to shop 1x, 2x, or 3x per week
- First trip buys all shelf-stable items
- Subsequent trips refresh fresh items only
- Clear guidance on what to buy each trip

### 📋 Complete Planning Tools
- 20+ pre-built Whole30-compliant recipes
- Weekly meal planner template
- Organized shopping lists
- Detailed meal prep guide

### 📊 Progress Tracking
- 30-day daily tracker
- Energy and sleep tracking
- Symptom monitoring
- Weekly reflection prompts
- Reintroduction planning guide

## Tips for Success

1. **Prep ahead**: Dedicate a few hours on Sunday for meal prep
2. **Keep it simple**: You don't need complex recipes—simple is best
3. **Read labels**: Many "healthy" foods contain sneaky non-compliant ingredients
4. **Stay hydrated**: Drink plenty of water throughout the day
5. **Plan for eating out**: When dining out, ask for modifications (protein + veggies + fat)
6. **Customize your plan**: Use the preference files to exclude foods you don't enjoy
7. **Pick your shopping frequency**: Choose 1x, 2x, or 3x weekly based on your schedule
8. **Track your journey**: Use the 30-day tracker to monitor your progress

## Shopping Frequency Options

### 🛍️ 1x Per Week (Sunday)
- Best for: Busy schedules, good meal prep skills
- Buy: All shelf-stable items + 7 days fresh
- Pro: Fewer store trips, better for bulk buying
- Con: Some produce less fresh by end of week

### 🛍️ 2x Per Week (Sunday + Wednesday)
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

## Getting Started Checklist

Before your first week of Whole30:

- [ ] I've read this README
- [ ] I've updated `dietary-preferences.json` with my food exclusions
- [ ] I've added any allergies to `dietary-preferences.json`
- [ ] I've chosen my shopping frequency in `shopping-preferences.json`
- [ ] I've read `SHOPPING-FREQUENCY-GUIDE.md`
- [ ] I've reviewed `meals.json` for recipes I like
- [ ] I've copied `weekly-planner-template.md` for Week 1
- [ ] I've planned my meals for Week 1
- [ ] I've created my shopping list using `shopping-list.md`
- [ ] I've read `meal-prep-guide.md` for prep strategies
- [ ] I've printed or downloaded `30-day-tracker.md`
- [ ] I'm ready to start!

## Whole30 Resources

- [Official Whole30 Website](https://whole30.com)
- [Whole30 Program Rules](https://whole30.com/whole30-program-rules)
- [Whole30 Approved Foods List](https://whole30.com/downloads)
- [Whole30 Frequently Asked Questions](https://whole30.com/faq)

## Troubleshooting & Common Questions

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

---

## 🎉 You've Got This!

You have everything you need to succeed on your Whole30 journey. The combination of customizable preferences, flexible shopping options, detailed meal planning, and comprehensive tracking will set you up for success.

**Remember: This is about learning how different foods affect your body. Be kind to yourself, stay compliant, and trust the process.**

Happy cooking! 🍗 🥦 🥑

---

**Questions?** Refer to the specific guide files:
- Customizing meals? → `CUSTOMIZATION-GUIDE.md`
- Shopping strategy? → `SHOPPING-FREQUENCY-GUIDE.md`
- Meal prep? → `meal-prep-guide.md`
- Tracking progress? → `30-day-tracker.md`
