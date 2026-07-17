# Customize Your Whole30 Meal Plan

Don't like certain foods? **No problem!** Use this guide to customize your meal plan by excluding foods you don't want to eat.

---

## How to Customize Your Plan

### Option 1: Use the Dietary Preferences File (Recommended)

1. Open `dietary-preferences.json` in this repository
2. For each food item you want to exclude, change the value from `false` to `true`
3. Add any allergies or special notes in the `allergies` section
4. Share this file with the meal planner to filter suggestions

**Example:**
```json
"excludedProteins": {
  "beef": true,        // I don't eat beef - exclude it!
  "chicken": false,    // I eat chicken - include it
  "shrimp": true       // I'm allergic to shrimp - exclude it!
}
```

---

### Option 2: Manually Filter Meals

If you prefer not to use the JSON file, simply:

1. Review `meals.json` to see all available recipes
2. Note which meals contain ingredients you want to exclude
3. Cross out those meals from your `weekly-planner-template.md`
4. Replace them with meals that match your preferences

---

## Quick Reference: Food Categories to Customize

### 🥩 Proteins
Choose which protein sources you want included:
- [ ] Beef (steak, ground beef, roasts)
- [ ] Pork
- [ ] Chicken (breast, thighs, whole)
- [ ] Turkey
- [ ] Lamb
- [ ] Seafood (salmon, shrimp, other fish)
- [ ] Eggs

**Exclude:** ___________________________________

### 🥬 Vegetables
Choose which vegetables you want included:
- [ ] Broccoli
- [ ] Cauliflower
- [ ] Brussels Sprouts
- [ ] Carrots
- [ ] Sweet Potatoes
- [ ] Bell Peppers
- [ ] Zucchini
- [ ] Asparagus
- [ ] Green Beans
- [ ] Spinach & Kale
- [ ] Mushrooms
- [ ] Onions
- [ ] Tomatoes
- [ ] Other: ___________________________________

**Exclude:** ___________________________________

### 🍎 Fruits
Choose which fruits you want included:
- [ ] Apples
- [ ] Bananas
- [ ] Berries (blueberries, strawberries, raspberries)
- [ ] Oranges & Citrus
- [ ] Avocados
- [ ] Other: ___________________________________

**Exclude:** ___________________________________

### 🥑 Healthy Fats
Choose which fats you want included:
- [ ] Ghee
- [ ] Coconut Oil
- [ ] Avocado Oil
- [ ] Olive Oil
- [ ] Almonds & Almond Butter
- [ ] Cashews
- [ ] Walnuts
- [ ] Pecans
- [ ] Tahini (Sesame)
- [ ] Olives
- [ ] Coconut (shredded)
- [ ] Other: ___________________________________

**Exclude:** ___________________________________

### 🧂 Seasonings & Herbs
Choose which seasonings you want included:
- [ ] Garlic
- [ ] Onion Powder
- [ ] Cilantro
- [ ] Basil
- [ ] Oregano
- [ ] Thyme
- [ ] Rosemary
- [ ] Cumin
- [ ] Paprika
- [ ] Chili Powder
- [ ] Other: ___________________________________

**Exclude:** ___________________________________

---

## Common Customization Scenarios

### Scenario 1: "I don't eat seafood"

**What to exclude in `dietary-preferences.json`:**
```json
"excludedProteins": {
  "salmon": true,
  "shrimp": true
}
```

**Impact:** 
- Removes: Baked Salmon, Shrimp & Zucchini Noodles
- Keep: Chicken, Ground Beef, Turkey meals

---

### Scenario 2: "I'm allergic to shellfish AND I don't like mushrooms"

**What to exclude:**
```json
"excludedProteins": {
  "shrimp": true
},
"excludedVegetables": {
  "mushrooms": true
},
"allergies": {
  "items": ["shellfish", "shrimp"]
}
```

**Impact:**
- Removes: Any meals with shrimp or mushrooms
- Keep: All other meals

---

### Scenario 3: "I'm vegetarian/only eat certain proteins"

**What to exclude:**
```json
"excludedProteins": {
  "beef": true,
  "pork": true,
  "lamb": true,
  "chicken": true,
  "turkey": true,
  "seafood": true,
  "salmon": true,
  "shrimp": true
}
```

**Note:** Whole30 is designed around animal proteins. For a vegetarian Whole30 variant, you'll rely heavily on eggs. This is possible but requires modification.

---

### Scenario 4: "I have a nut allergy"

**What to exclude:**
```json
"excludedHealthyFats": {
  "almonds": true,
  "almond_butter": true,
  "cashews": true,
  "walnuts": true,
  "pecans": true,
  "tahini": true
},
"allergies": {
  "items": ["nuts", "tree nuts", "peanuts", "sesame"]
}
```

**Impact:**
- Removes: Apple with Almond Butter, Olives & Nuts, Carrots with Tahini snacks
- Keep: All other meals and snacks

---

### Scenario 5: "I'm sensitive to garlic and onions"

**What to exclude:**
```json
"excludedSeasonings": {
  "garlic": true,
  "onion_powder": true
},
"notes": "Cannot consume garlic or onions - FODMAP sensitivity"
```

**Impact:**
- Removes many recipes with garlic/onion base
- Requires substituting with milder herbs (basil, oregano, thyme)

---

## How to Apply Your Preferences

### When Planning Your Week:

1. **Open your `dietary-preferences.json`** to remind yourself what you're excluding
2. **Reference `meals.json`** to find recipes that match your preferences
3. **Check ingredients** of any recipe you're considering - even "chicken" recipes may have garlic if you exclude it
4. **Note which meals work for you** and build your weekly plan around those

### When Meal Prepping:

1. **Cross-reference** your prep list with your exclusions
2. **Substitute ingredients** as needed (e.g., different seasonings, oil types)
3. **Label prepared meals** so household members know what you can eat

---

## Modifying Individual Recipes

### If you like a meal but not all ingredients:

**Original Recipe:** Herb-Roasted Chicken with Vegetables
- Ingredients: Chicken, sweet potato, carrots, broccoli, garlic, ghee

**Your Modification (no garlic):**
- Ingredients: Chicken, sweet potato, carrots, broccoli, **thyme instead of garlic**, ghee

**Result:** Same great meal, customized for you!

---

## Adding New Preferences Over Time

As you progress through your Whole30:

1. **You may discover new dislikes** - add them to your exclusion list
2. **You may find unexpected favorites** - remove them from exclusions
3. **Update `dietary-preferences.json`** as your tastes evolve
4. **Copy the updated file** to your weekly planner for next week

---

## Pro Tips for Customization

### ✅ DO:
- Be specific (e.g., "salmon" not just "seafood" if you'll eat other fish)
- Include allergies in the `allergies` section for safety
- Update preferences weekly as you discover what you like/dislike
- Substitute excluded ingredients rather than skipping meals
- Try new foods in small quantities to confirm dislikes

### ❌ DON'T:
- Exclude so many foods that you have no meal options
- Be afraid to modify recipes to fit your preferences
- Give up if your first week doesn't feel perfect
- Forget to check ingredient lists for hidden allergens
- Exclude foods out of habit - this is your chance to rediscover what you actually enjoy!

---

## Still Want Help?

If you're unsure about customizing your plan:

1. **Start conservative:** Only exclude foods you definitely don't want
2. **Add more exclusions as needed** as you meal plan
3. **Review official Whole30 resources** at whole30.com for guidance
4. **Remember:** Your plan should work for YOU - make it enjoyable!

---

## Your Customization Checklist

Before your first week of Whole30:

- [ ] I've reviewed `dietary-preferences.json`
- [ ] I've updated it with my food exclusions
- [ ] I've noted any allergies in the `allergies` section
- [ ] I've reviewed `meals.json` for recipes that fit my preferences
- [ ] I've planned my first week using only included meals
- [ ] I've printed or bookmarked my exclusion list for reference
- [ ] I'm ready to start my customized Whole30 journey!

**Let's go! 🚀**
