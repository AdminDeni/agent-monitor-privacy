# Privacy Policy — Agent Monitor

_Last updated: May 26, 2026_

This privacy policy describes how the **Agent Monitor** Chrome extension ("the Extension") handles data. The Extension is an internal team tool and is published as an **Unlisted** item on the Chrome Web Store.

## Who this policy applies to

This policy applies to anyone who installs and uses the Agent Monitor Chrome extension.

## What data the Extension reads

When you have the company monitoring portal (`https://webapps.otto-complus.de/*`) open in a browser tab, the Extension reads the **agents-overview table** from the rendered page. This includes:

- Agent usernames
- Agent display names
- Agent state (Available, Pause, Busy, etc.)
- Time in current state
- Campaign name
- Group and supervisor (from a separate reference list)

The Extension also fetches a CSV reference list (agent code, display name, group, supervisor) from a private GitHub repository when you provide a GitHub access token via the Extension's options page.

## Where the data is stored

**All data is stored locally on your device** using the browser's built-in `chrome.storage.local` API. Specifically:

- Most recent scan results
- Up to 72 hours of agent availability history
- Your GitHub access token (entered by you in the options page)
- Your preferences (refresh interval, theme)

**No data is transmitted to any server controlled by the Extension developer.** The Extension does not include any analytics, telemetry, or third-party tracking.

## What data is sent off-device

The Extension makes outbound network requests only to the following two destinations, and only for the stated purposes:

1. **`https://webapps.otto-complus.de/*`** — The monitoring portal. The Extension reads the rendered page in a tab you have open; it does not perform any login or background requests beyond what your active session is already doing.
2. **`https://api.github.com/repos/AdminDeni/Agent-Data/contents/agents.csv`** — GitHub API endpoint to download the agent reference list. Your GitHub access token is sent to GitHub in the `Authorization` header of this request.

The Extension does not send data to any other domain.

## Use of the GitHub access token

The token you enter in the Extension's options page is:

- Stored only in `chrome.storage.local` on your device
- Used solely to authenticate the request to fetch `agents.csv` from the private GitHub repository
- Never transmitted to any party other than GitHub
- Never bundled into the Extension's source code

You can clear the token at any time from the options page.

## Third-party services

The Extension communicates with two third parties:

- **The company monitoring portal** (operated by your employer / Otto-Complus). Your interaction with the portal is governed by the portal's own terms and privacy policies.
- **GitHub, Inc.** Requests made by the Extension to the GitHub API are governed by [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## Data we do not collect

The Extension does **not** collect, store, or transmit:

- Your browsing history
- Your location
- Your keystrokes, clicks, or mouse movements
- Health information
- Financial or payment information
- Personal communications

## Data retention and deletion

- Scan history is kept locally for **72 hours** and then automatically pruned.
- All other locally stored data persists until you clear it from the options page or uninstall the Extension.
- **Uninstalling the Extension removes all locally stored data**, including your access token, scan history, and preferences.

## Children's privacy

The Extension is intended for internal business use by adult employees only. It is not directed at children under 13.

## Changes to this policy

If this policy changes, the updated version will be published at the same URL. The "Last updated" date at the top will be revised.

## Contact

For questions about this privacy policy or the Extension, contact the team administrator who provided you with the access token.
