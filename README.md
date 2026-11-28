# Super Robot Wars K — English Fan Translation

An unofficial, free English fan translation of **Super Robot Wars K** for the Nintendo DS, presented by **Gyasuke & Wakabayashy Workshop**.

The translation is distributed through an **offline HTML patcher**. No game ROM is included: you must supply your own clean Japanese game dump.

**Patch version:** 0.9.2F (V99)  
**Last updated:** November 27, 2026  
**Language:** English  
**Status:** V99 passed static verification. The affected animation still needs an in-game check.

## Original game bug fixed in 0.9.2F

In one battle pose, an arm segment was drawn over the mecha's chest, making it look as though an extra arm was coming out of the torso. We reproduced the pose from the clean Japanese ROM and confirmed that it used the same sprite order as V97. V98 moved the main arm segment behind the torso. V99 corrected the draw order of the three remaining pieces that still overlapped the chest. The reconstructed pose preserves the original silhouette.

## What's included

- English story translation and editorial text reflow across scenario banks CH001–065.
- Native **one-byte ASCII text handling**, alongside the project's variable-width font (VWF), revised Latin glyphs and punctuation.
- Expanded story-text buffers, improved wrapping, and fixes for dialogue boxes, interface alignment and text rendering.
- Expanded names for weapons, mecha and pilots, replacing many unnecessarily abbreviated labels where their display fields allow it.
- Expanded English names and descriptions for **35 pilot skills** and **80 special mecha systems/abilities**.
- Expanded descriptions for **all 35 Spirit Commands**, while retaining their existing names, costs, icons and order.
- One-byte storage for compatible characters in all **210 battle-text banks**, reducing the space required by the battle-text data.
- A sequential editorial pass through all **210 battle-text banks / 20,994 entries**, with contextual revisions, punctuation and reflow based on the Japanese dialogue. The latest editorial pass preserves the original line structure rather than targeting three-line expansions.
- Preserved battle controls and speaker assignments, repaired auxiliary speaker pointers, and restored **49 missing dynamic-name commands** during the V78 editorial pass. V95 additionally restores a missing dynamic-name call in Chaser Combo.
- Earlier dialogue, character-name, shop, Pair Up, save-screen and chapter-title punctuation corrections.
- Earlier P19 safety adjustments for dynamic markers across **495 story dialogue boxes in 48 banks**.
- English labels for **87 terrain and location types across 227 records**, with compact forms where space remains limited.
- Earlier repairs to **18 battle-effect labels**, plus an adjusted Sortie Will heading.
- An ending graphic reading **“Thanks for playing”** on its first line.
- Corrected support-attack speaker selection, including the reported King Gainer and Stargazer cases.
- A corrected workshop logo and an offline English patcher interface. Your ROM is processed locally; it does not need to be uploaded to a server.

**Note:** More compact names and some short interface labels remain where a full spelling would overflow the actual on-screen field. The one-byte encoding does not remove screen-width limits.

## Changes through 0.9.2 (V95)

This cumulative update incorporates the work through ASCII V95:

- **Combat engine (V41–V54):** moved away from experimental three-line expansions and repaired auxiliary battle-bank pointers responsible for incorrect support speakers, including the unexpected Kira portrait and empty dialogue box. Confirmed repeated successful support attacks with King Gainer and Stargazer on V54.
- **Battle dialogue (V55–V78):** completed the sequential editorial pass through the battle archive, restoring context, improving wording and punctuation, and preserving Japanese line counts and dynamic controls in the revised entries. V78 restored 49 previously missing dynamic-name commands.
- **Names and interface (V79–V86):** reviewed pilot, unit and weapon labels; corrected Favorite Series titles, keyboard buttons, Spirit menu labels, Groovine Buster, Suspage, and selected story dialogue. Shortened Daiya's Mother to Daiya's Mom and the affected Demon Beast battle-preview label to D. Beast. Corrected the Critical! graphic's map data.
- **List alignment and terrain (V87–V90):** adjusted the left margin of unit, pilot and weapon names; restored Unit Status and Pilot Status; standardized terrain abbreviations to A/L/W/S and terminology to Land and Water. Expanded selected Missile labels and corrected Athrun and Diana A dialogue references.
- **Deployment and system menus (V91–V92):** removed overlapping fragments beneath deployment labels; aligned Change BGM; corrected Shop headings, including Sell Parts; separated Stats and Now in Skill Parts.
- **Name entry (V93):** restored the original spacing of selectable characters in the rename keyboard without changing the side buttons or other interface text.
- **Chapter 5–6 feedback (V94):** corrected Gadved and Bachclone in story dialogue; adjusted Type and Terr field widths and the Hero Unit heading in Save Data.
- **Chaser Combo (V95):** restored Mist's missing response using Angelica's saved name ("Angelica!" with the default name). Verified the affected attack sequence in melonDS 1.1.

## What’s new in 0.9.2F (V96–V99)

- **V96:** corrected the Gadved nameplate, standardized Kizz Munt and Zonnet, and updated the Bachclone and Zonnet location labels. Fixed the hyphen in “top-class” during Chaser Combo. Translated the remaining Unit Bonus and Weapon Bonus options, updated the Range heading to Rng, and adjusted the EN label in Unit Upgrades.
- **V97:** updated Steel Jeeg's activation label to “Bronze Bell Power” and redrew it to fit the available width. Corrected the central reticle label in Angelica's attack from “SCHEISSE” to “SCHIEẞ”.
- **V98–V99:** corrected the sprite order in the affected battle pose from the original game.

## Installation

1. **Back up** your original Japanese `.nds` file and any existing `.sav` file.
2. Download the offline HTML patcher
3. Open the `.html` file in a compatible browser on your computer or Android device.
4. Select your **clean, unmodified Japanese Super Robot Wars K ROM** (`.nds`).
5. Use the patcher's **Verify ROM and apply patch** option.
6. Save the generated English-patched `.nds` file and open it in your compatible emulator or on your own hardware.
7. To continue an existing save, keep a backup. Where required by your emulator or flashcart, make sure the `.nds` and `.sav` files share the same base filename.

**Important:** The patcher is cumulative. Always start from the original Japanese ROM; **do not apply it over a previously patched ROM from any earlier release**. Do not combine different patch versions.

### Required ROM

The reference Japanese dump is:

| Property | Value |
| --- | --- |
| Filename/reference | `3535 - Super Robot Taisen K (JP)(XenoPhobia).nds` |
| Size | `67,108,864` bytes |
| CRC32 | `D16DB8AF` |
| SHA-256 | `f26e30b8b6c2f0b3f898d094a806ffaa2571f44b485760f88fd7949852e2f707` |

A second clean Japanese dump from an original cartridge has also been verified as compatible:

| Property | Value |
| --- | --- |
| Reference | `Super Robot Taisen K (Japan)` — cartridge dump |
| Size | `67,108,864` bytes |
| **CRC32** | **`5510236D`** |
| SHA-256 | `337f901f5d0efccdd3837f7b241a65c244f18a632327c2d60ff5f213107f11a6` |

These two verified Japanese dumps differ only in reserved header areas (`0x378–0x39F` and `0xF80–0xFFF`). After normalizing those areas, their game data match exactly. The patcher recognizes both verified sources. The filename itself may vary; use the patcher's verification function to confirm that your clean Japanese dump is compatible.

### Expected 0.9.2F (V99) result

| Property | Value |
| --- | --- |
| Output filename | `Super_Robot_Wars_K_EN_V99_TEST.nds` |
| Size | `64,871,340` bytes |
| CRC32 | `7A9C3F5C` |
| SHA-256 | `5dcd72c1a59e10f608d1e15c99a1af5575331707b1fb896ee967eba8955cca93` |

## Testing and project status

**Full-playthrough tester: Ziegfried**

Ziegfried completed an earlier build of the translation, taking these routes:

- Berlin
- Build Base
- Archangel
- Tatsumiya Island

Many thanks to Ziegfried for completing a playthrough and helping test the translation. Other testers have worked on other routes. The latest builds, alternate routes and optional events still need broader playthrough testing.

### Validation of the latest changes

- **V38:** the project owner confirmed successful attacks with King Gainer and Murasame Liger.
- **V54:** repeated King Gainer and Stargazer support tests were reported successful after the auxiliary-pointer repair.
- **V78:** all 210 banks and 20,994 battle entries were structurally audited; auxiliary speaker references and restored dynamic-name commands were checked.
- **V80–V93:** targeted melonDS 1.1 checks covered Spirit menu labels, unit/pilot/weapon lists, terrain indicators, deployment commands, System, Shop, Skill Parts and name entry. The keyboard spacing was checked against the Japanese game, including ABC/Sym, Hiragana and Kanji pages.
- **V94:** the story corrections passed decoding checks; visual confirmation of Type, Terr and Hero Unit adjustments is still pending.
- **V95:** melonDS 1.1 reproduced the Chaser Combo sequence from the tester's battery save. Mist's restored response displayed with the correct portrait, and the attack animation continued. The V95 patch was independently reconstructed using Python and JavaScript.

- **V96:** the rebuilt patch passed reconstruction checks. Visual checks of the updated bonus menus remain pending.
- **V97:** both updated graphics were inspected after decoding. Their in-game animations still need visual confirmation.
- **V99:** the patcher reproduced the expected ROM byte for byte. The reconstructed pose differed from the supplied reference by 7 visible pixels, down from 101 in V98, using a tolerance of two RGB levels. The animation still needs an in-game check.

Full-playthrough coverage applies to the earlier build described above. Please continue to test different routes, support combinations, dynamic names, battle transitions and menu screens.

## Known limitations and bug reports

- Some interface labels and names remain abbreviated because of their available pixel width.
- The small Spirit indicators below Sup retain single-letter labels; the proposed two-letter layout is not yet validated.
- Some earlier graphical fixes, including Critical! during live combat and specific nameplates, still require targeted regression checks. The earlier wedding-title layout report also remains open for verification.
- The full editorial and visual review of every battle and route is not yet certified.
- Untested routes, optional scenes, save states and different emulators or hardware configurations can reveal additional problems. Back up battery saves before upgrading; emulator save states may not be compatible across builds or emulator versions.

If you encounter a crash, clipped text, a broken portrait, missing dialogue or an interface issue, please open an issue in the GitLab project and include, if possible:

- The **patch version (0.9.2F / V99)** and your emulator or hardware.
- The **chapter, route, unit and action** involved (attack, counterattack, support, defense, etc.).
- The **last visible dialogue line** or a description of the affected screen.
- A screenshot or short video; for a crash, a diagnostic dump may also help.

Please back up your save before investigating an issue. **Do not upload copyrighted ROMs** in bug reports.

## Credits

- **Project and patch presentation:** Gyasuke & Wakabayashy Workshop

### Testers

- **Theoldnile**
- **Maxcore**
- **Rowlet3196**
- **FeatheredFaye**
- **Ziegfried** — Completed a full playthrough covering the Berlin, Build Base, Archangel and Tatsumiya Island routes.
- **FieryBlitz** — Detailed interface feedback, consistency checks and bug reports.

A huge thank you to all testers for their time, dedication, feedback and bug reports. Your help locating graphical issues, dialogue problems, crashes and hardware-specific behavior has been essential to improving this translation.

## Legal notice and distribution

This is an **unofficial, non-commercial fan translation**. It is not affiliated with, sponsored by or endorsed by Bandai Namco or the original rights holders. All original game content, trademarks and characters remain the property of their respective owners.

**The patch is free. It must not be sold or placed behind a paywall.** If you paid someone for this patch, that payment was not authorized by this project.

No game ROM or BIOS is distributed here. You are responsible for obtaining and using your own game files in accordance with applicable laws.

---

Thank you for playing **Super Robot Wars K** in English!
