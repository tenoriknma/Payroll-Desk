Payroll Desk - redesign + privacy + local libraries (built on the "limited-user" version)

UPLOAD: put ALL files in this folder into the "public" folder of your GitHub repo (replace the old index.html and _headers).
  index.html          the app (new look, keyboard access for attendance, privacy links)
  _headers            security rules (updated: no outside scripts or fonts are allowed any more)
  privacy.html        employee privacy notice - EDIT the 3 yellow items before you rely on it
  supabase.js, 591.supabase.js, xlsx.full.min.js, jszip.min.js   libraries, now served from your own site
  *.woff2             fonts, now served from your own site

BEFORE GOING LIVE: open privacy.html in a text editor (or GitHub's pencil icon) and replace
  [name of data protection officer]   [email or phone]   [retention period ...]
with the real details. Have the company confirm the wording.

ROLLBACK: put back the index.html and _headers from PayrollDesk-Cloud-limited-user.zip.
  (The extra files can stay; the old index.html will simply not use them, but the old _headers
  must come back with it because the old page loads scripts from cdnjs/jsdelivr.)


Nov 17 (later): Settings > Payslip format has a tick box "Use the new payslip format". Unticked = old format (default). Ticked = new format with Salary Period beside Salary. Factor 312 (26 working days a month) added in Settings.

Nov 18: Payslip format tick box in Settings. Unticked = old green format (default), ticked = new black and white format. Factor 312 (26 working days a month) added.

SALARY ADJUSTMENT UPDATE: only index.html changed. Upload it to public/ in your repo, then hard refresh (Ctrl+Shift+R). The database table already exists.

GLASS UPDATE: only index.html changed. To undo the glass look, use index.html from the previous zip.

APPEARANCE UPDATE: only index.html changed. Settings > Appearance has Mode (Light/Dark) and Style (Classic, Glass v1, Glass v2). The sidebar Light/Dark button moved there.
