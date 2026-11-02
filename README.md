# Purdue Dining Watch

Pulls daily menus from the Purdue Dining API, checks them against each person's dietary restrictions and preferences, and notifies the group (via ntfy or email) who can eat what and where.

## MVP
- Fetch and parse daily menus
- Web UI for entering preferences
- Load preferences form JSON file
- Score locations per person and meal
- Send results via ntfy and email

## Tech stack
- **Python 3**: all logic, organized into classes (`DiningClient`, `Ranker`, `Notifier`)
- **Purdue Dining API** (`api.hfs.purdue.edu/menus/v2`): public, keyless source for menus, allergens, and locations
- **requests**: HTTP calls to the API and ntfy
- **ntfy**: push notifications to a shared topic
- **smtplib / Gmail SMTP**: email delivery using a Gmail app password
- **cron**: runs the bot once a day on the server PC
- **Git**: version control

## Future plans
- Deploy to server PC with daily cron job
- Testing and polish
- Login system for Web UI
- Support for multiple groups