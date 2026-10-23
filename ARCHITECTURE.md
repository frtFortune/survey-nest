# System Architecture: SurveyNest

## 1. System Overview
SurveyNest is structured as a modern web application designed for high responsiveness, low-friction survey participation, and organized student research coordination.

## 2. High-Level Component Architecture
* **Frontend Layer**: Responsive web interface (HTML/CSS/JavaScript or modern framework) serving the student dashboard, survey submission forms, and public redirection pages.
* **Routing & Branded Links Engine**: Handles custom short URLs (`surveynest.app/f/xyz`) and dynamically routes users to external form endpoints while logging interaction metrics.
* **Backend Services**: Handles user authentication, demographic filters, database CRUD operations, and completion tracking.
* **Notification Worker (Daily Digest)**: A scheduled background job that aggregates active surveys matching user demographics and dispatches a single batched daily email summary.

## 3. Database Schema Concept
* **Users Table / Collection**:
  * `id` (Primary Key)
  * `email`
  * `password_hash`
  * `department`
  * `academic_level`
  * `created_at`
* **Surveys Table / Collection**:
  * `id` (Primary Key)
  * `creator_id` (Foreign Key)
  * `title`
  * `external_url`
  * `slug` (Unique string for `surveynest.app/f/slug`)
  * `target_department`
  * `target_level`
  * `expires_at`
  * `created_at`
* **Completions Table / Collection (Tracking)**:
  * `id` (Primary Key)
  * `user_id` (Foreign Key)
  * `survey_id` (Foreign Key)
  * `completed_at`