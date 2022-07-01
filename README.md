# Wikitext Snippets
This is a file used for Frederisk's VS Code [Wikitext extension](https://github.com/Frederisk/Wikitext-VSCode-Extension) to provide autocompletes when writing Wiktionary entries.
It is made for my own purposes, but it also has various utilities for writing out common templates in a typical Wiktionary editor's work cycle.
Though it is currently quite minimal, I hope to augment it with further snippets in the future.

## Using
The usage will likely differ by platform, but follows this process: 
- Find where the Wikitext VS Code extension folder is;
- Replace the resident `snippets.json` file under the `snippets` directory with this one
... and your autocompletes will match mine.

This allows you to type e.g. `@ux`, and it will expand to `#: {{ux|lang|text|translation}}`,
with the `#:` prepended on purpose, as this is the most likely way to use the `{{ux}}` template. Similar rules for e.g. `@syn`. The extension also allows
snippets to contain user-defined parameters, e.g. in `#: {{ux|${1:lang}|${2:text}|${3:translation}}}`: this will place your cursor at 1, and once you type
whatever the parameter is supposed to represent (e.g. I type "de" into the `lang` field), pressing tab will move on to the next one, until all fields
are exhausted and it puts the cursor after the end of the entire snippet.
This function is very efficient for editing as it allows you to type in only the important parts, and save writing all the boilerplate every single time.
