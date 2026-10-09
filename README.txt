BodyLog Light v1.3
==================
1. On Windows: unzip, open index.html in Chrome or Edge. Record today's weight, workout and mood, then Save to view the report.
2. iPhone PWA: upload the folder to HTTPS static hosting. Open its HTTPS address in Safari -> Share -> Add to Home Screen.
3. Local storage: browser localStorage on each device, NOT a cloud account. Backup frequently from Settings -> Export JSON.
4. Old v1.0/v1.1 data: export JSON from old version; import JSON under Settings in this version. If opening in the same browser and origin, the old bodylog-v1 storage key may be read automatically.
5. Historic CSV: on Windows run `python import_csv.py history.csv`. Header: date,weight,workout,note (last two optional). Then import BodyLog-import.json from Settings. Import REPLACES all existing data; export backup first.
6. Report card fits the phone viewport without vertical scrolling; long workout and mood text is summarized visually but fully retained in data. Report PNG can be downloaded.
7. The report compares ONLY to the preceding calendar day's weight. If missing, it shows a dash.
8. iOS data is not automatically shared with Windows. No cloud sync. Avoid clearing website data and keep backups.
9. For safety, the HTML can be opened locally for Windows testing, but PWA installation and offline caching require HTTPS hosting.

Version 1.3: removed random quote from report; compacted daily change area; added a configurable historical-low comparison start date in Settings. Celebration appears only if the selected day is strictly lower than all earlier entries on/after that start date. Existing local data storage key is preserved for continuity on the same origin.

Version 1.4: Fixed proportional report layout. Workout and mood sections retain positions regardless of text length. Long text is truncated in card; full notes remain stored.
