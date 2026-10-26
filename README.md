# Contriviewer

Contriviewer helps you review your code editing activity and agent use in Visual Studio Code.

## What it shows

- **Edit Sessions**: summarizes edits between file saves as User, Assisted, Agent or Unknown.
- **Changed Characters**: shows the volume of inserted and deleted characters in each category.
- **Retained File Contribution**: shows the estimated contribution to the text currently in each file.
- **Commit Contribution**: shows contribution associated with changes recorded in Git commits.

Categories are estimates based on information available from VS Code and supported tools. Classifications and ratios may be refined when related information arrives later.

## Install and get started

Requires VS Code **1.102.0 or later**.

1. Download `contriviewer-<version>.vsix` from [Releases](https://github.com/seoultech-selab/contriviewer/releases).
2. Run **Extensions: Install from VSIX...** in the VS Code Command Palette and select the file.
3. Open your project folder. Recording starts automatically when a workspace is open.
4. Select the **Contriviewer** icon in the Activity Bar to open the Overview.

## Export your records

Run **Contriviewer: Export Collected Data** to save your records as a compressed `.tar.gz` archive at a location you choose. Each archive contains the cumulative history from the start of recording through that snapshot. Exporting does not clear your local records or upload the archive to a server.

Export archives include recorded edit text and may contain sensitive information, including text that was later deleted or undone. Store them privately and follow the precautions below. See the user manuals for detailed instructions.

## User manuals

The PDF manuals provide detailed usage instructions, including installation, displayed values, local storage and troubleshooting.

- [English user guide (PDF)](https://github.com/seoultech-selab/contriviewer/blob/main/output/pdf/Contriviewer_User_Guide_en.pdf)
- [Korean user guide (PDF)](https://github.com/seoultech-selab/contriviewer/blob/main/output/pdf/Contriviewer_User_Guide_ko.pdf)

Version-specific PDF manuals are also attached to each [Release](https://github.com/seoultech-selab/contriviewer/releases).

## Records and privacy

Records stay on your computer. The extension does not upload them to a server.

Edit records include **the exact text inserted and deleted**. Text that was never committed to Git, or was later deleted or undone, may remain in records and cumulative Exports. Proposed changes from supported agents may also be recorded even if you do not apply them. Clipboard text may be checked transiently to recognize a paste operation, but is not stored as a separate clipboard field.

Do not enter real passwords, API keys or personal information into monitored files. Do not post record directories or Export archives in public repositories or public issues. Use one VS Code window for a given physical project folder.

## Report a bug or suggest an improvement

Open an [issue](https://github.com/seoultech-selab/contriviewer/issues) with the extension version, VS Code version, operating system, steps to reproduce and expected result. You do not need to attach project source code or a complete Export archive.

This repository provides downloads, user manuals and a place for feedback. Development source is maintained separately.
