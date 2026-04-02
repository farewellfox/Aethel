# Aethel Apps

A pair of web apps for the **Aethel** tabletop RPG system.

---

## Apps

**[Aethel Character Sheet](https://farewellfox.github.io/Aethel/aethel-character-sheet.html)**
Full digital character sheet with live calculations and level tracking.

**[Pasqually's Spell Slinger](https://farewellfox.github.io/Aethel/pasqually-spell-slinger.html)**
Spell builder and library for The Mind and The Spirit classes.

Open either link in your browser. No download or installation required.

---

## Aethel Character Sheet

### Getting Started

1. Enter your ability scores first — modifiers, saving throws, and skill totals calculate automatically
2. Fill in your identity fields (name, species, class, archetype, background, alignment)
3. Open the **Level Log** tab and add your starting level. Character level on the sheet is driven by the log, not a manual field
4. Add your actions, reactions, and passives in the **Actions** section
5. Use **Ctrl+S** (or the Save button) to export your sheet as a `.json` file

---

### Tabs

#### Character Sheet

The main tab. Contains:

**Identity** — name, species, class, archetype, background, alignment, and level (derived from the Level Log).

**Ability Scores** — enter raw scores; modifiers calculate automatically and feed everything else.

**Combat Stats** — four panels:

- *Saving Throws* — Fortitude, Reflex, and Will calculate live. Reflex and Will automatically use whichever of their two governing stats is higher and label which one they're using
- *Offense* — Initiative, Attack Bonus, Spell Save DC (8 + ⌈level ÷ 2⌉ + governing mod; defaults to INT, switchable to WIS or CHA via dropdown), and a manual Defense field
- *Defense* — manual entry; the Inventory tab calculates a suggested value based on equipped gear
- *HP & Resource* — tracks current and max HP, and your class resource (AP / FP / RP, labelled automatically based on your class entry). Short Rest and Long Rest buttons are available here

**Skills** — shows points available, points spent, and remaining. Each skill displays its total bonus (points + ability modifier). Skills exceeding the cap for your current level are flagged in red. Skill cap is based on level and enforced as a visual warning — no cheating.

**Actions** — four categorized tables: Actions, Reactions, Bonus Actions, and Passives. Each entry is created through a modal with fields for:
- Name and range
- Action type and usage limit (no limit, per combat, per short rest, per long rest, daily)
- Optional resource cost (AP / FP / RP, or a custom resource)
- Effects: damage (with dice and type), healing, conditions (Basic / Advanced / Expert tier), and freeform "other"
- Resolution type: attack roll or saving throw, with modifier and DC configuration
- Trigger (for reactions), duration, spell form, spell augments, and notes

Action cards display a summary of all configured fields and auto-calculate attack bonuses and spell save DCs from your current ability scores.

**Import from Spell Slinger** — the Actions section has an "↑ Import Library" button. Load a Spell Slinger `.json` export and select which spells to add to your actions. Each spell maps automatically to an action entry with its form, augments, damage, and conditions pre-filled, with a review step before committing.

**Daily Archetype Ability** — a hex toggle to mark your daily ability as used. Resets on long rest.

---

#### Features

An automatically compiled reference list of all class features and abilities added across your level log entries. Sortable by name, source, or level gained. Read-only — features are added and managed through the Level Log.

---

#### Inventory

Six collapsible sections:

- **Armor & Shields** — track armor type, value, and DEX bonus eligibility; equip one armor and one shield at a time. The section calculates and displays your Suggested Defense Score based on equipped items and your DEX modifier, which you then enter manually on the Character Sheet tab
- **Weapons** — name, damage dice, damage type, properties
- **Consumables** — name, effect, quantity with +/− controls
- **Adventuring Gear** — name, quantity, notes
- **Magic Items** — name, rarity, attunement, description
- **Currency** — Gold, Silver, and Copper fields

---

#### Level Log

Add one entry per level gained. Each entry tracks:

- HP gained at that level
- Features and abilities unlocked (pulled into the Features tab)
- Skill point allocation per skill for that level
- Free-form notes
- Skill investment notes (e.g. "2 Arcana, 1 Lore")

The log enforces the correct skill point budget per level based on your INT modifier. Delete any entry to correct a mistake — entries renumber automatically.

---

#### Notes & Lore

**Proficiencies & Training** — structured tracking for four categories, each displayed as a chip list:

- Armor
- Weapons
- Tools
- Languages — includes an optional fluency tier (Native, Fluent, Conversational, Basic, Script Only) displayed as a badge on each chip

Add entries via the inline input fields; remove them with the ✕ on each chip. Proficiency data is stored separately from the rest of the sheet.

**Lore & Notes** — seven free-label text boxes for anything else: faction standing, retainer info, backstory, world notes, session reminders, etc. Labels are editable.

---

#### Cheat Sheet

Quick in-session reference covering attack rolls, advantage and disadvantage, critical hits, defense score, skill check DCs, resting rules, and condition tiers (Basic, Advanced, Expert).

---

### Saving & Loading

- **Ctrl+S** or the **Save** button exports a `.json` file containing all sheet data including actions, inventory, level log, notes, and proficiencies
- **Load** imports a `.json` file — useful for moving between devices or sharing with your GM
- Data also persists automatically in browser `localStorage` between sessions on the same device and browser
- Proficiency data (`aethel-proficiencies-v1`) is stored separately in `localStorage` and does not require a manual save to persist locally, but is not included in the exported `.json` — back up by keeping your export current

> Local storage is per browser, per device. Use Save / Load to move between machines.

---

## Pasqually's Spell Slinger

A spell builder and library for **The Mind** and **The Spirit** classes.

---

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
