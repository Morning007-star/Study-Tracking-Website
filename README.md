# Rey's Academic Command Centre

A dependency-free, local-first study tracker that runs in Chrome on Windows. It does not need a login, internet access, server, or install step.

## Run it

1. Extract the delivered project folder if it came as a ZIP.
2. Open `index.html` in Google Chrome (double-click it, or right-click and choose **Open with → Google Chrome**).
3. Bookmark the page for quick access.

The app saves changes in Chrome's local browser storage on this PC. Keep the folder in a stable location. Clearing Chrome site data or using a different Chrome profile can remove or hide the saved records.

## Included

- Seven editable courses, credit values, topic completion and 1–5 confidence ratings.
- Daily reflection check-ins, editable assignment/reminder tasks, due dates and overdue indicators.
- 25-minute focus timer and study log.
- Short practice quizzes and five-minute timed tests, with scores and answer explanations.
- Course weakness cues, weekly study summary, CGPA and semester target indicators.
- JSON backup export and restore.

Course codes follow the provided timetable mappings. COMP353 is provisionally shown as “Data Analysis / Algorithms”; confirm its official title. COMP351 remains unidentified. No C# course is included. GPA figures are planning indicators; edit the grading scale and goals to match your institution.

## Privacy and backup

Study records stay in local storage in the Chrome profile where you use the app. There is no account, analytics, remote database, or network request. Anyone with access to your Windows profile and Chrome profile may be able to use that browser profile. Use **Backup** regularly to download a JSON copy, and store it somewhere safe. **Restore** replaces the currently saved browser data with the selected backup.

## Optional hosting

The project is ready for GitHub Pages deployment from the repository root. The included `.github/workflows/pages.yml` publishes the static site whenever you push to `main` (or run it manually).

1. Put `index.html`, this README, `.nojekyll`, and `.github/workflows/pages.yml` at the root of your repository.
2. On GitHub, open **Settings → Pages** and set the build and deployment source to **GitHub Actions**.
3. Push the files to the repository's `main` branch. Open the Pages URL shown in the workflow run or repository Pages settings.

For an existing repository with a different default branch, change `main` in `pages.yml` to that branch. For a private repository, GitHub Pages availability depends on the repository owner's plan and policy. Do not commit exported JSON backups. The source contains the app name and course setup; choose a private repository if you do not want that code publicly visible.

Hosting the app does not upload or synchronize study records. Records are saved separately in local browser storage for each browser profile and site origin. The existing `file://` Chrome copy and hosted HTTPS copy are separate storage locations; export a backup from the old copy and restore it in the hosted copy if you want to carry records over. No custom domain is configured.
