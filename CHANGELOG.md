# Changelog

## 2026-09-13

- Added: three-day check-in asking whether to keep or adjust the diet menu and training plan.
- Added: meal planning can recommend dishes from the ingredients the user has on hand today.
- Added: completed training time and intensity are logged and used to prepare the next workout.
- Added: fixed 8-language versions of the opening message, three-day review, and training-log dialogues; replies now use the block matching the user's language verbatim.
- Added: dish recommendations now follow the regional cuisine style associated with the user's chosen language.
- Added: daily ingredient cost budget — intake asks for a food budget and currency, and plans show the estimated cost of what still has to be bought.
- Added: when the estimate is over budget, cheaper swaps are offered that keep calories and protein the same.
- Changed: skill references point to the fixed dialogue file instead of on-the-fly translation.
- Changed: changelog entries no longer carry version numbers.

## 0.1.3 (2026-09-05)

- Added: guided opening message that introduces the assistant and tells the user which details to prepare before the first plan.
- Added: profile intake now collects ingredient choices, preferred training time, and training intensity.
- Added: workout guidance defines light / moderate / high intensity and how sessions should be adjusted.

## 0.1.2 (2026-08-31)

- Added: customizable ingredient choices in meal planning — pick your own protein, carbs, vegetables, fats, and snacks to build a personal daily menu.
- Added: chosen ingredients are saved as preferences and reused by scheduled daily runs.
- Fixed: corrected the plan calculator example command in the skill docs.

## 0.1.1

- Fixed: added explicit version metadata for ClawHub publishing.

## 0.1.0

- Initial release: personalized daily diet and workout plans, 8 supported languages, scheduled daily delivery with IANA timezone.
