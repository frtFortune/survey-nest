# Software Requirements Specification (SRS): SurveyNest

## 1. Introduction
* **Purpose**: To centralize academic research surveys across departments and academic levels, eliminating group chat clutter and tracking completion states.
* **Core Philosophy**: Frictionless response collection for respondents combined with robust tracking, community collaboration, and organic growth through branded links.

## 2. Key Features & Functional Requirements
* **User Accounts & Profiles**: Users can register and log in, specifying their department and academic level.
* **Survey Submission**: Authenticated users can submit external survey links (Google/Microsoft Forms) with target demographic filters (department/level) and expiry dates.
* **Branded Public Links**: Each submission generates a clean, branded public URL (`surveynest.app/f/xyz`) that allows anyone to view/fill the form *without* forcing them to create an account.
* **Personalized Dashboard & Feed**: 
  * Filtered feed of active surveys matching the user's target criteria.
  * **Trending / Community Favorites Section**: Highlights surveys that are nearing completion or heavily active, encouraging community support without feeling forceful.
* **Return Flow & Manual Tracking**: 
  * "Mark as Completed" toggle available on every survey card.
  * Browser visibility triggers ("Welcome back" prompt) to gently encourage users to check off surveys after returning from external form tabs.
* **Creator Analytics**: Form submitters can view real-time completion counts from platform users.
* **Daily Digest Email Notifications**: Instead of spamming users every time a form drops, the system aggregates available matching surveys and sends a **single daily digest email summary** to targeted users.
* **User Feedback System**: A dedicated feedback channel or form allowing users to submit suggestions, bug reports, or comments directly to the platform creator.
* **Safety & Integrity**: Automated duplicate URL checks and basic content reporting/moderation.

## 3. Non-Functional Requirements
* **Usability & Responsiveness**: Fully responsive layout optimized for mobile phones and desktop browsers.
* **Performance**: Fast-loading dashboard and lightweight public survey redirection pages.
* **Security**: Secure password hashing and protection against unauthorized data access.