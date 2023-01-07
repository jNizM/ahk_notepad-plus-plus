# Set up Notepad++ for AutoHotkey
Tested with Notepad++ v8.4.8 (64-bit)

---

## Syntax Highlighting
- Download `userDefineLang_AHK.xml` (right-click the download link and choose `Save link as`)
  - [Download](../../raw/master/userDefineLang/default/userDefineLang_AHK.xml) | [Preview](../../raw//master/userDefineLang/default/udl_default.png) _(Default theme)_
  - [Download](../../raw/master/userDefineLang/lazy/userDefineLang_AHK.xml) | [Preview](../../raw/master/userDefineLang/lazy/udl_lazy.png) _(Lazy theme)_
- Open your download folder
- Start Notepad++ and click on menu `Language -> User Defined Language -> Open User Defined Language folder...`
- Move `userDefineLang_AHK.xml` from your download folder to this folder
- Restart Notepad++

---

## Auto-Completion
- Download `AutoHotkey.xml` (right-click the download link and choose `Save link as`)
  - [Download](../../raw/master/autocomplete/AutoHotkey.xml) | [Preview](../../raw/master/autocomplete/autocomplete.png)
- Save it to the right location:
  - 32-Bit `(C:\Program Files (x86)\Notepad++\autoCompletion\)`
  - 64-Bit `(C:\Program Files\Notepad++\autoCompletion\)`
- Start Notepad++ and click on menu `Settings -> Preferences`
- Click on `Auto-Completion` and activate `Enable auto-completion on each input`
- (Recommendation: From 2th character, Function completion & Function parameters hint on input)

---

## Useful Notepad++ Plugins
These plugins may be useful when using Notepad++ to edit AutoHotkey scripts:
* [AutoSave](https://github.com/francostellari/NppPlugins) - _automatically save the currently open files based on a timer schedule._
* [RunMe](https://github.com/francostellari/NppPlugins) - _execute the currently open file, based on its shell association._

### Install Notepad++ Plugins
You can install Notepad++ plugins by using the Notepad++ plugin manager:
- Start Notepad++ and click on menu `Plugins -> Plugins Admin...`
- Check the box for the plugins you want to install
- Click `Install`

Or by using Notepad++ import:
- Download the plugin's dll file
- Start Notepad++ as administrator and click on menu `Settings -> Import -> Import plugin(s)...`
- Navigate to the downloaded dll file and click the `Open` button

---

## Set up AutoHotkey to Use Notepad++
AutoHotkey launches an editor to edit a script when menu option `Edit Script` or `Edit This Script` is selected. This menu option is listed in Windows Explorer's right-click menu and in several AutoHotkey menus.

### If AutoHotkey v2 is installed
To set up AutoHotkey to use Notepad++ as script editor:
- Run `AutoHotkey` (which launches AutoHotkey Dash) and click `Editor settings`  
  (Or select `Edit Script` or `Edit This Script` in one of the menus if an editor has not been set yet)
- A dialog will appear where you can set the editor of your choice. In the Command line field, enter the following text:  
  ```
  Notepad++.exe "%L"
  ```
- Click `OK`

### If AutoHotkey v1 is installed and not also AutoHotkey v2
To set up AutoHotkey to use Notepad++ as script editor, do one of the following:
- Create and run a .reg file with the following contents:
  ```
  Windows Registry Editor Version 5.00
   
  [HKEY_CLASSES_ROOT\AutoHotkeyScript\Shell\Edit\Command]
  @="Notepad++.exe \"%L\""
  ```
- Or create and run a .ahk file with the following contents (run as administrator):
  ```
  RegWrite REG_SZ, HKCR, AutoHotkeyScript\Shell\Edit\Command,, Notepad++.exe "`%L"
  ```

---

## Downloads
* [Notepad++](https://notepad-plus-plus.org/download/ "Notepad++ download page") _(software)_
* [AutoHotkey](https://autohotkey.com/download/ "AutoHotkey download page") _(software)_
* [userDefineLang_AHK.xml](../../raw/master/userDefineLang/default/userDefineLang_AHK.xml) _(xml file for Syntax Highlighting, **Default theme**)_
* [userDefineLang_AHK.xml](../../raw/master/userDefineLang/lazy/userDefineLang_AHK.xml) _(xml file for Syntax Highlighting, **Lazy theme**)_
* [AutoHotkey.xml](../../raw/master/autocomplete/AutoHotkey.xml) _(xml file for Auto-Complete function)_

---

## Forum topics
* AutoHotkey forum: [Setup Notepad++ for AutoHotkey](https://www.autohotkey.com/boards/viewtopic.php?f=88&t=50)

---

## Donations
[Donations are appreciated if I could help you](https://www.paypal.me/smithz)
