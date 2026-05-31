# Iron Log

**Iron Log** is a lightweight gym tracking Progressive Web App built for fast workout logging on iPhone and mobile browsers. It helps you track sets, reps, weights, exercise history, rest times, and workout structure without requiring an account or backend.

The app runs as a single-page web app and stores data locally on the device.

## Features

- **Workout day templates**
  - Push Day, Pull Day, Leg Day, Whole Body, Chest, Arms, Shoulders, and Back
  - Add, edit, or delete custom training days

- **Exercise library**
  - Preloaded exercise list with photos
  - Exercises grouped by muscle group
  - Add, edit, delete, and customize exercises
  - Exercise types: Basic Exercise and Complement Exercise

- **Smart workout suggestions**
  - Suggests complement exercises after basic exercises for large muscle groups
  - Shows a non-blocking volume notice when enough training volume is reached

- **Workout logging**
  - Track weight and reps for each set
  - View previous logs for the selected exercise
  - Resume and edit previous training days from history

- **Rest timer**
  - Separate timers for rest between sets and rest between exercises
  - Configurable timer durations

- **Backup and restore**
  - Export all training data as a JSON backup
  - Restore from backup file or pasted JSON
  - Includes exercises, logs, photos, training days, timer settings, group photos, and language

- **Localization**
  - English and German app language
  - Default exercise names and muscle groups are localized
  - Image file paths remain stable and are not renamed

- **PWA support**
  - Installable on iPhone via Safari
  - Includes manifest, icons, and service worker
  - Optimized for iPhone safe areas and Dynamic Island spacing

## Screens And Data

Iron Log includes:

- Start screen
- Training day selector
- Exercise picker grouped by muscle
- Set logging view
- Exercise and session history
- Exercise management
- Settings with timer, language, backup, and restore

All user data is stored in the browser's `localStorage`. There is no server, login, cloud sync, or analytics.

## Project Structure

```text
.
├── index.html          # Main single-page app
├── manifest.json       # PWA manifest
├── sw.js               # Service worker
├── icon.png            # App icon
├── icon-192.png        # PWA icon
└── images/
    └── exercises/      # Exercise photos
```

## Running Locally

Because the app is a static web app, you can open `index.html` directly in a browser.

For a more realistic PWA/service-worker test, serve the folder with a local web server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deploying With GitHub Pages

1. Create a GitHub repository.
2. Upload or push the project files.
3. Go to repository **Settings**.
4. Open **Pages**.
5. Set source to the `main` branch and `/ (root)`.
6. Save.

Your app will be available at:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY
```

## Installing On iPhone

1. Open the GitHub Pages URL in **Safari**.
2. Tap the share button.
3. Choose **Add to Home Screen**.
4. Launch Iron Log from the home screen.

## Backup Strategy

Iron Log is local-first, so backups are important.

Use:

```text
Settings -> Export Backup
```

This downloads a `.json` file containing the app data. Store it in iCloud Drive, Files, or another safe place.

To restore:

```text
Settings -> Restore from File
```

or paste the JSON into:

```text
Settings -> Restore from Paste
```

## Privacy

Iron Log does not send your workout data anywhere.

- No account required
- No backend
- No analytics
- No cloud sync
- Data stays on the device unless you export it manually

## Development Notes

- The app is intentionally implemented in a single `index.html` file.
- Default exercise image filenames may be German, but the visible app labels can be English or German.
- Keep image paths stable when renaming visible exercise labels.
- Backups should be exported before clearing app data or replacing a device.

## License

Personal project. Add a license file if you plan to publish, share, or accept contributions.
