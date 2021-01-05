---
package_name: "ahkAutoCorrectList"
package_title: "Auto correct list from AutoHotkey"
package_desc: "A package to do auto correction of common English language mis-spellings. Adapted from http://www.biancolo.com/blog/autocorrect/. Also includes the regex needed to convert ahk hotstrings to work in espanso."
package_version: "0.1.0"
package_author: "Clancey"
package_repo: "https://github.com/cmcneal/espanso-autocorrect-package"
---
A package to do auto correction of common English language mis-spellings. Adapted from http://www.biancolo.com/blog/autocorrect/. Also includes the regex needed to convert ahk hotstrings to work in espanso.


To convert an ahk hotkey list to espanso in Codium (VSCode)
# First, move any trailing comments to the previous line
  - find: `^(.*)\s{1,}(;.*)$`
  - replace: `\t$2\n$1`
# Second, setup the triggers
  - find: `^:.{0,1}:(.*)::(.*)$`
  - replace: `\t- trigger: "$1"\n\t\treplace: "$2"\n`
