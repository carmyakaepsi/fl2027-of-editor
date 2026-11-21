# FL2027 OF Editor By Epsi — Alpha 0.97

An option-file editor for **SP Football Life 2027** and **PES 2021**. It opens the game's `EDIT00000000` save, lets you change squads, players, line-ups, leagues and more, and writes the file back.

Everything runs on your own PC. No installation, no account, nothing is uploaded.

> **Alpha.** The editor has been tested by reading and re-writing real FL2027 files, but most features have **not yet been confirmed inside the game**. Always keep a backup of your `EDIT00000000` and try changes on a new Master League or exhibition match first.

---

## Quick start

1. Run `FL2027 OF Editor By Epsi Alpha 0.97.exe` (or open `FL2027_Editor.html` in Edge or Chrome: it is the same editor).
2. Click **Load files** and select these three files together (or drag them onto the window):

   | File | Where it is | Needed for |
   |---|---|---|
   | `EDIT00000000` | `Documents\KONAMI\eFootball PES 2021 SEASON UPDATE\<id>\save\` | everything (required) |
   | `Player.bin` | extracted from the FL2027 patch database | reading every player in the game |
   | `PlayerAppearance.bin` | same place as `Player.bin` | keeping a player's look when you start editing them |

3. Make your changes. Every change is listed in the **Log** tab.
4. Click **Save as…** and choose where to write the file, or use **Link save folder** to pick the game's save folder once: Save then overwrites `EDIT00000000` there and keeps the previous file as `EDIT00000000.backup`.

The save keys of FL2027 and PES 2021 are built in and the game is detected automatically. Use the **Game** selector next to *Load files* to force one, or to load a custom 64-byte key file for another patch.

**First launch on Windows:** the program is not code-signed, so SmartScreen may show "Windows protected your PC". Choose *More info → Run anyway*. The window closes the program automatically about 20 seconds after you close it.

---

## What you can do

### Squads
- Browse **Clubs → league → team**, **National** teams and **Other** teams.
- **Ladder**: all teams ranked by Team / DEF / MID / ATK rating (from the squad's best eleven in a 4-4-2, plus a small weight for depth), filterable by league and sortable. The same ratings are shown on each team page.
- Edit team name, short name, stadium name, manager, three rival teams, two team colours and four banner texts.
- Sign, transfer and release players; change shirt numbers (duplicates are swapped automatically).
- **Injured / Out of squad**: flag a player as unavailable. He goes to the reserves, cannot be picked in Game Plan or by the automatic tools, and his abilities can be lowered so the CPU does not use him; **Recover** restores everything. The flag is kept by the editor, not in the EDIT file.
- **Adjust squad %**: raise or lower the abilities of a whole squad.
- **Manager effect**: apply (or remove) the influence of the manager's attributes on the squad.
- Click any column header to sort.

### Game Plan
- Virtual pitch: drag the eleven starters; the role follows the pitch zone and can be forced by hand.
- Each starter shows his rating **in the role he is playing**; out-of-position players are lowered and flagged.
- Substitutions by clicking a starter and a bench player. Bench is squad slots 12–23, the rest are reserves.
- Three presets, fluid formation, team instructions.
- **Formations**: 21 shapes grouped by family (4-3-3, 4-4-2, 4-2-3-1, 3-5-2, 5-3-2 and so on), plus **34 historical game plans** (teams and managers of different eras) with their own player positions and team instructions.
- **Tactics files**: import and export `.PES2021_tactics` files (nkei's format on Evo-Web); drop one on the window to apply it to the selected team.
- **Auto line-up**: picks the best eleven for the current formation, sets takers and captain, and orders the bench from goalkeeper to attack.
- **Auto line-up · all teams**: the same for every team of the option file at once, each with its own formation.
- **Set pieces & captain**: chosen among the eleven starters.

### Plan Library
- Every built-in formation and historical plan in one place, with its pitch and instructions; edit them, duplicate them, or build your own **custom game plans**.
- Apply a plan to any team, save a team's current plan into the library, and exchange plans as plain text (copy / import).

### Transfers
- Two teams side by side: move a player either way, swap two players, release.
- Free-agent search with *Sign for Team 1 / Team 2*.

### Scout DB
- About 126,300 players with **PES-scale ratings estimated by the editor's own conversion model**, inspired by community data from football management games and calibrated on FL2027 (about 3 points of average difference per ability, 2 for goalkeepers). The Scout DB contains no original game values.
- Each player has the 25 abilities, a registered position with A / B positions, reputation (one level for every 10 points of potential, from under 120 → 1 to 180 or more → 8), form, injury resistance, weak foot and an estimated playing style (the least reliable value, about 59% agreement with FL). Tick or untick each group before importing.
- **Power scale**: the overall level follows a fixed scale (world's best 90+, top internationals about 87–89, Serie A stars about 84–86, very good Serie A starters 81–83, the best player of a Serie A team about 79–81, Serie A starters about 77–79, best Serie B players about 74–77, Serie B starters and bench 69–74, lower levels below 68), so every league sits on the same ladder. Players of the Scout DB are therefore on a slightly lower scale than the FL players you do not import.
- **Lower-rated players**: optional lowering of the abilities of players rated 65 or less (−2 to −8 points), fading out to nothing at 78; the best players are never touched.
- Import one player, the players shown (filters: club, nationality, position, match), a game team, a game league or the whole database. Players are matched to the game **by name only**: *Automatic* imports the unique exact names; *Manual* lists every match, lets you pick among players with the same name and untick the wrong ones.
- Click a player to see his PES values and copy them as paste text.
- The same import is in the Squads tab: **Scout** on every player row, **⚽ Scout DB** on the player page and **⚽ Scout DB for this squad** above the squad.
- **Managers**: *From Scout DB* in the Managers tab fills the manager attributes for the managers found by name (70 = the median manager).
- Not affiliated with or endorsed by any game publisher.

### Database
- Every player in the game, with filters by name, position, nationality, league, free agents.
- Value filters on any ability (for example *Dribbling ≥ 80*), combined freely.
- **Ladders**: rank players by any field, top or bottom.
- **Potential**: the best rating a player is expected to reach, simulated season by season with the development measured on a real Master League (growth until about 25–26, a little faster for the highest reputations). Editor estimate, not stored in the game.
- **Create player**: a new player in the ID range the game uses for created players (from 2147483648), copying the look of any existing player (experimental).
- **Export list**: every player of the current list (filters and ladder) in one paste file, with ID and club.

### Call-ups
- National team squads: call up, replace or drop players of that nationality.
- **Auto call-up**: best 26 by quota (3 GK, 4 CB, 4 FB, 8 MID, 7 FWD), then rebuilds the line-up.

### Global Adjust
- Change abilities for many players at once. Choose **who** (league, team, national squads, free agents, position, nationality, age, rating, any stat), **what** (a group or one ability) and **how** (percent, points, or a fixed value).
- A preview shows how many players and values change before anything is written.
- **Names**: shorten the names of the filtered players to `N. Surname`.

### Player page
- Players that were never edited are shown **read-only** from `Player.bin`. **Edit this player** turns them into a modified player stored in the EDIT file.
- Editable: names, nationality, age, height, weight, foot, registered and playable positions (A/B/C, on a clickable position map: click to change, Shift+click to register), 25 abilities, weak foot, form, injury resistance, **reputation (1–8)**, playing style, player skills, COM styles, attitude, commentary ID, motions and goal celebrations.
- **Quick adjust %** by group: all, attacking, technical, physical, defending, goalkeeping.
- **From FMInside**: paste the text of a player page from fminside.net and convert it to PES values (conversion engine from the PES Suite by Epsi). FMInside gives only the natural positions: B positions are suggested by a model learnt from the game (about 70% match).
- **Import paste / Copy as paste**: see below.
- **⚡ Paste & apply** (on the player page and on every row of a squad): applies the stats copied to the clipboard to that player in one click. If the paste is for another player it asks first, and the player keeps his name.
- **Forecast**: every ability and the OVR season by season for the next five seasons of a Master League, next to a small growth chart.
- **🗑 Delete**: players created by the user (in the game or in the editor, ID 2147483648 and up) can be deleted; they leave every squad first. Database players cannot be deleted.

### Match Sim
- Pick two teams. Each side starts from its own game plan (choose one of the team's three presets, or any formation with *Best XI*); swap starters and bench by clicking, and set style, defensive line, stakes and motivation.
- **Form**: five arrows per player (↓ ↘ → ↗ ↑, about −4 to +4 rating points), kept by the editor; *Random form* and *Reset form* per team.
- **Match type** changes intensity (cards), home advantage and how much the stronger side's edge counts: friendly, league, derby, title / relegation decider, cup tie, cup final (neutral, extra time, penalties).
- **Play match** shows the match minute by minute, then statistics, player ratings and the man of the match. **Simulate 1000×** gives the win / draw / loss chances the most likely scores and the most likely scorers (anytime, first, two or more).
- **Form mode**: random every match (drawn again in each of the 1000 simulations), the arrows you set, or neutral.
- **📋 Paste SofaScore**: paste the text of a SofaScore match page and the editor sets the line-ups and formations, leaves out the injured and suspended players, applies the recent results as a small team form effect and the referee's cards, and shows the bookmakers' odds next to the simulator's. Only the pasted text is read.
- **📋 Matchday**: your own list of matches between any teams (or a random round of a league), each with its kind of match; play them all at once or get the odds of each.
- **🏆 League season**: a whole season matchday by matchday or to the end, with standings, results, scorers, assists, ratings, cards, injuries and suspensions that carry over, derbies, persistent form, and the odds of 100 seasons (title, top places, relegation).
- **Which abilities count**: Finishing (shots in the box), Heading / Jump / Physical Contact / height (crosses, corners, wide free kicks), Kicking Power / Curl (shots from distance), Lofted Pass (crosses), Place Kicking / Curl (free kicks), passing and ball control (possession, assists), defending abilities and speed (chances conceded), Aggression (fouls and cards), Stamina (fatigue, substitutions), Injury Resistance (injuries), goalkeeping (saves). Skills and playing styles are not used yet.
- It is a statistical model of this editor, calibrated on real averages and on whole seasons (the best side of a league averages about 76–78 points; about 2.7–3 goals, 26 shots, 10 on target, 11 corners, 22 fouls per match; home wins about 44%, draws 26% between equal sides). It does not reproduce the game's engine.

### League mode (new, experimental)
Load a league-mode save (`LG00000000`) with the other files: standings of every league (computed from the results in the save), last results and next matchday; move players between clubs; bring squads (and game plans) in line with the option file; edit game plans; simulate the rest of the season in the Match Sim from the real standings; *Save LG* (verified). Fixtures and results are only read.

### Master League (new, experimental)
Load a Master League save (`ML00000000`, same folder as the EDIT file) together with the other files, or on its own. A club can hold at most **40 players under contract including those out on loan**: the editor counts them and blocks moves into a full club (they would not register in the game).
- **Read the career**: every squad as it is in the save, free agents, search by name; rating in the career against rating in the option file, salary and contract end.
- **Player page**: database / option file / Master League values side by side. Abilities, registered position, reputation, age, playing style and playable positions can be edited directly in the save.
- **Bring to ML** (also from the normal player page): carries a player you changed in the option file into the career. By default each ability becomes *value in the save + (option file − original database)*, so what the player gained or lost during the career is kept; you can also overwrite with the option-file values. **Bring all modified players** does it for everyone. Repeating it does not add the change twice.
- **Transfers inside the career**: move a player to another club, release him, or sign a free agent. Only the squads change: no fee, no budget change, nothing in the transfer history.
- **Growth chart**: on every player page, the expected rating now, in 3 and in 5 seasons.
- **Save ML** (top bar, next to Save) writes the save and re-opens it to check it. **Reload ML** / **Reload OF** read the files again from disk, for example after playing and saving in the game. With **Link save folder** active the button becomes *Save ML to <folder>* and overwrites the save directly, keeping the previous file as `ML00000000.backup`. Save while the career is not open in the game.

Keep a copy of your save. What is confirmed in the game: ability changes, and transfers between CPU clubs. **Moving a player into the club you control does not work** (the game puts him among the free agents): sign him in the game.

### Managers, Leagues, Competitions & Stadiums
- Rename managers and change their nationality; filter them by nationality, league or team.
- **Manager attributes** (Goalkeeping, Attacking, Defending, Fitness, Possession, Technical, Tactical, Set pieces, Determination; 40–99, 70 = neutral), used by the manager effect on the squad. Three more have their own effects: **Man management** (Match Sim motivation and discipline), **Tactical knowledge** (how well the plan is played in the Match Sim) and **Youth development** (growth of the club's players up to 22 in Forecast and Potential, about ×0.8 to ×1.2). Small effects, editor estimates. The game has no such data: they are kept by the editor and can be exported as a file or CSV, read from an FMInside staff page, or pre-filled with a baseline estimated from squad strength.
- **Leagues**: swap two teams between leagues (each league keeps its number of teams).
- Rename the competitions and stadiums that are stored in the EDIT file.

---

## The paste format

Players can be imported and exported as plain text. Only the lines that are present are applied, so a partial paste changes only those values. Several players can be pasted one after another; each starts with `Name:`.

**Import paste** in the Database tab takes many players at once. Each block is matched by **ID**, or else by name, shirt name or surname checked against nationality, age (±1) and position; only sure matches are pre-selected, the others are shown for you to check. **Export list** saves every player of the current Database list (filters and ladder) as one paste file, with ID and club.

```
PES 2021
Name: Luis Milla
Shirt Name: LUIS MILLA
Nationality: Spain
Player Styles: Box-to-Box
Height: 175 cm
Weight: 71
Foot: R
Age: 32
Registered Position: CMF
Playable Positions: DMF, AMF(B)
Reputation: 5
Ability Settings
Offensive Awareness: 68
Ball Control: 81
...
Weak Foot Usage: 3
Weak Foot Acc: 3
Form: 6
Injury Resistance: 3
<Player Skills>
19 - First-time Shot
20 - One-touch Pass
<COM Playing Styles>
05 - Long Ball Expert
```

- **ID:** the FL player ID, written by the editor's exports. When present it decides which player the block is for.
- **Club** and **Date of Birth** (`YYYY-MM-DD`, also `DD/MM/YYYY`): used to find the right player when there is no ID, and Date of Birth gives the age (FL2027 counts age as 2026 − year of birth) when there is no `Age` line.
- **Playable positions:** no suffix = A, `(B)` = B, not listed = C. The registered position is always A and is not repeated. `-` means none.
- **Nationality:** country name or numeric ID.
- **Optional lines:** `Reputation`, `Commentary`, `Attitude`, `Goal Celebration 1/2`, `Free Kick`, `Penalty Kick`, `Corner Kick`, `Hunching (Dribbling)`, `Arm Movement (Dribbling)`, `Hunching (Running)`, `Arm Movement (Running)`, `Dribbling Motion`.
- An empty `<Player Skills>` or `<COM Playing Styles>` section leaves the current ones untouched.

The same format is produced by the **PES Suite** ("Copy stats FL 2027" and "Esporta FL 2027").

---

## Known limits — please read

- **Not verified in the game yet.** File reading and writing is exact (an unmodified file is re-written byte for byte), but how the game reacts to each change still needs testing.
- **Players read from `Player.bin`.** Its format is not publicly documented and was worked out for this tool. Names, nationality, age, height, foot, position, reputation and the 25 abilities are read; weight is the least reliable value. Playable positions (A / B / C), playing style and the corner-kick motion are read too (located against a Master League save, exact on 25,858 players). Skills, COM styles, weak foot, form, injury resistance and some motions are **not** read yet.
- **"Edit this player"** marks only the decoded groups as edited and relies on the game keeping its own values for the rest. This is an assumption: test one player in the game before converting many.
- **Position level B** is written as the middle value between C and A, the same value the game uses in Master League saves.
- **Rating** is an estimate of the in-game overall (per-position regression model calibrated on 44 in-game values from 62 to 89, 36 of them within ±1 and 43 within ±2; fast centre backs tend to be rated 1–3 points too high and playmaking defensive midfielders 1–2 too low).
- **PES 2021** support was tested on the key handling only, not on an original PES 2021 EDIT file. League names are shown as "League n" for non-FL files.
- **Created players** exist only in the EDIT file; whether the game accepts an ID that is not in its database is untested.
- **Global Adjust and the manager effect** turn database players into modified players, which relies on the same assumption as "Edit this player".
- **Manager attributes** are stored on your PC (and in the files you export), not in the EDIT file.
- **Leagues:** only swaps are offered; league names are inferred from the teams they contain.
- **Not in the EDIT file, so not editable there:** contract and loan dates, owner club, market value, competition structure.
- **Master League.** Skills, weak foot, form and injury resistance are not located in the save yet, so they are not carried over. *Bring to ML* assumes your option-file changes were made after the career started (a career already contains the edits that existed when it began). Salary and contract dates are shown but not editable. Transfers do not work towards the club you control.
- **Goalkeepers converted with Alpha 0.5 or earlier**: GK Catching and GK Reflexes were read in the wrong order from `Player.bin`. Players you turned into modified players with those versions have the two values swapped; check your goalkeepers.

---

## Credits

- Save encryption: algorithm from **pesXdecrypter** (public domain), the4chancup.
- EDIT file layout: based on **4ccEditor** (zlib licence), the4chancup, checked against FL2027 files.
- FMInside conversion: **PES Suite** by Epsi.
- SP Football Life is the work of the SmokePatch team. This tool is unofficial and not affiliated with them or with Konami.
