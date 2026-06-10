Offline Attendance PWA v4, IndexedDB Database Version

Files included:

index.html
manifest.json
service-worker.js
icons/icon-192.png
icons/icon-512.png
icons/maskable-512.png
icons/apple-touch-icon.png

Main changes in this version:

1. The tablet local database now uses IndexedDB as the main storage engine.
2. Existing localStorage data from the previous PWA version is migrated automatically on first load.
3. The app keeps the same LRN-based attendance logic:
   Date + Grade Level + Section + Subject + LRN.
4. The Database tab now shows the last backup date clearly.
5. A weekly backup reminder appears when records exist and the backup is old or missing.
6. A backup warning appears when records exist but are not fully backed up.
7. Backup Now exports the full local database in one tap.
8. Restore Database checks and verifies the restored data before confirming success.
9. Monthly CSV reports still include the Month row after Subject.

GitHub Pages update guide:

1. Extract this package.
2. Replace the files in your GitHub repository with the extracted contents.
3. Make sure index.html, manifest.json, service-worker.js, README.txt, and the icons folder are at the repository root.
4. Commit the changes.
5. Open the GitHub Pages link online.
6. If the installed app shows an update banner, tap Refresh App.
7. If the old version still appears, remove the Home Screen app, reopen the GitHub Pages link, then add it to Home Screen again.

Important backup reminder:

The app stores records on the tablet device. IndexedDB is safer and more structured than localStorage, but clearing browser website data can still delete the local database. Use Backup Now regularly and before clearing browser data, changing devices, or updating the app.

Recommended teacher routine:

Use Backup Now every Friday.
Save the backup file to Files, Google Drive, USB, or a computer folder.
Use Restore Database when moving records to another device.

Current CSV roster format:

LRN,Complete Name,Gender,Grade Level,Section,Subject
