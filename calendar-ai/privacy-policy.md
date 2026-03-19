# Privacy Policy for Calendar AI

**Last updated: March 19, 2026**

Calendar AI ("the Extension") is a Chrome browser extension that helps you quickly add events to Google Calendar using natural language or screenshots. This Privacy Policy explains what data we access, how it's handled, and your choices.

## Data We Access

### Google Account & Calendar Data
- **Basic profile info**: name, email, profile picture, and account ID — used for sign-in and displaying your account in the extension.
- **Google Calendar data**: your calendar list and upcoming events — used to create, update, or delete events on your behalf, and to detect which existing event you may be referring to when editing.

### User-Provided Content
- **Text input**: anything you type, paste, or select via right-click to create calendar events.
- **Images/screenshots**: any images you paste or upload for AI-powered event extraction.
- **Clipboard content**: when you open the extension, it may read your clipboard to auto-detect calendar-related content. You can dismiss this, and dismissal preferences are saved locally.

### Locally Stored Preferences
- Your selected default calendar
- Frequent contacts (names and emails you save for quick attendee suggestions)
- Your chosen AI provider (Free mode, OpenAI, Gemini, or Claude)
- Your API key if you choose to use your own (stored locally in your browser, not on our servers)

## How Data Is Processed

### AI Processing
When you submit text or an image, the following may be sent to the AI provider for event parsing:
- Your input text or image
- Current date, time, and timezone
- Titles and dates of your upcoming events (for edit/delete detection)
- Your saved frequent contacts (for attendee matching)

**AI Providers:**
- **Free mode**: Requests go through our Cloudflare Worker proxy (`calendar-ai-proxy.calendarai.workers.dev`) before reaching the AI provider.
- **Custom API key mode**: Requests go directly from your browser to your chosen provider (OpenAI, Google Gemini, or Anthropic Claude).

### What We Don't Store
- We do not persistently store your text inputs, images, or calendar event content on any server.
- We do not have a database or long-term storage backend.
- The Cloudflare Worker proxy processes requests in real-time but does not retain your data after the request completes.

### Rate Limiting
In free mode, we use IP-based rate limiting (in-memory, not logged) to prevent abuse. This resets when the worker restarts and is not used to track or identify you.

## Third-Party Services

The Extension interacts with:

| Service | Purpose | Their Privacy Policy |
|---------|---------|---------------------|
| Google | Authentication & Calendar API | [Google Privacy Policy](https://policies.google.com/privacy) |
| OpenAI | AI processing (if selected) | [OpenAI Privacy Policy](https://openai.com/privacy) |
| Google Gemini | AI processing (if selected) | [Google Privacy Policy](https://policies.google.com/privacy) |
| Anthropic Claude | AI processing (if selected) | [Anthropic Privacy Policy](https://www.anthropic.com/privacy) |
| Cloudflare | Proxy hosting (free mode only) | [Cloudflare Privacy Policy](https://www.cloudflare.com/privacy/) |

## Your Choices

- **Revoke Google access**: Visit [Google Account Permissions](https://myaccount.google.com/permissions) to disconnect the extension.
- **Use your own API key**: Avoid using our proxy by providing your own OpenAI, Gemini, or Claude API key.
- **Clear local data**: Go to `chrome://extensions`, find Calendar AI, and click "Remove" to delete all locally stored data.
- **Manage frequent contacts**: Delete saved contacts anytime within the extension settings.

## Data Security

- API keys are stored locally in `chrome.storage.local` within your browser.
- We use HTTPS for all network requests.
- We do not sell, share, or rent your personal data to third parties.

## Children's Privacy

This Extension is not intended for children under 13. We do not knowingly collect data from children.

## Changes to This Policy

We may update this Privacy Policy occasionally. Changes will be posted on this page with an updated "Last updated" date.

## Contact

Questions or concerns? Reach out:
- **X (Twitter)**: [@Jeeeeeeswa](https://x.com/Jeeeeeeswa)
- **Chrome Web Store**: [Calendar AI](https://chromewebstore.google.com/detail/calendar-ai-text-screenshot-to-event/jbceogdnbbhhhjeglpllfbdpcccfhkkd)
