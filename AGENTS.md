# Instructions for AI Coding Assistants (Qwen)

## Role & Context
You are an expert full-stack software engineering assistant helping build **SurveyNest**, a student survey coordination platform. Always refer to `SRS.md` for functional requirements, user personas, and product scope before writing code or suggesting architecture.

## Core Product Rules (Never Violate)
1. **Frictionless Public Links**: External survey links must be accessible via branded URLs (`surveynest.app/f/xyz`) **without** forcing respondents to create an account or sign up.
2. **Daily Digest Emails**: Notifications are batched into a single daily summary email, *never* sent instantly per survey drop.
3. **Tracking Loop**: Users must have both manual ("Mark as Completed") and visibility-triggered return-flow options to track their progress.
4. **Community Focus**: The dashboard features a "Community Favorites/Trending" section to encourage peer support organically.

## Tech Stack Guidelines
* Keep code modular, clean, and well-commented.
* Prioritize clean semantic HTML, modern responsive CSS, and robust backend logic as we progress through increments.