Offline Attendance PWA

Files included:

index.html
manifest.json
service-worker.js
icons/icon-192.png
icons/icon-512.png
icons/maskable-512.png
icons/apple-touch-icon.png

GitHub Pages upload guide:

1. Create a new GitHub repository.
2. Upload all files and the icons folder to the repository root.
3. In the repository settings, enable GitHub Pages for the main branch root folder.
4. Open the GitHub Pages link on the iPad or Android tablet.
5. On iPad Safari, use Share, then Add to Home Screen.
6. On Android Chrome, use Install App or Add to Home Screen.
7. Open the installed app once while online so the service worker can cache the app shell.
8. Test airplane mode after the first successful load.

Important reminders:

- Attendance records are stored on the device browser storage.
- GitHub Pages hosts the app files, not the attendance database.
- Use Backup Database JSON regularly.
- Use Restore Database JSON when moving data to another device or browser.
- When uploading a new app version, change CACHE_NAME inside service-worker.js so tablets receive the update.

Current CSV format:

LRN,Complete Name,Gender,Grade Level,Section,Subject

Current attendance key logic:

Date + Grade Level + Section + Subject + LRN
