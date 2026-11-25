WEDDING GATE SCANNER - SETUP (about 10 minutes, free)

PART 1 - Backend (remembers which QR codes were used)
1. sheets.google.com -> create a new blank Google Sheet.
2. Extensions > Apps Script. Delete everything, paste backend/Code.gs.
3. Change PASSCODE (staff) and SUPERVISOR (override code) to your own secrets. Keep GSEC as is. Save.
4. Deploy > New deployment > Web app. Execute as: Me. Who has access: Anyone. Deploy, allow permissions.
5. Copy the Web app URL (ends with /exec).
   Later code changes: Deploy > Manage deployments > edit > New version (keeps the same URL).

PART 2 - Website
1. Log in to app.netlify.com, then go to app.netlify.com/drop and drag index.html onto the page.
2. Open the link on the gate phones. First time: paste the Web app URL and the staff passcode (⚙).
3. Type the EVENT CODE of the wedding (the 6-letter code shown when you generated the customer's link) and the staff name.
4. Allow camera access. Green = valid (first time). Red = NOT AVAILABLE (already used). Wrong event / forged QRs are rejected.

OFFLINE: if the internet drops, the phone keeps scanning from its last synced list and sends the scans later.
Open the scanner online once before the event so the list and security key are downloaded.
Supervisor override: after a red result tap "Supervisor override" and enter the SUPERVISOR code.
The Google Sheet "Scans" lists every check-in (event, number, time, staff, offline).

REUSING THE SCANNER FOR EVERY CUSTOMER
- Use the same scanner link for all customers. Type each wedding's Event code at the top.
- When an event is finished: open "History & Reset", type the event name, retype the event code, enter the SUPERVISOR code and confirm twice.
  The check-in list is saved to the "History" sheet (and in the app's history list) and cleared from the live list.
- Past events: open "Past events" to see each archive, view every check-in and download it as CSV.
