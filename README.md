# Fitness Assistant (OpenClaw skill)

A personal fitness assistant skill for OpenClaw. It plans a daily diet and workout from the user's age and health profile, and can publish the plan on a schedule (cron + IANA timezone) in one of 8 supported languages.

## Structure

```text
skills/fitness-assistant/
|-- SKILL.md
|-- references/    profile, meal planning, training, languages, scheduling
`-- scripts/       plan.py (BMI/BMR/TDEE/calorie/macro calculator)
```

## Install

```bash
openclaw skills install fitness-assistant
```

Or copy the `skills/fitness-assistant` folder into your OpenClaw workspace `skills/` directory.

## License

Published via ClawHub under MIT-0.
