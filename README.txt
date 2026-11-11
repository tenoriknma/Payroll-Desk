PAYROLL DESK (sign-in + database version)

FILES
  index.html   the whole app
  _headers     security settings for Cloudflare (keep it next to index.html)

UPLOAD TO CLOUDFLARE PAGES
  1. Sign in at dash.cloudflare.com. Go to Workers & Pages > Create > Pages > Upload assets.
  2. Name the project (for example payroll-desk) and press Create project.
  3. Drag the FOLDER "PayrollDesk-Cloud" (both files inside) into the upload box. Press Deploy.
  4. Open the address Cloudflare shows (payroll-desk.pages.dev).
  To update later: open the project > Create deployment > upload the folder again.

PROTECT THE ADDRESS (recommended)
  Cloudflare Zero Trust > Access > Applications > add your pages.dev address, allow only your email.
  This adds a second lock in front of the app's own sign-in.

SUPABASE SETTING TO CHECK
  Supabase > Authentication > URL Configuration: set Site URL to your pages.dev address.

FIRST SIGN-IN
  Use the email and password of your Supabase user. The app asks you to scan a QR code with an authenticator app
  the first time, then asks for the 6 digit code at every sign-in. It signs you out after 30 minutes of no activity.

DATA
  Everything is saved to Supabase as you work. "Saved" at the top means the database has the change.
  If it says "Not saved", do not close the page. It retries by itself. Use Backup in Settings regularly.
