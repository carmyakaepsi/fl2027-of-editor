# FL2027 OF Editor By Epsi — Changelog

## Alpha 0.97
- **Scout DB: about 126,300 players** (was 109,900): Czech Republic, Austria, Ukraine, Norway and Sweden added; FL's European group of clubs is now covered 57% (was 37%). Sure matches about 17,800 game players.
- **Master League: the 40-player limit counts loans** — a club can hold at most 40 players under contract, including those out on loan at other clubs; a move into a club already at 40 does not register and the player ends up a free agent (that was the whole mystery of the moves into Inter and into your club: Inter 36 + 6 on loan, Juventus 29 + 19). The club list and the deal window now show *squad + on loan = total/40*, plain moves into a full club are blocked with the reason, and an exchange (or releasing someone) is proposed instead.
- The 0.96 rule "your club: exchanges only" is lifted: plain moves into and out of the club you control are allowed again (within the limit). Exchanges and signings in place of one of its players still also update the club's other tables.
- **Match Sim: broken saved line-ups are replaced** — a team whose saved eleven has several goalkeepers (or three or more players far out of position) plays with the best available eleven instead. In the FL2027 option file this concerns Lazio, Lecce and Hearts (4 goalkeepers in the saved eleven), Wydad (2) and two selections with none: use *Auto line-up* on them if you want the game to have a proper eleven too.
- Master League saves of **SP Football Life 2026** (PES 2021 key) open too: squads, contracts, loans, game plans and fixtures read the same way.
- **League mode (new tab, experimental)** for league-mode saves (LG00000000):
  - every league of the save with its **standings** (computed from the results in the save), the last results and the next matchday; the career date range;
  - **squads**: move a player to another club (his squad entry moves with him), exchange when the destination has 40;
  - **⇩ squads from the option file** (one club, one league or all): squads and shirt numbers become those of the option file, optionally the three game-plan presets too; players new to the league take the place of players who left the squad;
  - **📐 game plans** of every club, with the same window as the Master League;
  - **🏆 Simulate the rest in the Match Sim**: the League season starts from the real standings of the save and plays only its remaining matchdays (also the 100-season odds);
  - *Save LG* (verified by re-opening). Fixtures, results and standings are only read; player abilities in league mode come from the option file and the database.

## Alpha 0.96
- **Scout DB matching rebuilt**: each Scout DB player is compared with the game players of the same name, initial + surname or similar name of about the same age, and every pair is scored on **age, club, position and nationality first, the name after**; then the pairs are assigned best first, one to one. A pair is sure only when age, club or nationality and role agree and no other candidate comes close. Examples fixed: Ben White (Arsenal) now gets Benjamin White of Arsenal (82), not a 19-year-old Ben White (47); Alessandro Romano gets the Cagliari one, Giovanni Leoni the Liverpool centre-back instead of a goalkeeper with the same name; the two Vitinhas (PSG, Genoa) each get their own. Sure matches about 17,500 game players (were about 16,500 by name), Serie A 639 sure and 6 doubtful (were 613 and 33).
- The matching is computed once per session (a few seconds, with a message) and kept after imports.
- The doubtful-case screen also shows whether the role agrees.
- **Match Sim line-ups: stands and two clicks** — under the bench each side now lists the **stands** (the rest of the squad, best first). Click a player, then another: two starters swap places, and any starter, bench or stands player can swap with one of the other groups.
- **Managers: no team is left without one** (Squads → Change manager): choosing a manager who already leads a team swaps the two teams' managers (taking him away alone would leave his team without a manager and crash the game); a manager without a team simply replaces the current one. The list shows each manager's team.
- **Master League: game plans (experimental)** — *📐 Game plan* next to the team in the Master League tab: the team's three presets read from the save, a formation from the Plan Library on any preset, the twelve instructions, the presets copied from the option file, and starters / bench / stands with two clicks. The save keeps the presets in a tactics table and preset 1's formations also in the team record: both are written. CPU clubs probably pick their eleven by themselves before each match — to be confirmed in the game.
- **Master League: moves with the club you control (experimental)** — the editor finds the club you control (its players are listed in about ten more tables of the save: season data, morale, development…; a player added only to its squad was dropped by the game, which is why moves into your club ended with a free agent). Moves into or out of your club are now **exchanges only**: the incoming player takes the outgoing one's squad slot, shirt number, contract club and his place in all those tables (17–18 places per player in the test save). A free agent can be signed in place of one of your players (who becomes a free agent). Plain transfers into your club and releases from it are blocked with an explanation.
- Club finances: each team record holds two money values (+1604, +1608: about the club's funds and a round budget figure). They are not a wage cap — most clubs pay more in wages than either value — so the editor does not touch them.
- **Master League: career dates** — the Master League tab shows the career date range (from the most recent signing to the next match of your club: the exact day is not stored where the editor can read it yet), the club you control and its next match, read from the save's fixture list.
- **Master League moves keep the game plans consistent**: after a transfer, exchange or release, the starters / bench order and the set-piece takers of both clubs are remapped to the new squad (before, they kept pointing at the old squad slots).
- **Game Plan, two clicks to move anybody**: click a player, then another one — two starters swap places, a starter and a bench or reserve player swap in and out, two bench / reserve players swap. With a bench or reserve player selected, click the *Bench* or *Reserves* heading to move him there.

## Alpha 0.95
- **Scout DB: about 109,900 players** (was about 39,700 in 0.85). Covered like the big leagues (70–95% of the FL players of each league): England 1–2, France 1–2, Spain 1–2, Italy A–B, Germany, Netherlands, Belgium, Portugal, Scotland, Turkey, Denmark, Greece, Russia, Argentina, Chile, Colombia, China, Saudi Arabia, Japan, the MLS. Brazil A–B about one player in two (many nicknames end among the proposals), FL's Asian, European and Latin American groups 37–47%. Mexico, Canada, Switzerland, Poland, South Korea and more added. Nationalities completed for 35 more countries.
- One power scale as before: the four top leagues within about 1 point of FL's own level, smaller leagues stricter (second divisions, Netherlands, Portugal, Belgium −3 to −4; Scotland, MLS, Greece, Brazil B −5 to −6; Chile −7; China −10 on the 11 best players of each team).
- **🔍 Search Scout DB** on the player page: type a name, choose the Scout DB player and import him. It also opens by itself when *Scout DB* (player page or squad row) finds nobody with the player's name.
- Among namesakes in the Scout DB, the one with the player's age (±1) is now chosen directly (e.g. Lautaro Martínez of Inter, not the 19-year-old of Racing).
- **The player page closes with a click outside it** (also the Master League player page and the match reports).
- Doubtful-match screen faster with the bigger database (about 3 seconds for a league or the whole database).

## Alpha 0.9
- **League season** in the Match Sim tab (new "🏆 League season" mode): choose a league and play the whole season **matchday by matchday** (every match of the round at once) or straight to the end. Standings with form and top / relegation zones, the fixtures and results of every matchday (click a result for the full match report), top scorers, assists, average rating and cards.
  - Every team plays with its own game plan (preset 1). Injured players miss 1–5 matchdays, a red card one (two for a straight red), five yellow cards one; the best available eleven replaces them.
  - Matches against one of the team's three rivals are played as derbies. Home and away, injuries and derbies can be switched off.
  - **Season odds**: 100 whole seasons from the start (about 20 seconds) for title, top places and relegation percentages and average points.
- **Matchday** mode in the Match Sim tab: build your own matchday with any matches between any teams (add them one by one, or add a random round of a league), choose for each the kind of match (league, derby, decider, cup tie, final) and neutral ground, swap home and away; then **play them all at once** (scorers shown, click a result for the report) or get the **odds of each** (1000 simulations: 1 / X / 2, or who goes through in cup ties).
- **Most likely scorers** in every 1000× simulation: for each player the chance to score at least once, to score the first goal of the match and to score two or more (Single match: top six per side; Matchday: the four most likely in each match).
- **📋 Paste SofaScore** (Single match and Matchday): paste the text of a SofaScore match page (Ctrl+A, Ctrl+C, Line-ups tab open, Italian or English) and the editor reads:
  - the two teams (matched to the game's teams, changeable) and the **line-ups with formation** (probable or official): every player is matched by name and shirt number to the game squad, or to any game player when he is not in the squad; roles come from the formation; the bench comes from the substitutes when the official line-ups are pasted, otherwise from the game squad;
  - the **injured and suspended** players, left out (doubtful ones are kept);
  - the **recent results** of both teams (W/D/L of the last five) as a small team form effect (±0.5 rating points at most);
  - the **referee**'s cards per match, as a multiplier of the cards in the match;
  - the **bookmakers' odds**, turned into percentages without the margin and shown next to the simulator's.
  - Nothing is downloaded: only the text you paste is read. Player ratings are not in the copied text and are not used.
- **Form mode** in all three sims: *Random every match* (↓ 5% · ↘ 20% · → 50% · ↗ 20% · ↑ 5%, drawn again in every one of the 1000 simulations), *Arrows set by you*, or *Neutral*. In League season the random form persists from one matchday to the next (it stays about 6 times in 10, otherwise moves one step) and good or bad match ratings push it up or down; the players at ↑ are listed.
- **Match engine recalibrated** so that a season looks like a real one: the stronger side now gets clearly more chances (strength ratio exponent 0.5 → 2.5, normalised so that the total number of chances stays the same). Over many seasons the best team averages about 76–78 points (Inter, Arsenal, Bayern; Bayern wins the title about 8 times in 10), the weakest 19–34, with 2.7–3.1 goals per match. A single match between unequal teams is now less of a coin toss.
- Manager effects rescaled to the new engine (man management ±0.65 rating points, tactical knowledge ±0.8%): best against worst manager with the same squads about 48% against 25% wins.

## Alpha 0.85
- **Scout DB extended to about 39,700 players** (from about 15,700): England, Spain, France and Germany down to the second division, plus Scotland, now covered like Italy (86–96% of the FL players of those leagues). Women's football and the players generated at random by each source save are left out; a person present in several sources is kept once.
- Nationalities of the Scout DB completed for 28 more countries.
- **Doubtful matches in mass imports** (team, league, players shown, whole Scout DB): after the sure matches the editor shows how many cases are doubtful and lets you choose:
  1. **resolve them one by one** — the Scout DB player against the candidates in the game, with age, nationality, club, position, OVR and how close the name is; Back, skip, "accept the remaining likely ones", stop and import the choices so far;
  2. **accept all the proposals** (risky) — the best free candidate of every likely case, optionally also the possible ones;
  3. **import only the sure matches**.
- **Better matching**: besides the exact name, players are found by similar name (Kiernan / Kierman Dewsbury-Hall, Kang-In Lee / Lee Kang-In), initial ("F. Bernardeschi"), short or long form (Wesley / Wesley França, Max / Maximilian Kilman), with the same age (±1) and the same nationality or club. Nationalities and clubs are learnt from the sure matches. Several players with the same name are now resolved automatically when only one fits age and nationality / club.
- Names with ı, ø, æ, ß, ł, đ, ð, þ, œ are now compared correctly (Kenan Yıldız, Hörður, Đorđe…).
- One game player is never given to two Scout DB players.

## Alpha 0.8.1
- **Position map** on the player page and in the Master League player editor (replaces the 13 drop-downs): the positions on a pitch, green A / yellow B / grey C. Click a position to cycle it, Shift+click to make it the registered position (always A).
- **Second strikers from the Scout DB**: a forward rated A both as AMF and as CF becomes **SS** when his profile is more technical than physical (Dybala, Raspadori, Nkunku, Lookman, De Ketelaere…; about 1.7% of the DB, FL2027 has about 1%). Strikers such as Lautaro or Kane stay CF.
- **Three new manager attributes** with their own effects (they do not change abilities, nor the manager average or the squad effect):
  - **Man management** — Match Sim: motivation (about ±1 rating point between 40 and 99) and discipline (cards about ±20%).
  - **Tactical knowledge** — Match Sim: how well the chosen plan is played (attack, creation and defence about ±2.5%).
  - **Youth development** — Forecast, growth chart and Potential: growth of the club's players up to age 22 about ×0.8 (40) to ×1.2 (99). In practice 0–2 OVR points over five seasons.
  - Same squads, best possible manager (99) against the worst (40) on neutral ground: about 45% wins against 26% in 4,000 simulations (48% against 25% with the engine of the next version). These sizes are design choices of the editor, not measurements from the game.
  - Filled from the Scout DB; the Match Sim panels show each side's manager with the two values.

## Alpha 0.8

### New
- **Scout DB** (new tab): about 15,700 players with PES-scale ratings estimated by the editor's own conversion model, inspired by community data from football management games and calibrated on FL2027 (about 3 points of average difference per ability, 2 for goalkeepers). It contains no original game values. Abilities, registered position and A / B positions, reputation, form, injury resistance, weak foot and an estimated playing style.
  - Import one player, the players shown, a team, a league or everything; players are matched **by name only**, automatically (unique exact names) or manually (review and choose).
  - Each group (abilities, positions, style, reputation, weak foot, form, injury) can be switched off before importing.
  - **Lower-rated players** setting: lowers the abilities of players rated 65 or less by up to 8 points, fading out to nothing at 78; the best players are never touched.
  - Also in the Squads tab: *Scout* on every player row, *⚽ Scout DB* on the player page, *⚽ Scout DB for this squad* above the squad.
- **Managers from the Scout DB** (Managers tab): the manager attributes for the managers found by name, estimated on the editor scale (70 = the median manager).
- **Player.bin: playable positions, playing style and corner-kick motion are now read** for every player in the game (located against a Master League save: exact on all 25,858 players present in both). Line-ups, team ratings, call-ups and the Match Sim now know who is A or B in each role; *Edit this player* copies them, and editing one position keeps the others.
- **Auto line-up · all teams** (Game Plan): best eleven, bench, set-piece takers and captain for every team at once, each keeping its own formation; teams with fewer than 11 available players are skipped and listed.
- **Goalkeeper development**: forecast and potential now use a standard model for goalkeeping abilities (the measured curve shifted three years later: growth until about 28–29).

### Changed
- **Scout DB power scale**: the overall level of each player now follows a fixed scale of source ability levels (from about 58 for the lowest professional levels to 90+ for the world's best), weighted 80% against the model's own estimate so that each player keeps some individuality; the ability profile is kept and moved as a block. Serie A starters average about 79, Serie B starters about 71.
- Reputation of imported players in bands of 10 of the source potential: under 120 → 1, 120 → 2, 130 → 3, 140 → 4, 150 → 5, 160 → 6, 170 → 7, 180 or more → 8.

## Alpha 0.7

### New
- **Match Sim** (new tab): Team 1 against Team 2 with each side's game plan (one of the team's three presets, or any formation), starters and bench (swap by clicking), style, defensive line, stakes (must win / normal / a draw is fine) and motivation. Every player has a **form** of five arrows (↓ ↘ → ↗ ↑), kept by the editor. Match types: friendly, league, derby, title / relegation decider, cup tie and cup final (extra time and penalties). *Play match* shows the match minute by minute (goals, assists, cards, injuries, substitutions), then the statistics, player ratings and man of the match; *Simulate 1000×* gives win / draw / loss chances and the most likely scores. It is a statistical model calibrated on real football averages, not the game's engine.
- **Match Sim reads more abilities**: crosses from the wide players (Lofted Pass, Curl) to the players in the box, chosen and winning the duel by Heading, Jump, Physical Contact and height against the opposing centre backs; corners and wide free kicks bring the centre backs forward; shots from distance by Kicking Power and Curl; injuries depend on Injury Resistance and Physical Contact. Aggression decides who commits fouls and gets booked, Finishing who scores in the box.
- **Master League moves update the contract club.** Until now a transfer changed only the squads, so the player stayed under contract with his old club: the game treats that as a loan and could put him back or release him. Transfer, exchange, signing and release now also set (or clear) the contract club and the contract dates. Not confirmed in the game yet.
- **Exchange in Master League**: after choosing the destination club the editor shows the player's salary, both clubs' wage bills before and after, and the destination players with the closest salary (same role first) to exchange him with; a free agent can be signed by releasing one of them.
- Salary shown in bold on every Master League row, with a **loan** tag when the contract belongs to another club.
- **Save ML** next to Save in the top bar (it pulses while the career has unsaved changes).
- **Reload OF / Reload ML**: read EDIT00000000 or the Master League save again from disk, for example after playing and saving in the game. They use the linked save folder, or the file as it was opened or saved (Edge / Chrome); unsaved changes are discarded after a confirmation.

## Alpha 0.65

### Changed
- OVR recalibrated on 44 in-game values (36 within ±1, 43 within ±2).

### New
- **Paste format v1**: new lines `ID`, `Club` and `Date of Birth`. The editor writes ID and club in every export.
- **Bulk import matching**: by ID, or by name / shirt name / surname checked against nationality, age and position. Only sure matches are pre-selected; the dialog shows how each player was matched.
- **Export list** in the Database tab: all players of the current list in one paste file.
- **Forecast** on every player page: each ability and the OVR season by season for the next five seasons of a Master League.
- **Delete created players**: players created by the user (in the game or in the editor, ID 2147483648 and up) can be deleted from the squad table or their page; they leave every squad first. Database players cannot be deleted.
- **Paste & apply** on every row of the squad table and on every player page: reads the stats from the clipboard and applies them to that player in one click (asks first if the paste is for someone else, and then keeps the player's name).
- **Suggested B positions** in the FMInside conversion (FMInside gives only the natural positions). The model was learnt from the positions of 23,000 players in a FL2027 career: 71% of its suggestions match the game.

## Alpha 0.6

### New
- **Master League editor (experimental).** Load a Master League save (`ML00000000`) next to the EDIT file.
  - Browse every squad and the free agents as they are in the career, search any player, compare the rating in the career with the option file, see salary and contract end.
  - Player page with database / option file / Master League values side by side; abilities, registered position, reputation, age, playing style and playable positions are editable in the save.
  - **Bring to ML**: carry a player modified in the option file into the career, keeping the development he already had (*value in the save + option file − original database*), or overwriting it. One player at a time or all modified players at once; repeating it never adds the change twice.
  - **Transfers inside the career**: move to another club, release, sign a free agent. Confirmed in the game between CPU clubs; it does **not** work towards the club you control (the player becomes a free agent).
  - Ability changes are confirmed in the game.
  - **Save to folder**: with *Link save folder* active the Master League save is overwritten in place, like the EDIT file (previous file kept as `.backup`).
- **Growth chart** on every player page: expected rating now, in 3 and in 5 seasons of a Master League.
- **Formation families and historical game plans.** 21 shapes grouped by family and 34 historical plans (teams and managers of different eras), each with its own player positions and team instructions.
- **Plan Library.** All built-in and historical plans in one place; edit, duplicate, create custom plans, apply them to any team, and exchange them as text.
- **Tactics files.** Import and export `.PES2021_tactics` files (nkei's format on Evo-Web).

### Changed
- **Potential** is now simulated season by season with the development measured on a real Master League save (22,000 players): growth until about 25–26, almost the same for everyone, a little faster for reputation 6–8; goalkeeping abilities do not develop.
- **FMInside**: only the text paste is left; fetching the page from a link was removed because browsers block it.

### Fixed
- **Goalkeepers read from Player.bin**: GK Catching and GK Reflexes were swapped. Goalkeepers converted to modified players with earlier versions have the two values exchanged in the EDIT file and should be checked. OVR recalibrated accordingly (37 of 41 reference values within ±1).
- Position level **B** is confirmed as the middle value (it is used throughout the Master League data).

## Alpha 0.5

### New
- **Injured / Out of squad.** A player can be flagged as unavailable from the squad table or from his page, with a free note. He is sent to the reserves of every team he is in (a starter is replaced by the best available player for that role, and takers / captain are reassigned), he cannot be picked in Game Plan, and auto line-up, auto call-up, Global Adjust and the manager effect skip him. Optionally his abilities are lowered to 40 or 50 in the EDIT file so that the CPU does not pick him either. **Recover** makes him available again and restores the abilities.
  - The flag is kept by the editor (with the manager data), not in the EDIT file: the game has no "injured" state in the option file.
  - New Database filter: *Unavailable (injured / out)*.

### Changed
- "Rtg" is now called **OVR** everywhere.
- **Potential** always shows a number (equal to the OVR when there is no growth left).
- **OVR** recalibrated on 41 in-game values (37 within ±1); centre backs and midfielders were about one point too high.

## Alpha 0.4

### New
- **Potential.** Every player gets an estimated potential rating (the rating he could reach at 27). Players aged 27 or more have no growth left. Before that, growth depends on the years left, on the current rating and on reputation, and it flattens as the rating gets high. Shown on the player card, in the squad table and in the Database, where it can be filtered and ranked like any other value. It is an estimate of this editor and is not stored in the game.
- **Rating on the pitch.** In Game Plan each starter shows his rating in the role of the slot he occupies. A player out of position is recalculated for that role, lowered, and flagged in orange (related role) or red (wrong role).

### Changed
- **Team ratings** are based on the squad's best eleven in a 4-4-2 instead of the current starters, with a small weight (10%) for the next best players, so they no longer drop when the line-up is changed.
- **Name shortening** added to Global Adjust (`N. Surname`).

## Alpha 0.3

### New
- **Team ratings and ladder.** Every team gets a Team / DEF / MID / ATK rating from the best eleven of its squad in a 4-4-2 (each rated in the role of his slot; DEF includes the goalkeeper), whatever the current line-up. The team value also gives a small weight (10%) to the next best players. Shown at the top of the team page and in the new **Ladder** view in Squads, which can be filtered by league and sorted by any column.
- **Formation presets** in Game Plan: 4-3-3, 4-4-2, 4-2-3-1, 4-2-1-3, 3-5-2, 5-3-2, 4-3-2-1, 4-2-fantasia, 4-3-3 false nine. After setting one you can pick the best eleven for it straight away.
- **Save location.** *Save as…* asks where to write the file every time. *Link save folder* lets you choose the game's save folder once: Save then overwrites `EDIT00000000` there and keeps the previous file as `EDIT00000000.backup`.
- **Manager filters**: by nationality, by league, with or without a team, national teams.
- **Name shortening** in Global Adjust: turn the names of the filtered players into the short form `N. Surname` (Korean and Chinese names can be skipped).

### Changed
- **Created players** now use the ID range of players created in the game (from 2147483648). IDs outside that range made the option file fail to load.
- **Auto line-up** also sets the set-piece takers and the captain, and orders bench and reserves from goalkeeper to attack.
- After a manual substitution, a taker or captain who left the eleven is replaced automatically.
- **Overall rating** recalibrated on 31 in-game values from 62 to 89 (29 within ±1).

### Known limits
- Created players are still unconfirmed in the game with the new ID range.
- Choosing where to save and writing into a folder need Edge or Chrome (the exe uses them); the folder link has to be chosen again at every start.

## Alpha 0.2

### New
- **PES 2021 support.** A game selector next to *Load files*: auto-detect (default), Football Life 2027, PES 2021, or a custom 64-byte key file for other patches. The file is saved back with the key it was opened with.
- **Create player.** New players get a brand-new ID (the next one after the highest in use) and copy their look from any existing player. *Experimental: not yet confirmed in the game.*
- **Global Adjust page.** Change abilities for many players at once: filter by league, team, national squads, free agents, position, nationality, age, rating or any stat; adjust a group or a single ability by percent, by points, or set a fixed value. Preview before applying.
- **Manager attributes.** Nine staff attributes per manager (Goalkeeping, Attacking, Defending, Fitness, Possession, Technical, Tactical, Set pieces, Determination), 40–99 with 70 as neutral. They are kept by the editor, not in the EDIT file.
  - **Manager effect** on a squad: raises or lowers the players' abilities according to the manager; can be removed again, and re-applying never stacks.
  - Manager database tools: export / import as CSV, read an FMInside staff page, generate a baseline from squad strength, export / import the whole managers file.
- **Application icon** and window icon.

### Changed
- **Overall rating** now uses a per-position regression model, calibrated on 25 in-game values (all within ±1, 15 exact). Ratings below about 80 are not yet verified against the game.
- **Set pieces & captain** moved from Squads to **Game Plan**; only the eleven starters can be chosen. A taker who is no longer in the XI is flagged.
- **Playable positions** format shared with the PES Suite: `LWF, SS(B)` — no suffix = A, `(B)` = B. The two-line form (`Playable Positions B:`) is also accepted.
- **FMInside conversion** now also outputs reputation and playable positions in the shared format.
- An empty `<Player Skills>` or `<COM Playing Styles>` section in a paste no longer clears the existing ones.
- Converting many players at once is much faster (thousands per second).
- The program now uses a fixed local address so that manager data is remembered between sessions; only one instance runs at a time.

### Known limits
- Most features are still **not confirmed inside the game**. Keep a backup of your EDIT file.
- PES 2021 support was tested on the key handling only, not on an original PES 2021 EDIT file.
- Created players exist only in the EDIT file; whether the game accepts IDs that are not in its database is untested.
- Mass changes and the manager effect turn database players into modified players, which relies on the same untested assumption as "Edit this player".

## Alpha 0.1
- First release: squads, game plan with virtual pitch and auto line-up, transfers, database with filters and ladders, national call-ups with auto call-up, player editor, paste import / export, FMInside conversion, leagues, managers, competition and stadium names.
