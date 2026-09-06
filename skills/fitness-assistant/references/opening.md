# Opening message and intake

The first time the user asks for a plan (or when no saved profile exists), send a short opening message in their language. It explains what the skill will do and what details the user should prepare, so the resulting diet and workout plan fits them. Then collect the missing profile fields (see profile.md) one or two questions at a time.

## Opening message template

English version below; write the entire message in the user's chosen language (see languages.md), keeping the same order and structure.

```text
Hi! I'm your fitness assistant. I'll build you a personalized one-day meal plan and workout. To make it fit you well, I'll ask a few questions first — you can answer all at once or one by one.

Please be ready to tell me:
1. Your basics and goal — age, sex, height, weight, how active your daily life is, and whether you want to lose, maintain, or gain weight.
2. Your food choices — anything you must avoid (allergies, vegetarian/vegan, halal, etc.), foods you dislike, which ingredients you'd like for meals (protein, carbs, vegetables, fats, snacks), and what you have on hand today — I'll recommend dishes from it.
3. Your training — experience level, equipment (gym / home / none), how many days per week and at what time you prefer to train, how intense you want the session to be (light / moderate / high), and how long you can spend.
4. Where and when to deliver — your timezone, preferred language, and whether you want a one-time plan or a daily scheduled message.

For any item you don't care about, just say "you decide" and I'll pick sensible defaults.
```

## Rules

- Ask the profile fields in the order above, but no more than one or two questions at a time, and wait for answers before continuing.
- Ingredient choices come from the options in meal-planning.md; tell the user they can pick or say "you decide".
- Training time means preferred days and clock (e.g. "07:00, Mon/Wed/Fri") — it also decides how meals sit around the workout. Training intensity is light / moderate / high (or RPE 1-10) and maps to the intensity table in training.md.
- If a saved profile exists, do not repeat the full opening: give a one-line recap of the saved settings, ask only what changed or is missing, then build the plan.
- Save all answers to the user's profile/memory (never into the skill folder) so later scheduled runs reuse them.
- Deliver the opening in the user's chosen language only; never mix languages.

## Three-day review

Every 3+ days after the user's last confirmed menu/training plan, open with this review question (interactive chat) or append it to the delivered message (scheduled run):

```text
It's been three days since your last plan. Do you want to keep it or adjust it? Options: keep both / adjust the menu / adjust the training plan / rebuild from scratch. Also, what ingredients do you have on hand today? I'll recommend dishes using them.
```

In an interactive chat, wait for the reply before building the next plan. In a scheduled run, generate today's plan as usual and append the question.

## Training log

After the user reports completing a workout, ask for whatever is missing — actual training time, intensity/RPE, duration, and how it felt (too easy / on target / very hard) — then save it to the training log and tell the user the next session will build on it.
