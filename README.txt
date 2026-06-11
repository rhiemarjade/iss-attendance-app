Offline Attendance PWA v7 restore and print fix

This package fixes backup restore so attendance records are restored into IndexedDB, not only students and rosters. It also makes the print preview close automatically after printing or saving as PDF when the browser supports afterprint, with a Close Print Preview fallback button.

Offline Attendance PWA v5, Print Reports and Teacher Guide

Contents:
- index.html
- manifest.json
- service-worker.js
- icons/icon-192.png
- icons/icon-512.png
- icons/maskable-512.png
- icons/apple-touch-icon.png

What is new in v5:
1. Print Report button added to the Reports tab.
2. Print layout opens a clean report page that can be printed or saved as PDF.
3. Printed reports include title, grade level, section, subject, month/date range, summary counts, date printed, app version, and prepared by line.
4. Database tab now shows app version, database mode, last backup, and latest attendance record.
5. Teacher Quick Guide added inside the Database tab.
6. Service worker cache version updated so tablets can detect the new app version.

GitHub Pages upload steps:
1. Extract this package.
2. Upload all extracted files to the root of your GitHub repository.
3. Make sure index.html, manifest.json, service-worker.js, README.txt, and the icons folder are all at the repository root.
4. Commit the changes.
5. Open the GitHub Pages link while online.
6. Tap Refresh App if the update banner appears.
7. Test CSV import, attendance saving, report export, print report, backup, and restore.

Tablet reminder:
This app stores attendance records locally on the device using IndexedDB. Clearing website data in Safari or Chrome can delete the local database. Use Backup Now regularly and keep the JSON backup in a safe location.


Version 7 note: Print Report now prints summary columns only. Full date-by-date records remain available through Export CSV.


Version v8 late enrollment patch:
- Add Roster Entry now includes Enrollment Date.
- Dates before a learner's enrollment date show Not Yet Enrolled.
- Roster CSV import/export supports optional Enrollment Date column.


Version note: v9 filter refresh fix ensures Daily Record names reload correctly whenever Date, Grade, Section, or Subject changes, including locked saved records.
