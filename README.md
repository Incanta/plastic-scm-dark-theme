# Montana Actually Dark PlasticSCM Theme

This is a prototype theme that is actually dark (and not just the side/top bars) for PlasticSCM on Windows. Many of the colors take inspiration from VSCode's Dark+ theme.

**NOTE:** This is not a complete theme. It only provides bits and pieces here to make my eyes not burn, and only covers my use cases. Want to contribute more languages? **PRs are more than welcome.**

## Installation

### Base Theme

You can easily install the theme by copying the `montana-actually-dark` folder and paste it in `C:\Program Files\PlasticSCM5\theme\windows`. Restart PlasticSCM, and it will be available in the Preferences as `Montana Actually Dark`, and then restart again to see the effects.

### Syntax Highlighting

When viewing code in the viewer, the syntax is colored based on non-themeable colors. This means you'll be overwriting the syntax highlight colors for the language for all themes by installing this. **NOTE:** We recommend that you backup the original files to prevent if you ever need to revert changes.

To install each language, copy each `*.langdef` file in the `syntaxhighlightlanguages` folder and paste them `C:\Program Files\PlasticSCM5\client\syntaxhighlightlanguages`, replacing the current contents. Restart PlasticSCM to have the changes reflected.

Languages supported:
- C++ (C/C# seem to be working as well)

## Making Changes

You can make changes to colors for the theme in `montana-actually-dark/colors/colors.conf`. Finding the variable you're interested in is a trial-by-error task of changing colors for some variables to see if the change was made (I usually use `Green`, `Orange`, `Red` as stark colors to help identify variables).

To make changes to syntax highlighting, you can add/change `ClassificationType` nodes in the `LanguageDefinition.ClassificationTypes` node using the `DefaultStyle` variable. The `Key` node relates to `TokenKey` references found within the `LanguageDefinition.Lexer` node.

**You must restart SCM to see the changes take effect for both cases.**
