![image](https://github.com/Rilichime/Planet-Zoo-Genetics-Manager/blob/main/banner.png?raw=true)

A desktop tool for managing and breeding animals in **Planet Zoo** using save-file genetics data. Made using Devin and Kimi K2.7. 

![Python version](https://img.shields.io/badge/python-3.9+-blue.svg)

## What it does

ZooGeneticsManager reads your Planet Zoo `.zoo` save files and gives you a clean, searchable interface for:

- Browsing every animal in your Franchise zoos by species
- Viewing each animal's Size, Longevity, Fertility, Immunity, and hidden coat genes
- Filtering by name, sex, stats, color morph, notes, and ID
- Getting pairing suggestions ranked by primary stats or by perfect secondary stats
- Comparing a chosen male/female pair to preview expected offspring stats
- Tracking extra per-animal info such as price, seller, color notes, and genealogy
- Preventing accidental inbreeding based on mother/father records


## Screenshots
 
<details>
<summary>Click to expand</summary>

![image](https://github.com/Rilichime/Planet-Zoo-Genetics-Manager/blob/main/Screenshot01.png?raw=true)

![image](https://github.com/Rilichime/Planet-Zoo-Genetics-Manager/blob/main/Screenshot02.png?raw=true)

</details>

## Quick start

1. Make sure you have Python 3.9+ installed. You can download the installer for Python here.
   https://www.python.org/downloads/
3. Download the  `Planet.Zoo.Genetics.Manager.zip` folder from the most recent release here.
   https://github.com/Rilichime/Planet-Zoo-Genetics-Manager/releases
5. Run the program `ZooGeneticsManager.pyw`  (open in Python)

6. Copy a Planet Zoo `.zoo` save file into the folder where this program is located. You can usually find this at:

`Users\(your username here)\Saved Games\Frontier Developments\Planet Zoo\(your steam ID)\Saves`

Sort files by Date Modified and select the most recent `.zoo` file listed there. This will be the save file of your last saved zoo. The file name will be a bunch of random letters/numbers. Copy that `.zoo` file to the folder this program is in.

5.  Click **Open .zoo file** and select a save.

6.  You can also merge additional saves with **File > Add Save**, which is useful if you have animals across multiple Franchise zoos.

7. You're done! All animals should be accounted for by the program, just select a species from the drop-down to view them.

## Main tabs

| Tab | Purpose |
|-----|---------|
| **Individuals** | List every animal of the selected species. Double-click any cell to copy it. |
| **Primary Stats** | Pairings that prioritize better Size/Longevity outcomes. |
| **Secondary Stats** | Pairings that prioritize perfect Fertility/Immunity outcomes. |
| **Tips** | Built-in usage reminders and hotkey info. |

## Side panel (Filters / Notes / Compare)

- **Filters** — narrow down the Individuals list and pairing suggestions.
- **Notes** — edit per-animal records. Includes a **Genealogy** section for Mother and Father.
- **Compare** — inspect the expected outcome of a chosen male/female pair.

## Hotkeys

| Key | Action |
|-----|--------|
| `1` / `2` / `3` | Switch between Individuals, Primary Stats, and Secondary Stats |
| `F` | Open the **Filters** side tab |
| `N` | Open the **Notes** side tab |
| `C` | Open the **Compare** side tab |

Hotkeys are ignored while you are typing in a notes or filter field.

## Features in detail

### Pairing suggestions

Primary Stats ranks pairs by their expected Size/Longevity outcomes. Secondary Stats ranks pairs by their expected Fertility/Immunity outcomes, favoring perfect secondary stats.

Use the **Min Prob** filter to hide pairings below your desired success chance.

### Color morph tracking

Color morphs are not automatically read from the save file. You can set them manually per animal in the Notes panel or with the **ColorMorph** filter controls. The program supports species-specific morph names such as Leucistic, Melanistic, Albino, and others.

### Genealogy and inbreeding prevention

In the **Genealogy** section of the Notes panel, you can record each animal's mother and father. The **Prevent Inbreeding** checkbox then filters out pairings that would match siblings or parent/child pairs.

- Enter the parent **ID** when you know it for the most accurate matching.
- A **name** also works; however, animals that share the same name will be treated as the same individual.
- Use **Bulk Set Parents...** to apply the same mother/father to many selected animals at once.

### Monogamy Lock, Release, and Perfect highlights

- **Monogamy Lock** restricts an animal to only its chosen mate.
- **Highlight Release** flags animals you may want to release.
- **Highlight Perfect** flags animals that already have perfect stats.

## Data files

The program creates two local files next to the script:

- `ZooGeneticsManager_data.json` — your per-animal notes, color morphs, and mate locks.
- `ZooGeneticsManager_settings.json` — recent files and window settings.

These files are safe to back up or move with the program.

## Notes and limitations

- The parser reads the compressed `parkdata` inside `.zoo` files. Scenario mode is not supported.
- Some animals may share the same in-game ID; this is rare, but it happens. The program removes duplicates by `AnimalId` so on occasion it will accidentally remove a non-duplicate animal because it shares an AnimalID.
- Color morphs must be input manually, as the save file does not expose them as plain text.

## License

This project is released under **The Unlicense**. See `LICENSE` for the full text.
TLDR this is open-source, do whatever you want with the code and program, I don't care.
