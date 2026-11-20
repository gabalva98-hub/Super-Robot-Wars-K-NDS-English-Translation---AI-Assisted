# Super Robot Wars K — English Fan Translation

An unofficial, free English fan translation of **Super Robot Wars K** for the Nintendo DS, presented by **Gyasuke & Wakabayashy Workshop**.

The translation is distributed through an **offline HTML patcher**. No game ROM is included: you must supply your own clean Japanese game dump.

**Patch version:** 0.9.1 (ASCII V40 — full battle-text test build)  
**Last updated:** November 18, 2026  
**Language:** English  
**Status:** Test release — the latest battle-text changes still need in-game validation.

## What's included

- English story translation and editorial text reflow across scenario banks CH001–065.
- Native **one-byte ASCII text handling**, alongside the project's variable-width font (VWF), revised Latin glyphs and punctuation.
- Expanded story-text buffers, improved wrapping, and fixes for dialogue boxes, interface alignment and text rendering.
- Expanded names for weapons, mecha and pilots, replacing many unnecessarily abbreviated labels where their display fields allow it.
- Expanded English names and descriptions for **35 pilot skills** and **80 special mecha systems/abilities**.
- Expanded descriptions for **all 35 Spirit Commands**, while retaining their existing names, costs, icons and order.
- One-byte storage for compatible characters in all **210 battle-text banks**, reducing the space required by the battle-text data.
- A full review of **20,994 battle-text entries**, with **4,499 entries restored, expanded or reflowed** across 191 banks in the latest test build. The build contains **559 three-line battle entries** in total.
- Preserved dynamic commands, speaker order and battle controls. **49 entries with incompatible dynamic-command sequences were deliberately left unchanged** rather than risking broken in-game variables or scripts.
- Earlier dialogue, character-name, shop, Pair Up, save-screen and chapter-title punctuation corrections.
- Earlier P19 safety adjustments for dynamic markers across **495 story dialogue boxes in 48 banks**.
- English labels for **87 terrain and location types across 227 records**, with compact forms where space remains limited.
- Earlier repairs to **18 battle-effect labels**, plus an adjusted Sortie Will heading.
- An ending graphic reading **“Thanks for playing”** on its first line.
- Stargazer's six support quotes arranged on one line, including quotes addressed to Sven/Noir.
- A corrected workshop logo and an offline English patcher interface. Your ROM is processed locally; it does not need to be uploaded to a server.

**Note:** More compact names and some short interface labels remain where a full spelling would overflow the actual on-screen field. The one-byte encoding does not remove screen-width limits.

## What's new in 0.9.1

This version incorporates the ASCII improvements developed through V37–V40:

- **ASCII V35:** expanded numerous weapon, unit and pilot names.
- **ASCII V36:** expanded pilot-skill and special-mecha-ability text.
- **ASCII V37:** expanded the 35 Spirit Command descriptions.
- **ASCII V38:** converted compatible battle text to one-byte storage, without changing the meaning of the decoded dialogue. The new storage format was successfully tested by the project owner with attacks involving **King Gainer** and **Murasame Liger**.
- **ASCII V39–V40:** began restoring combat dialogue that had previously been shortened because of text-space restrictions. V40 extends the revision across the complete battle archive rather than a small set of isolated examples.

The V40 battle archive is **1,087,643 bytes**, compared with **1,436,577 bytes** in V37. This is a **348,934-byte reduction**, even after the dialogue expansions.

The battle-text changes in this build have passed structural checks, including pointer ranges, preserved control sequences and exact patch-output reconstruction. **They have not yet passed full emulator, visual or hardware testing.** Restored lines from an earlier English master also need additional contextual editorial review.

## Installation

1. **Back up** your original Japanese `.nds` file and any existing `.sav` file.
2. Download the **0.9.1 / ASCII V40** offline HTML patcher.
3. Open the `.html` file in a compatible browser on your computer or Android device.
4. Select your **clean, unmodified Japanese Super Robot Wars K ROM** (`.nds`).
5. Use the patcher's **Verify ROM and apply patch** option.
6. Save the generated English-patched `.nds` file and open it in your compatible emulator or on your own hardware.
7. To continue an existing save, keep a backup. Where required by your emulator or flashcart, make sure the `.nds` and `.sav` files share the same base filename.

**Important:** The patcher is cumulative. Always start from the original Japanese ROM; **do not apply it over a previously patched V37, V38, V39 or older ROM**. Do not combine different patch versions.

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

### Expected 0.9.1 / V40 result

| Property | Value |
| --- | --- |
| Suggested filename | `Super_Robot_Wars_K_EN_0.9.1.nds` |
| SHA-256 | `8eb7843b72449cb96d669573011b3123b1b3adc3c6d80bb8767ae98c4a7b6d1a` |

The suggested filename is only a label; the SHA-256 identifies the expected patched ROM. The patcher was independently checked to reproduce this output byte for byte from the verified Japanese source.

## Testing and project status

**Full-playthrough tester: Ziegfried**

Ziegfried completed an earlier build of the translation, taking these routes:

- Berlin
- Build Base
- Archangel
- Tatsumiya Island

Many thanks to Ziegfried for completing a playthrough and helping test the translation. Other testers have worked on other routes. A full playthrough of an **earlier build** does **not** establish that the latest 0.9.1 changes, all route combinations or optional events are free of issues.

### Validation of the latest changes

- **V38:** the project owner confirmed successful attacks with **King Gainer** and **Murasame Liger**, providing a limited gameplay check for the new battle-text storage.
- **V39:** 110 three-line dialogue restorations passed structural checks; gameplay testing was not confirmed.
- **V40 / 0.9.1:** all 210 combat banks and 20,994 entries were audited, 4,499 entries were expanded or repaired, and the resulting patch was reconstructed and verified exactly. **In-game testing of this specific build is still pending.**

For testing 0.9.1, please try attacks, counterattacks, defenses, support actions and battles involving different series. Pay particular attention to long two- and three-line messages, speaker or portrait changes, voice-related effects, transitions to shorter messages, and the return to the map. Repeating the King Gainer and Murasame Liger tests is especially helpful for checking regressions.

## Known limitations and bug reports

- Some expanded battle dialogue may overflow or display incorrectly until visually verified in-game. **The maximum tested reconstruction format is three lines, not a guarantee of correct display in every battle.**
- The **49 dynamic-command entries** mentioned above remain unchanged pending investigation of their functions.
- The restored combat text comes partly from an earlier English translation master and still needs further contextual and terminology auditing.
- Some pilot-skill labels, weapons, units and other interface fields must remain abbreviated because of their available pixel width.
- Previously reported Sortie-alignment, punctuation and portrait/speaker issues should still be checked for regressions; do not assume that the new ASCII work fixes all of them.
- Three proper terrain/location labels were previously reported as untranslated; these have not been confirmed resolved in this build.
- The earlier Stargazer support-portrait issue, as well as terrain, battle-effect and ending-graphic fixes, still benefit from targeted visual checks.
- Untested routes, optional scenes, save states and different emulators or hardware configurations can reveal additional problems.

If you encounter a crash, clipped text, a broken portrait, missing dialogue or an interface issue, please open an issue in the GitLab project and include, if possible:

- The **patch version (0.9.1)** and your emulator or hardware.
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

A huge thank you to all testers for their time, dedication, feedback and bug reports. Your help locating graphical issues, dialogue problems, crashes and hardware-specific behavior has been essential to improving this translation.

## Legal notice and distribution

This is an **unofficial, non-commercial fan translation**. It is not affiliated with, sponsored by or endorsed by Bandai Namco or the original rights holders. All original game content, trademarks and characters remain the property of their respective owners.

**The patch is free. It must not be sold or placed behind a paywall.** If you paid someone for this patch, that payment was not authorized by this project.

No game ROM or BIOS is distributed here. You are responsible for obtaining and using your own game files in accordance with applicable laws.

---

Thank you for playing **Super Robot Wars K** in English!
