# PocketFirm

Connects your AI assistant to [PocketFirm](https://pocketfirm.app), where you work with your accounting firm. Ask what your firm still needs from you, then handle it in a conversation: answer forms, upload requested documents, message your firm and download documents it shared with you.

The assistant signs in as you and reaches only your own records with your own firm. It never sees another client's records.

## Connect

Your firm decides whether its clients may use AI apps. The connection only appears in PocketFirm when your firm allows it.

Connection address:

```
https://app.pocketfirm.app/api/mcp
```

1. In PocketFirm, open **Settings → AI apps** and choose your AI app under **Connect an app**, or open your AI app's Apps or Connectors settings and add the connection address above.
2. Sign in to PocketFirm as yourself and approve the connection. No password is shared with the AI app, and there is no API key or secret to configure.
3. Choose the access: **Ask before changes** (the default) or **View only**, within what your firm allows. With View only, the assistant can look but cannot change or send anything.

To disconnect, open **Settings → AI apps** in PocketFirm and disconnect the app. You can also remove the connection in the AI app's own settings.

In Claude Code, install it from this repository with `/plugin install pocketfirm --marketplace Firmary/pocketfirm-plugin`.

This repository is a plugin package for hosts that install plugins (Claude Code, Cursor, Grok, and hosts that read `plugin.json`). It contains the manifests, the connection address and two skills, and no credentials.

## What the assistant can do

- **See what your firm needs**: your to-dos, forms, document requests, signature requests, proposals, invoices, unread messages and appointments.
- **Answer forms and questionnaires**: open an assigned form, go through the questions with you, save a draft, and submit once you have seen the answers and said go ahead.
- **Upload documents**: send a file to a document request, a form's file question or a message, when your firm has turned on uploads. Files are checked for malware before your firm sees them.
- **Find and download documents** your firm shared with you.
- **Message your firm**: read your threads, reply, or start a new one.
- **Appointments, invoices and notifications**: book, move or cancel appointments, read invoices, and read notifications.
- **Search PocketFirm's help articles.**

## What the assistant cannot do

- Sign documents, pay invoices or set up payment methods. These stay in PocketFirm, on your firm's own pages. The assistant gives you the link.
- Reach anyone else's records, or anything your own PocketFirm account cannot see.
- Change anything when the connection is set to View only.

## Nothing reaches your firm without your confirmation

Anything your firm will see, such as a message, a submitted form, an upload, a booking or a proposal decision, needs your go-ahead first. In **Ask before changes**, the assistant shows you what it will send before it runs. When a change needs your approval, you get a link that opens PocketFirm, where you check the exact change and choose **Approve** or **Decline**. Accepting a proposal also asks you to sign in to PocketFirm again.

## Skills

- `get-started`: what you can ask for and how approvals work.
- `finish-my-requests`: work through everything your firm has asked of you, one item at a time.

## Support

Help and setup: https://firmary.app/support/. Questions about your own account or documents go to your firm. For problems with PocketFirm itself, email support@firmary.app with your firm's name and what you tried. Never send passwords, sign-in codes or tax identifiers.

[Privacy policy](https://firmary.app/privacy/) · [Terms](https://firmary.app/terms/)

## License

MIT
