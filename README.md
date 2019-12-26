AutoFileName Improved
============

Autocomplete Filenames in Sublime Text
--------------------------------------
Do you ever find yourself sifting through folders in the sidebar trying to remember what you named that file? Can't remember if it was a jpg or a png? Maybe you just wish you could type filenames faster. *No more.*

Whether you're making a `img` tag in html, setting a background image in css, or linking a `.js` file to your html (or whatever else people use filename paths for these days...), you can now autocomplete the filename. Plus, it uses the built-in autocomplete, so no need to learn another pesky shortcut.

Features
--------

- Display filenames and folders
- Show dimensions next to image files
- Autoinsert dimensions in img tags (can be disabled in settings)
- Support for both '/' and '\' for all you Windows hooligans


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`AutoFileName`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


Usage
-----
**Nothing!**

For example:

If you are looking to autocomplete an image path in an HTML `<img>` tag:
```html
    <img src="../|" />
```

Pressing <kbd>ctrl</kbd>+<kbd>space</kbd>, will activate AutoFileName.  I list of available files where be ready to select.

*Looking for an even more automatic and seemless completion?*  Add the following to your User Settings file:

    "auto_complete_triggers":
    [
      {
         "characters": "<",
         "selector": "text.html"
      },
      {
         "characters": "/",
         "selector": "string.quoted.double.html,string.quoted.single.html, source.css"
      }
    ]

With this, there's no need to worry about pressing <kbd>ctrl</kbd>+<kbd>space</kbd>, autocompletion with appear upon pressing /.
