# Aethel Apps

A pair of web apps for the **Aethel** tabletop RPG system.

## Apps

**[Pasqually's Spell Slinger](https://farewellfox.github.io/Aethel/pasqually-spell-slinger.html)**
Spell builder and library for The Mind and The Spirit classes.

**[Aethel Character Sheet](https://farewellfox.github.io/Aethel/aethel-character-sheet.html)**
Full digital character sheet with live calculations and level tracking.

Open either link in your browser — no download or installation required.

---

## Pasqually's Spell Slinger

A spell builder and library for **The Mind** and **The Spirit** classes.

### Building a Spell
- Select your **class** (Mind or Spirit). The augments update to show only what's relevant to you
- For Spirit, select your **subclass** (Oracle, Templar, or Zealot) to filter subclass-specific augments
- Choose a **Spell Form**. This is the shape and delivery method of your spell
- Add **Strand Augments**. Each one adds to the spell's cost and effect
- The running **Resource Point cost** and **power tier** update live as you build
- Name your spell and save it to your **spell library**

### Spell Library
- Saved spells persist between sessions in your browser
- **Export** your library as a `.json` file to back it up or share it
- **Import** a `.json` file to load spells from another device or player

### Notes
- Higher-tier augments are gated by class level; these are flagged in the interface
- Condition augments include a dropdown to choose the specific condition applied
- The power tier reference table highlights your current spell's tier as you build

---

## Aethel Character Sheet

A digital character sheet with some live calculations.

### Getting Started
1. Enter your **ability scores** first. Modifiers, saving throws, and skill totals calculate automatically, though racial and other skill bonuses are excluded from calculation.
2. Fill in your identity (name, species, class, archetype, etc.)
3. Go to the **Level Log** tab and click **Add Level 1**. Your character level on the sheet is driven by the log
4. Continue adding levels as your character progresses: track your HP and skill point allocation. It is okay to exceed the available points as the character sheet does not track specific increases.
5. Skill caps based on level are flagged in the skill section of character sheet. Exceeding the cap is cheating. No cheating!!!!

### Character Sheet Tab
- **Ability scores**: Enter your scores and modifiers calculate automatically
- **Saving throws**: Fortitude, Reflex, and Will calculate live from your scores. Reflex and Will automatically use whichever of their two governing stats is higher, and label which one they're using
- **Spell Save DC**: Calculates as `8 + ⌈level ÷ 2⌉ + governing mod`. Defaults to INT; use the dropdown to switch to WIS or CHA for archetypes that use those instead
- **Resource**: Tracks current and maximum AP / FP / RP.
- **Skills**: Shows available points, points spent, and points remaining. Each skill displays its total bonus (points + ability mod). Skills over the cap for your current level are flagged in red
- **Daily Archetype Ability**: Click the hex to mark it as used; requires a manual reset; reset occurs on long rest.

### Level Log Tab
- Add one entry per level gained
- Each entry tracks HP gained and notes (new features, augments learned, etc.)
- Skill points for that level are allocated per skill within the entry
- The log enforces the correct point budget per level based on your INT modifier
- Delete any level entry if you need to correct a mistake. Entries renumber automatically

### Notes & Lore Tab
- Nine free-label text boxes for equipment, faction standing, treasure, retainer info, backstory, or anything else

### Cheat Sheet Tab
- Quick reference for attack rolls, advantage/disadvantage, critical hits, defense, skill DCs, resting, and conditions

### Saving Your Character
- Click **Save** to store your sheet in the browser's local storage
- Click **Load** to import a `.json` character file. Useful for moving between devices or sharing with your GM (we don't use the term DM. DM is henceforth banned)
- Your data is stored locally and does not leave your machine

---

## Notes for the Group

- Both tools work entirely in the browser.
- Local storage is per browser, per device. Use Export / Load to move data between machines
- The HTML files are plain text, and you can open them in any text editor to inspect the code
