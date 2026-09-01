# Privacy Statement — Candidate URL Checker

_Last updated: 2026-08-27._

## What the extension does

Candidate URL Checker checks a candidate profile URL that **you copy and submit yourself** against a Google Sheet that **you configure and own**, and can append new URLs to that sheet at your request.

## What it does NOT do

- It does not read, scrape, modify, or automate LinkedIn in any way. It requests no LinkedIn permissions, injects no scripts, and never accesses LinkedIn pages, cookies, or network traffic.
- It does not monitor your clipboard. The clipboard is read once, only when you click **Check copied URL**.
- It does not monitor browsing history or open tabs.
- It has no backend server, no analytics, and no telemetry. No data is sent to anyone except Google's Sheets API, under your own Google account.

## Data handling

| Data | Where it lives | Retention |
| --- | --- | --- |
| Spreadsheet configuration & preferences | `chrome.storage.local` on your device | Until you reset it |
| Recent activity (canonical URL, result, row, timestamp; max 20) | `chrome.storage.local` on your device | Until you clear it |
| Cached URL column | `chrome.storage.local` on your device | ~5 minutes (configurable) |
| Candidate rows you add | Your private Google Sheet | Controlled by you |
| Google OAuth tokens | Managed entirely by Chrome (`chrome.identity`) | Never stored by the extension |

Clipboard content that is not a supported candidate URL is discarded immediately after validation.

## Google access

The extension uses the `https://www.googleapis.com/auth/spreadsheets` OAuth scope. This grants it read/write access to spreadsheets accessible to the signed-in Google account. It only ever reads and appends to the single spreadsheet you configure, but you should understand the scope's breadth before consenting. You can revoke access at any time via the extension's **Disconnect Google** button or at [myaccount.google.com/permissions](https://myaccount.google.com/permissions).

## Your controls

- **Disconnect Google** — revokes the extension's cached access.
- **Clear recent activity** — deletes the local activity log.
- **Reset all local data** — one click clears all configuration, activity, and cache.
