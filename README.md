# Wand Duel

Wizard duelling as an installable web app (PWA). Pick one of six wizards, step in and out of range, cast bolts, raise your shield at the right moment and unleash your own super spell. A Duelmaster on the dais calls every hit in Latin and signals it with a lantern staff, and the first to the point limit wins.

**Play:** https://matdata-eu.github.io/game-wizard-duel/

## Modes
- **Starter** (default): for people who have never played. Only step, cast, shield and your super spell. Bolts fly a little slower, duels go to 5 points in 3 minutes, and a gold hint under your wizard says when to shield, when to step away and when your super spell is ready. The menu only asks for opponent, bot level and wizards.
- **Expert**: everything below, including the charged blast, the blink, reflecting with a perfectly timed shield, and 5, 7 or 10 point duels.
- **Bot**: you (gold, left) against a bot (azure, right) on Easy, Medium or Hard. Harder bots react faster, shield more often and more precisely, keep a closer range and save their super spell for the right moment.
- **2 Players**: two people on one device. Keyboard: Player 1 `A D` step, `S` cast, `W` shield, `E` blink, `Q` super spell. Player 2 `← →` step, `↓` cast, `↑` shield, `/` or right `Shift` blink, `.` or `Enter` super spell. Against the bot, the arrows, `Space` (blink) and `F` (super spell) work for you too. On a touchscreen each player gets buttons on their side.

## The wizards
| Wizard | Super spell | What it does | How to survive it |
|---|---|---|---|
| Orin Ashgrove | Starfall | Three stars fall where the opponent stands; their shadows follow, then stop just before impact. | Shields don't help: step out of the shadow. |
| Kael Emberforge | Phoenix | A fast firebird that burns through a shield. | Raise the shield at the very last moment, or blink. |
| Bram Thornwood | Rootbind | Vines hold the opponent: no stepping, casting or shielding. | Mash any button to break free sooner. |
| Selene Frostmere | Mirror Ward | For 5 seconds an ice mirror throws back every bolt. | Don't cast into it. |
| Nyra Voss | Storm Lash | Thunder gathers over the opponent, then lightning strikes. | Shield before it strikes, or blink. |
| Mira Quickfern | Triple Volley | Three quick bolts in a row. | One shield won't stop them all. |

Three men and three women, all original characters. The star bar under each name fills slowly during the duel, faster when you block and a little when you are hit.

## Moves
| Control | What it does |
|---|---|
| Step | Advance or retreat half a metre. Closer means your bolts arrive before your opponent can react, but so do theirs. |
| Cast | Fires a spark bolt. Costs mana (the blue bar), which refills quickly. |
| Hold cast (Expert) | Charges a blast. A shield stops it but is driven back hard, towards the edge of the circle. |
| Shield | A short magic shield. Blocking pushes you back a little. In Expert, a shield raised just before the bolt arrives reflects it. |
| Blink (Expert) | Jumps 1.5 m back (or forward while holding forward); spells pass through you during the blink. |
| Super spell | Your wizard's own spell, once the star bar is full. |

Two bolts that meet in the air cancel out; a charged blast or the Phoenix wins against a plain bolt.

## Scoring and the Duelmaster
- **Punctum**: a point for every hit. Hit by your own reflected bolt? The point goes to your opponent.
- **Ictus duplex**: both hit at the same moment, no point.
- **Extra circulum**: step (or get pushed) out of the circle and the point goes to your opponent.
- **Tempus** and **Mors subita**: when time runs out the leader wins; if the score is level, the next point wins.
- The Duelmaster calls Salutate (bow), Ad baculos (wands up), Pugnate (duel), Siste (stop), Scutum (blocked), Reflexum (reflected), Concursus (spells collide) and the names of the super spells, and signals with the staff: raised to the side that scores, pointing down for a ring-out, arms waving for no point.

## Install
Open the game in Chrome, Edge or Safari and choose "Install" or "Add to Home Screen". After the first load it works offline.

## Run locally
No build step. Serve the folder over `localhost` or HTTPS, for example:

```sh
python3 -m http.server 8000
```

Files: `index.html` (the whole game), `manifest.webmanifest`, `sw.js` (offline cache), `icons/`. Pushes to `main` deploy to GitHub Pages through `.github/workflows/pages.yml`.

## Support
Found a bug or have an idea? [Open an issue](https://github.com/Matdata-eu/game-wizard-duel/issues).

## Credits
- Game, characters, graphics and sound effects: made from scratch in code (canvas drawing, Web Audio), no third-party assets. The Duelmaster's voice uses your browser's built-in speech (an Italian voice reads the Latin) when available.
- Fonts: [Bungee](https://fonts.google.com/specimen/Bungee) by David Jonathan Ross and [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) by Jeremy Tribby, both under the SIL Open Font License, loaded from Google Fonts.
- Built by [Matdata](https://matdata.eu) with [Claude Code](https://claude.com/claude-code).

## License
[MIT](LICENSE)
