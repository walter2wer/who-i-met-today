# Who I Met

A tiny app for the people you meet. Snap a photo, say a sentence, or jot a note — it lands in a private daily diary and a living map of your network. Designed for HiRey's **Hi** platform: sign in and each person you log can claim their own Hi profile, and the two of you become a real, consented relationship edge.

**Live app:** https://walter2wer.github.io/who-i-met-today/

## What it does

- **Capture** — one tap: take a photo, pick from your library, or *just say / write* who you met (the app pulls the names out).
- **Diary** — everyone you meet, by the day.
- **Network** — a colour-coded map of your circle; a lightweight CRM (notes, follow-up flags, every moment with a person).

## Sign in (optional)

The diary works fully offline with no account. **Sign in to HiRey** (tap the avatar in the header) to unlock the cloud half — and nothing more:

- **Your real profile on the cards.** One-tap sign-in with email, phone, or Google. Your HiRey name, headline and bio (editable in-app) flow onto the we-met cards you send. Calls Hi's web-auth endpoints directly — no backend, no server holds your session.
- **Send a real, consented invite.** When you have a person's email or phone, *Send HiRey invite* registers you as the person who met them (`connectors.report_met_person`) and pre-creates a page they can claim. They choose to accept or decline — decline and the edge is gone.
- **See who's on HiRey.** People who are connected through you show a live status pulled from `connectors.list_met`.

Capabilities used: `hi.owners`, `hi.connectors` (→ `hi.social-relationships` + `hi.pairings`).

## Privacy by design

- **Your diary stays on your device.** Photos and notes live in your browser (IndexedDB). They are *never* uploaded — signing in only syncs **your own** profile and sends the invites **you** choose to send.
- **No face recognition. Ever.** A face is only named by a person who was there, typing. The app never runs 1:N "search a face → find the person" matching — that line is what separates this from surveillance tooling.
- **Claim is invitation-based and consented.** A person becomes a node only when *they* opt in; the invite carries no diary data, just your name and a way to claim.

## Run locally

Open `index.html` over http (not `file://`, so browser storage works):

```
python3 -m http.server 4178
# then visit http://127.0.0.1:4178/
```

Single self-contained HTML file — no build, no dependencies, no tracking.

## License

MIT
