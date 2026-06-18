# Who I Met

A tiny app for the people you meet. Snap a photo, say a sentence, or jot a note — it lands in a private daily diary and a living map of your network. Designed for HiRey's **Hi** platform: later, each person you log can claim their own Hi profile, and the two of you mutually tag into a real relationship edge.

**Live app:** https://walter2wer.github.io/who-i-met-today/

## What it does

- **Capture** — one tap: take a photo, pick from your library, or *just say / write* who you met (the app pulls the names out).
- **Diary** — everyone you meet, by the day.
- **Network** — a colour-coded map of your circle; a lightweight CRM (notes, follow-up flags, every moment with a person).

## Privacy by design

- **Everything stays on your device.** Photos and notes live in your browser (IndexedDB). Nothing is uploaded or published.
- **No face recognition. Ever.** A face is only named by a person who was there, typing. The app never runs 1:N "search a face → find the person" matching — that line is what separates this from surveillance tooling.
- The future "claim your profile" + "mutual tag" steps are **invitation-based and consented**: a person becomes a node only when *they* opt in.

## Run locally

Open `index.html` over http (not `file://`, so browser storage works):

```
python3 -m http.server 4178
# then visit http://127.0.0.1:4178/
```

Single self-contained HTML file — no build, no dependencies, no tracking.

## License

MIT
