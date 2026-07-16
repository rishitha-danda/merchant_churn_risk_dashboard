# AI Assessment Transcript Prompt Guide

## Prompt 1
I'm working on an AI proficiency assessment.

The task is to build a dashboard that identifies merchants who are at risk of churning and recommends the next best action.

I want to build this using React, Vite and Tailwind CSS.

Before writing any code, help me understand the problem, identify the missing requirements, and create a simple V1 specification document with reasonable assumptions.

---

## Prompt 2
Now help me design the merchant data model.

Since no dataset is provided, suggest realistic fields that would be available in a payment or e-commerce platform.

Explain why each field is useful for detecting churn.

---

## Prompt 3
Let's design the churn detection logic.

Since there is no historical data, I don't want to use machine learning.

Help me create a simple weighted scoring system that calculates a churn score from 0 to 100.

---

## Correction Prompt 1
I think some of these weights feel arbitrary.

Can you explain why each weight was chosen?

If two signals are overlapping, like revenue decline and order decline, should they both have the same influence?

Please refine the scoring logic.

---

## Prompt 4
Generate 15 realistic merchants.

Make sure the values are realistic and include Low, Medium and High risk merchants.

Return them as a JavaScript array.

---

## Correction Prompt 2
Looking at the sample data, some merchants don't seem to match the risk level I would expect.

Please calculate the churn score for each merchant and verify that the generated data actually produces a good distribution of Low, Medium and High risk merchants.

Adjust any unrealistic records.

---

## Prompt 5
Let's start building the React application.

Suggest a clean folder structure for a React + Vite + Tailwind CSS project.

Explain the responsibility of each component.

---

## Prompt 6
Generate the commands to create the project and install all required dependencies.

After that we'll build the UI step by step.

---

## Prompt 7
Build the dashboard layout with:

- Summary cards
- Search
- Filter
- Merchant table

Use React and Tailwind CSS.

---

## Prompt 8
Now implement the reusable utility functions:

- calculateChurnScore()
- getRiskLevel()
- getRecommendation()

---

## Correction Prompt 3
I noticed getRecommendation() is mostly based on the final score.

I think recommendations should explain WHY the merchant is risky instead of only using the overall score.

Can you redesign it so recommendations are generated from the specific risk signals?

---

## Prompt 9
Build the Summary Cards component.

Display:
- Total merchants
- High Risk
- Medium Risk
- Low Risk

---

## Prompt 10
Build the Merchant Table component.

Display:
- Merchant Name
- Industry
- Score
- Risk
- Recommendation

---

## Prompt 11
Create a reusable Risk Badge component with appropriate colors.

---

## Prompt 12
Add search functionality so merchants can be searched by name.

---

## Prompt 13
Add filtering by risk level.

---

## Prompt 14
Add sorting by churn score and merchant name.

---

## Correction Prompt 4
The UI works, but I think the most important information should be easier to notice.

Can you suggest small UX improvements so that high-risk merchants stand out more without making the interface cluttered?

---

## Prompt 15
Let's improve the dashboard.

Add:
- Progress bar
- Better spacing
- Responsive layout

---

## Correction Prompt 5
Let's review the business logic before finishing.

Can you think of any edge cases where this scoring system could incorrectly classify a merchant?

If yes, suggest improvements and explain why.

---

## Prompt 16
Before I consider the business logic complete, I want to test cases that may not behave normally.

Please check how the system handles:

- A brand-new merchant with very little history
- A merchant with zero transactions in the previous period
- A merchant who is inactive but has historically high revenue
- A merchant with multiple risk signals at the same time

For each scenario:
- Explain the expected churn score and risk classification.
- Identify whether the current scoring logic behaves reasonably.
- If not, suggest improvements while keeping the scoring system simple, transparent, and explainable.

---

## Prompt 17
Generate test cases to verify:
- Churn score calculation
- Risk classification
- Recommendations
- Search
- Filter
- Sorting

---

## Prompt 18
Review the complete project like a senior engineer.

Look for issues in:
- React code
- Component structure
- Business logic
- Maintainability
- User experience

Suggest improvements before deployment.

---

## Prompt 19
Help me deploy this React + Vite application to GitHub Pages.

List every required step.
