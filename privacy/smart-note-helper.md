# Smart Note Helper — Privacy Policy

**Last updated:** 2026-10-22

Smart Note Helper ("the extension") is a Manifest V3 Chrome extension for taking
notes from web pages and turning a page into a structured summary with a large
language model (LLM) that **you** configure (bring your own API key).

## The short version

- The developer runs **no server**. The extension has no analytics, no telemetry,
  no ads and no third-party tracking scripts. The developer never receives your
  notes, page content, API key or GitHub token.
- Page content leaves your browser **only** when you click "Summarize this page",
  and it goes **only** to the AI endpoint you entered in Settings.
- Cloud sync is **off by default**. If you turn it on, summaries go **only** to a
  secret Gist in your own GitHub account.

## What data is processed, and where it goes

| Data | When | Sent to |
|---|---|---|
| Title, URL and visible text (first 12,000 characters) of the current tab | Only when you click "Summarize this page" in the extension popup | The AI endpoint you configured (for example an OpenAI-compatible or Anthropic-compatible API, or your own proxy), together with your API key. That provider's own privacy policy applies to what it receives. |
| Generated summaries | Only when you enable cloud sync, authorize GitHub, and click "Sync to cloud" | `api.github.com`, into one **secret** Gist (`summaries.md`) owned by your GitHub account. |
| GitHub sign-in (OAuth Device Flow) | Only when you click "Authorize" | `github.com`. The extension receives an access token limited to the `gist` scope. |

The extension does not read other tabs, does not inject scripts into pages
automatically, and does not read pages in the background. Text you select and
add to a note through the context menu stays on your device.

## What is stored locally (in your browser only)

| Storage | What it holds |
|---|---|
| `chrome.storage.local` | Notes, settings, AI configuration (endpoint, model, **API key**), GitHub sync settings and **access token**, daily usage counter for the free tier, Pro unlock status. |
| IndexedDB (`my-note-extension`) | Summary history and tasks/reminders. |

The API key and GitHub token are stored in plain text in Chrome's extension
storage on your device (Chrome offers extensions no OS keychain). They are never
sent anywhere except to the AI endpoint and GitHub respectively, and are masked
in any error message shown on screen. Uninstalling the extension deletes all of
this data. You can also delete individual history items, tasks and notes inside
the extension, and revoke the GitHub authorization at
<https://github.com/settings/applications>.

## Permissions and why they are needed

| Permission | Purpose |
|---|---|
| `contextMenus` | "Add to note" on selected text. |
| `storage` | Save notes and settings locally. |
| `downloads` | Export notes as a TXT file you choose to save. |
| `notifications`, `alarms` | Remind you when a task is due. |
| `activeTab`, `scripting` | Read the current tab's text **only** after you ask for a summary. |
| Optional host access | Requested at runtime, one site at a time: the host of the AI endpoint **you** enter (needed because it can be any provider or self-hosted proxy), and `github.com` / `api.github.com` only if you turn on cloud sync. Nothing is requested at install time. |

## Data sharing and sale

The developer does not sell, rent or share user data, does not use it for
advertising or credit decisions, and does not use it for any purpose unrelated to
the extension's single purpose of note-taking and page summarization.

## Children

The extension is not directed at children under 13.

## Changes

If this policy changes, the "Last updated" date above will change and the new
version will be published at the same address.

## Contact

Questions: open an issue on the extension's support page in the Chrome Web Store.
