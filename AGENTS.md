# AGENTS.md — jonathanmccallum-te (Telugu mirror of jonathanmccallum.com)

Telugu mirror site. Same theme and design as the main site (Paper Light),
content translated into Telugu, meaning-first. Repo: streamjonathan/jonathanmccallum-te.
Live (when approved): te.jonathanmccallum.com. Proof: jonathanmccallum-te.pages.dev.

## Mission

Mirror jonathanmccallum.com in Telugu — every article translated for meaning,
not word for word, in Jonathan's voice: plain short sentences, friendly, positive,
never preachy. An average person interested in Jesus, not an expert or theologian.

## Roles

- **Bobby (Muse) is the lead builder.** He coordinates, builds, pushes to GitHub
  and deploys to Cloudflare. He is the ONLY one who pushes or deploys.
- **Claude advises and reviews** translation quality. He does not push or deploy.
- **Helper Muses translate** one article at a time, drafts only.

## The one rule above all

**Never publish or alter live production assets without Jonathan's clear
permission.** The Telugu site goes live on te.jonathanmccallum.com only when
he says so, after reading the pilot article(s). Drafts stay drafts until he
approves them. Work on a branch, never straight on main. Give Bobby a preview URL.

## Translation rules

- English repo (streamjonathan.github.io) is the source of truth. Articles are
  translated from the English Markdown, keeping the same date, slug, source_video
  and shareImage. Only the title and body are translated.
- Lewis quotations: use the published Telugu translation where one exists
  (cite it); otherwise translate fresh and mark it "translated for this site".
- Bible verses: use the TELUBSI (Telugu Bible, Bible Society of India) wording, never re-translate from the English article. No direct verse quotations appear in the 5 proof articles; the 'bread of life / water of life' lines are Jonathan's paraphrase, translated meaning-first (John 6:35 TELUBSI verified: జీవాహారము నేనే…).
- Names (never vary): యేసు, దేవుడు, అస్లాన్, నార్నియా, లూసీ, డిగోరీ, టిరియన్, ఆదాము మరియు హవ్వ. Book titles use the meaning-first site renderings (నార్నియా కథలు, మాంత్రికుడి మేనల్లుడు, గొప్ప విడాకులు, అంతరిక్ష త్రయం, చివరి యుద్ధం) — flagged for Jonathan, as no published Telugu titles were found.
- Voice: Register: respectful plain Telugu, reader addressed as మీరు, short plain sentences, warm and honest, no preaching.
- No emojis, no newsletter form, no links the English article does not have.
- Never invent facts, dates, links or details.

## Site facts

- Eleventy 3, Cloudflare Pages, Paper Light theme (Fraunces + Newsreader).
- No Ask chat and no note Worker on this site yet — search (Pagefind) works,
  Ask and notes come later. The Ask floating button and ask.js are removed.
- CSS is preloaded, not inlined (CSP blocks inline style). Bump the `?v=` query
  on any CSS/JS file you change.
