# Candidate URL Checker

Candidate URL Checker is a Chrome side-panel extension for recruiters. It checks a candidate profile URL that you copy and submit yourself against a private Google Sheet that you configure and own, and can append new URLs to that sheet at your request.

## Key points

- **You are in control** — the extension only acts when you click **Check copied URL**. It never monitors your clipboard, browsing, or tabs.
- **Your data stays yours** — configuration and recent activity live only in your browser's local storage; candidate rows live in your own private Google Sheet.
- **No backend, no tracking** — there is no server, no analytics, and no telemetry. The only network calls are to Google's Sheets API under your own Google account.
- **No LinkedIn access** — the extension requests no LinkedIn permissions and never reads, scrapes, or automates LinkedIn.

## Google account access

The extension uses Google OAuth (via `chrome.identity`) with the `https://www.googleapis.com/auth/spreadsheets` scope so it can read from and append to the single spreadsheet you configure. You can revoke access at any time from the extension's **Disconnect Google** button or at [myaccount.google.com/permissions](https://myaccount.google.com/permissions).

## Privacy

See the full [Privacy Policy](privacy).

## Support

Questions or issues? Open an issue on the [GitHub repository](https://github.com/altmajorjohn/candidate-url-checker) or contact the support email listed on the Chrome Web Store listing.
