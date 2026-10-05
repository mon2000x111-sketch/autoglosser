 # autoglosser

## Try it out

### Web

Visit the following page: https://cicadacinema.github.io/autoglosser/ .

### Windows

Visit the following page: https://github.com/CicadaCinema/autoglosser/actions/workflows/auto-build.yaml .

Click on the latest (top-most) entry with a checkmark.

Click on either 'windows_msix' to download the MSIX installer (recommended, supported on [Windows 10 version 1709 and later](https://learn.microsoft.com/en-us/windows/msix/supported-platforms)) or 'windows_exe' to download the executable program file.

## Changes to savefile formats `.agmap` and `.agtext`

- [9629ea7](https://github.com/CicadaCinema/autoglosser/commit/9629ea7f52891c13d46906127f94711f10ffa0ae) introduced a change which stopped saving the `FullMap._sourceToMappings` field in the `.agmap` savefile. You can load old savefiles into the new version but you cannot load new savefiles into the old version.
- [d5561a7](https://github.com/CicadaCinema/autoglosser/commit/d5561a762b49840006d57da4b7cfc6b8aa9c9b28) introduced a change which relies on the fact that the mappings are sorted alphabetically by pronunciation in their map section during the runtime of the program. As a temporary measure, any imported maps are sorted beforehand. Therefore you can both load old savefiles into the new version and load new savefiles into the old version.
- [9c94e81](https://github.com/CicadaCinema/autoglosser/commit/9c94e81315ee1aca9ef2f9eb496e3ad8cbf6c2bc) modified the sorting order introduced in the change above.
- [71e70e8](https://github.com/CicadaCinema/autoglosser/commit/71e70e8a91fce41ad6b8acf0f6168144ac7c2102) modified the sorting order again.

## Usage

- When saving an `.agtext` or an `.agmap`, you cannot overwrite files. Autoglosser will display no error, but the old file will not be overwritten and the new file will not be saved anywhere.
- In Map mode, press enter to save the modification you have made to a mapping.

## Feature list

- [x] saving/loading translations as JSON
- [x] saving/loading maps as JSON
- [x] importing a text file string into translation mode
- [x] splitting/combining words
- [ ] ignoring punctuation
- [x] adding glosses/translations to individual words in translation mode
- [x] editing chunk translations
- [x] adding words to a gloss dictionary
- [x] gloss dictionary remains sorted
- [x] using the gloss dictionary to gloss a word
