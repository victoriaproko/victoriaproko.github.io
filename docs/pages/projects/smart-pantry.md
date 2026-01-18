---
layout: project-page
title: "Smart Pantry"
short_description: "Reducing Food Waste through Intelligent Inventory Management."
role: "Product Manager & Lead Developer"
tools: "Java, JSON, DeepSeek API, JUnit"
timeline: "Winter 2025 (3-week Sprint)"
permalink: /projects/smart-pantry/
---

**[ GitHub Repository](https://github.com/CharlotteWangv587/cs62FinalProject_Smart-Pantry-Inventory-Tracker)**

## Overview
The Smart Pantry was conceived to solve a critical user friction point: **the cognitive load of managing expiring ingredients.** Many users struggle with "recipe paralysis"—knowing an item is expiring but failing to find a creative way to use it—resulting in unnecessary household waste.

Our solution is a data-driven inventory tracker that automates prioritization. By leveraging specialized data structures, the system proactively suggests recipes that maximize existing stock and generates optimized grocery lists for missing items.

---

## Inquiry
To validate our product direction, we conducted interviews with a diverse cohort, including on-campus students, off-campus residents, and professors. We identified two core friction points:

* **Core Friction:** Users often forget items in the "back of the fridge," only discovering them when it’s too late to cook.
* **Creativity Gap:** Users expressed frustration with "redundant recipes" and the time-sink of searching blogs for meals that match their specific, expiring ingredients.

**The Goal:** Shift the user from reactive searching to proactive, algorithmic guidance.

---

## Technical Scaffolding & Architecture
We prioritized a system architecture that balanced search speed with automated prioritization for a dataset of over 1,000 entries.

<div style="text-align: center; margin: 20px 0;">
  <img src="/assets/architecture.jpg" alt="Smart Pantry System Architecture" style="border-radius: 12px; border: 1px solid #eee; width: 100%; max-width: 800px;">
  <p style="font-size: 0.8em; color: #666;">System Architecture: From CSV Data to LLM-powered Recipe Suggestions</p>
</div>

### Data Structures
We utilized an **ArrayList** for efficient CSV integration and general record storage, paired with a **Priority Queue** for $O(\log N)$ efficiency in extracting the soonest-expiring items.

### The Matching Engine
The program calculates a "match percentage" between the user’s pantry and a JSON-based recipe database. 

### API Integration (The "Smart" Layer)
For users wanting more flexibility, we implemented a feature that sends a snapshot of the user's pantry to the **DeepSeek LLM** via API call to generate bespoke, ingredient-aware suggestions.

---

## Key Product Features

1.  **Prioritized Inventory:** Automatically bubbles up the top ingredients needing immediate attention based on expiration dates.
2.  **Dynamic Grocery Generation:** Instead of a generic list, the system outputs exactly what is needed (with quantities) to complete a specific suggested meal.
3.  **Intelligent Substitution:** The LLM integration allows for ingredient-aware substitutions, such as using Korean *doenjang* as a savory base instead of vegetable broth.

---

## Future Roadmap & Strategy
A key takeaway from this project was the importance of **affordance analysis**. Moving forward, the product roadmap focuses on:

* **Customization:** Adding support for non-standard diets, including medical needs and allergies.
* **Diversity:** Expanding the recipe database beyond Western-centric cuisines to ensure the tool serves a broader user base.
* **Frictionless Entry:** Refining CSV parsing to handle varied unit formats and misformatted dates more gracefully.
