# **Split HTML Attributes (Vue, React, Angular)** - VSCode Extension <!-- omit in toc -->

[![Inline (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/dannyconnell.split-html-attributes.svg?color=1B7D91&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=dannyconnell.split-html-attributes)
[![Inline (VSCode extension) installs badge](https://vsmarketplacebadge.apphb.com/installs-short/dannyconnell.split-html-attributes.svg?color=1B7D91)](https://marketplace.visualstudio.com/items?itemName=dannyconnell.split-html-attributes)
[![Inline (VSCode extension) rating badge](https://vsmarketplacebadge.apphb.com/rating-short/dannyconnell.split-html-attributes.svg?color=1B7D91)](https://marketplace.visualstudio.com/items?itemName=dannyconnell.split-html-attributes&ssr=false#review-details)

Tired of manually splitting your HTML attributes (or ![Vue.js](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/Vue.png "Vue.js") / ![React](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/React.png "React") / ![Angular](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/Angular.png "Angular") directives & props) up onto multiple lines? 

You can now do it **instantly** with this extension:

![Demo](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoSelfClosing.gif)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

Created by Danny, from [Make Apps with Danny (YouTube Channel)](https://dannys.link/youtube "Make Apps with Danny (YouTube Channel)"):

[![MakeAppsWithDanny](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/MakeAppsWithDannyYouTube.jpg)](https://dannys.link/youtube "Make Apps with Danny (YouTube Channel)")

## Contents <!-- omit in toc -->

- [Support](#support)
- [Features](#features)
  - [Opening Tags](#opening-tags)
  - [Self-Closing Tags](#self-closing-tags)
  - [Multiple Selections](#multiple-selections)
  - [Closing Bracket on New Line](#closing-bracket-on-new-line)
  - [Ordering](#ordering)
  - [Unsplit Attributes](#unsplit-attributes)
- [Usage](#usage)
- [Extension Settings](#extension-settings)
  - [Settings](#settings)
  - [Keybindings](#keybindings)
- [Don't Forget...](#dont-forget)
- [Known Issues](#known-issues)
- [Change Log](#change-log)
- [My Other VSCode Extensions](#my-other-vscode-extensions)

## Support

Find this extension useful? Please support it by leaving a review:

[![LeaveAReview](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/ButtonLeaveAReview.png)](https://marketplace.visualstudio.com/items?itemName=dannyconnell.split-html-attributes&ssr=false#review-details "Leave a review")

## Features

### Opening Tags

The extension works on opening tags:

![OpeningTags](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoOpeningTags.gif)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

### Self-Closing Tags

As well as self-closing tags:

![SelfClosingTags](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoSelfClosing.gif)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

### Multiple Selections

And even works with multiple selections:

![MultipleSelections](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoMultipleSelections.gif)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

### Closing Bracket on New Line

You can choose whether to place your closing bracket (`>` or `/>`) on a new line or not:

![DemoClosingBracket](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoClosingBracket.png)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

### Ordering

You can set the sort order for your attributes. For example, as a **Vue.js** developer, you can make sure your important Vue directives & handlers come first:

![AttributeSorting](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoAttributeSorting.png)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

### Unsplit Attributes

If you trigger the extension on an opening (or self-closing) tag that's already split, it will unsplit it back onto a single line:

![Unsplit](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoUnsplit.gif)
<br><small>*Theme: [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")*</small>

## Usage

Just select your opening (or self-closing) tag - from the opening angle bracket (`<`) up to the closing angle bracket (`>`) and either:
* Open Command Pallette (`CMD/CTRL + Shift + P`) and choose `Split HTML Attributes`
* Or use the keyboard shortcut (which defaults to `Ctrl + Alt + Shift + A`)

## Extension Settings

### Settings

| Setting | Default | Type |
| - | - | - |
| **tabSize**<br><small>`splitHTMLAttributes.tabSize`</small><br><br>Set the indentation size for your split lines. | `2` | Number
| **useSpacesForTabs**<br><small>`splitHTMLAttributes.useSpacesForTabs`</small><br><br>Use spaces for indentation (instead of tabs). | `true` | Boolean
| **closingBracketOnNewLine**<br><small>`splitHTMLAttributes.closingBracketOnNewLine`</small><br><br>Place closing bracket (`>` or `/>`) on a new line.| `false` | Boolean
| **sortOrder**<br><small>`splitHTMLAttributes.sortOrder`</small><br><br>Preferred sort order of attributes.<br>Can be an array of strings or regex.<br>A typical setting for Vue.js development might be:<br>`["^v-if", "^v-else", "^v-show", "^v-model", "^v-for", "^:key", "^key", "^v-", "^:", "^@click", "^@", "^id", "^class", "^.*=\""]`<br>Which would sort your attributes like so:<br>![AttributeSorting](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/DemoAttributeSorting.png) | `[]` | Array

### Keybindings

You can change the keyboard shorcut. This is the default:

```json
{
  "command": "extension.splitHTMLAttributes",
  "key": "ctrl+alt+shift+a"
}
```

## Don't Forget...

If you find this extension useful, please support it by leaving a review:

[![LeaveAReview](https://github.com/dannyconnell/vscode-split-html-attributes/raw/master/./images/ButtonLeaveAReview.png)](https://marketplace.visualstudio.com/items?itemName=dannyconnell.split-html-attributes&ssr=false#review-details "Leave a review")

## Known Issues

No known issues yet.

## Change Log

[View the Change Log here](https://github.com/dannyconnell/vscode-split-html-attributes/blob/master/CHANGELOG.md)

## My Other VSCode Extensions

- [Make Apps Theme](https://marketplace.visualstudio.com/items?itemName=dannyconnell.make-apps-theme "Make Apps Theme")