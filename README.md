# 家永 泰地 / Taichi Ienaga

長崎大学 情報データ科学部 3年(2028年3月卒業見込み)。大学セーリング部(470級)で広報を担当しています。
**部活や自分の生活で困ったことを、AI を使って自分で作って解く**のが、いまいちばん力を入れていることです。

Third-year student at Nagasaki University (Faculty of Informatics and Data Science, class of 2028). I race 470-class dinghies on the university sailing team, and I build the tools my team and I are missing — with AI doing much of the implementation while I decide what to build and what is good enough to ship.

📧 happiitsumo@gmail.com

---

## 主な制作物 / Featured projects

| | 何を解くか / What it solves | 技術 / Stack |
|---|---|---|
| **[470.daichi.app](https://470.daichi.app)**<br>([ソース / source](https://github.com/happiitsumo-bit/470-reviewer)) | 艇も海も無い家でセーリングを練習できる、470級の3Dアプリ。ロープを引くとセールの形が変わり、走りが点数で出る。実在の35製品を試着でき、「チューニング道場」で部品から規則・安全まで学べる。クラスルールの寸法から Blender で艇を生成している。<br>A browser-based 3D learning app for the 470 dinghy: pull a line and the sail reshapes, with a live performance score and 35 real sail products to try on. The boat is generated in Blender from the class-rule dimensions. | Blender (Python) → glTF → three.js, Vite + React, Hono on Cloudflare Workers |
| **[sailvlog](https://github.com/happiitsumo-bit/sailvlog)**<br>([本番 / live](https://sailvlog.vercel.app)) | ヨット部の反省会を、記憶とホワイトボードから航跡データへ。複数艇の GPS を同じ時間軸で再生し、タイムラインに注釈を残して共有する。最初の版を「何の課題を解くか説明できない」と自分で否定し、課題1本に絞って作り直した。<br>Replays several boats' GPS tracks on one timeline, with annotations, for post-race debriefs. I scrapped v1 as unfocused and rebuilt it around a single problem. | Next.js, Express, Prisma, PostgreSQL, Docker, GitHub Actions(CI・本番の死活監視 / CI and production watchdog) |
| **[daichi.app](https://www.daichi.app)**<br>(Bunshin) | QR から開く LINE 風の自己紹介チャットボット。生成 AI は使わず、例文で意図を分類しルールで返す方式で、誤答するより聞き返す側に倒した。外部 AI と測り比べ、安全弁が消えるため本体には入れないと判断した。<br>A QR-code chatbot about me, built without an LLM (intent classification + rules). It asks clarifying questions rather than guessing; I benchmarked an external AI and chose not to adopt it. | TypeScript, TF-IDF + ロジスティック回帰, Vercel |

## そのほかの制作物 / More projects

非公開のリポジトリです。コードを見たい場合はご連絡ください。 / Private repositories — happy to walk through them on request.

- **home-agent** — 自宅の PC で24時間動く個人用エージェント。新着の確認を15分おきに行い、知らせと質問は Slack に届く。SQLite の台帳と検索で記憶を持つ。 / A personal always-on agent on a home server (WSL2), with a SQLite ledger and Slack for notifications. — Python, SQLite, Slack
- **talk-notes** — 講演の録音を文字起こしして要約メモにする。iOS ショートカットと Swift/Python、無料枠だけで動く。 / Transcribes talk recordings into summary notes, running on free tiers. — Swift, Python, Whisper
- **botswap** — 自分の分身チャットボットを作って人と交換できるアプリの構想(Bunshin の発展)。 / Concept: build your own chatbot persona and swap it with others.
- **atcoder-practice** — 競技プログラミングの練習記録。 / Competitive-programming practice log.

## 技術スタック / Tech stack

| 分野 / Area | 使っているもの / What I use |
|---|---|
| 言語 / Languages | TypeScript · JavaScript · Python · Shell · SQL |
| フロント / Frontend | React · Next.js · Vite · three.js(3D) |
| バックエンド / Backend | Node.js · Express · Hono · Prisma |
| DB | PostgreSQL(Neon) · SQLite |
| インフラ・配信 / Infra | Vercel · Render · Cloudflare Workers · Docker · Tailscale · WSL2 |
| CI・品質 / CI & quality | GitHub Actions · Playwright · テストの実測(CI で件数を数える) |
| 3D・制作 / 3D & media | Blender (Python) · glTF / gltfpack · Figma |
| データ・ML / Data & ML | Python · scikit-learn の分類器(TF-IDF + ロジスティック回帰) · Whisper(文字起こし) · Kaggle |

## 開発の道具 / Tools & workflow

- **AI コーディング / AI coding**: Claude Code · Codex CLI · Google Antigravity — 並列に走らせ、実装は任せ、仕様・品質ゲート・公開の条件は自分が持つ。 / I run several agents in parallel and own the spec, the quality gates and the release criteria.
- **環境 / Environment**: macOS · zsh · tmux · Ghostty · VS Code · git worktree · Homebrew
- **連携 / Integrations**: GitHub · Slack · Notion · Google Workspace · Microsoft Outlook(MCP コネクタ経由 / via MCP connectors)

## 大事にしていること / What I care about

**AI で楽をする。** 手でやると時間がかかる作業は、AI に任せられる形に直してから任せる。浮いた時間で、何を作るか・どこまでやれば公開してよいかを考える。
**Make AI do the tedious work.** If something is slow to do by hand, I reshape it so AI can do it, and spend the saved time on what to build and when it is good enough to ship.

- 実装は Claude Code・Codex などに並列で任せる(sailvlog は AI エージェントに実装させて作った)。 / I hand implementation to several coding agents in parallel.
- 繰り返す作業は仕組みにする(新着の確認を15分おきに行う常駐エージェント、録音から要約メモまでの自動化)。 / Recurring chores become automations.

## 連絡 / Contact

インターン・選考のご連絡は上のメールへ。 / Reach me by email for internships and recruiting.
