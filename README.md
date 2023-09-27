![](https://img.shields.io/github/license/alangrainger/obsidian-share) ![](https://img.shields.io/github/v/release/alangrainger/obsidian-share?style=flat-square) ![](https://img.shields.io/github/downloads/alangrainger/obsidian-share/total)

# Share Note

Free, encrypted public note sharing for Obsidian. Notes are encrypted on your device before being sent to the server, and the decryption key is never sent to the server - it only exists inside the note in your vault.

## Features

- Uploads using your current theme.
- Local and remote image support.
- Supports anything that Obsidian Preview mode does, like rendered Dataview queries and any custom CSS you might have enabled.
- Supports callouts with full styling.
- If your shared note links to another note which is also shared, that link will also function on the public page.
- Frontmatter is stripped on upload by default to avoid leaking unwanted data.

## Encryption

- Your notes are encrypted on your device with a key that only you have.
- Each note is encrypted with its own random key. A key from one of your notes cannot be used to decrypt another of your notes.
- The key is never sent to the server, it only exists as part of the share link created inside your device.

## Installation

The plugin is awaiting review for the Community store. In the meantime you can install it using BRAT, [see the instructions here](docs/BRAT.md).

Once you've installed the plugin, enable it by clicking the "Connect plugin" button on the Settings page.

## Usage

Use the `Share Note` command from the Command Palette. You can map it to a hotkey to make things faster.

The first time a file is shared, the plugin will automatically upload all your theme styles. The next time you share a file, it will use the previously uploaded theme files. 

If you want to force the theme CSS to update, use the command `Force re-upload of all data for this note`.

### Sharing a note unencrypted

If you want to share a note without any encryption, you can set a frontmatter checkbox property:

`share_unencrypted` = true

## Troubleshooting

If your shared note isn't displaying correctly, before creating an Issue try these steps first:

1. Change to Reading mode.
2. Scroll to the top of the note.
3. Use the command `Force re-upload of all data for this note`.
4. Refresh the shared note a few times to make sure you're seeing the latest copy rather than a cached copy.

And see if that gets the note to share correctly.

### MathJax / LaTeX

If your MathJax / LaTeX elements are not displaying correctly, `Force re-upload` the note which is having the issues to force your custom stylesheet to be rebuilt with the MathJax classes included.

## Running your own server

[See the docs here](docs/Running%20your%20own%20server.md).

## Attributions

Encryption code is based with thanks on code from https://github.com/mcndt/obsidian-quickshare
