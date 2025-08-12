# 🥗 Optimizing Nutritional Meal Logistics for School Programs

Design cost-effective, USDA-compliant school lunch trays for students aged 9–12 using binary optimization in Excel Solver and Pyomo, with integrated nutrition and price data.

## 🎯 Problem Statement

School meal programs must deliver affordable, nutritious meals within strict budgets and USDA nutrition standards while accommodating student preferences and dietary restrictions. This project builds an optimization model that selects daily lunch trays to minimize cost while meeting nutrient thresholds and category requirements across a week.

## 📊🧮 Methods & Approach

## Data Sources

Nutrition: Emoji Diet Nutritional Data SR28 (Kaggle) with cleaned serving sizes suitable for children.

Prices: BLS Average Retail Food and Energy Prices to reflect realistic per-serving costs.

USDA Guidelines: Daily nutrient ranges for ages 9–12 used as constraints.

## Modeling

Decision Variables: Binary selection per food item per day (no repetition across days).

Objective: Minimize total weekly cost across trays.

## Constraints

Nutrition minimums per tray: calories, protein, fiber, vitamin A, vitamin C, calcium, iron.

Category coverage: exactly one item from each category (Beverage, Dessert, Fruit, Main, Meat, Snack, Vegetable). Vegetarian scenarios remove Meat and optimize a Vegetable substitute.

Budget: Weekly cap based on $30 per student for 5 trays across 75 students (total $2,250).

No repetition: An item used on a day cannot appear again that week.

## Implementation

Excel Solver: Rapid prototyping and scenario setup with category and nutrient matrices.

Python (Pyomo + CBC): Robust, scalable MILP with reusable data pipeline and “exclude used items” logic across trays.

## 💼 Business Relevance

Reduces per-tray costs while ensuring USDA compliance, enabling more students to receive nutritious meals.

Offers inclusive vegetarian plans with measurable savings.

Scales beyond schools to public health feeding programs, clinics, and disaster relief menu design.

## Contributors
Aishwarya Rauthan <br>
Gunjan Sharma<br>
Haaniya Umair<br>
Parita Patel<br>
