# Setup Notepad++ for AutoHotkey
tested up to Notepad++ v7.9.1 (64-bit)

## Syntax-Highlighting
- Download `userDefineLang_AHK.xml` (as raw)
- Save it to the right location:
  - 32-Bit `(C:\Program Files (x86)\Notepad++\)`
  - 64-Bit `(C:\Program Files\Notepad++\)`
- Start Notepad++ and click on Menu `Language -> User Defined Language -> Define your language...`
- `Import` your userDefineLang_AHK.xml
- `Restart` Notepad++

* **Default Theme** (
[Download](../master/userDefineLang/default/userDefineLang_AHK.xml) | [Preview](../master/userDefineLang/default/udl_default.png) )  
* **Lazy Theme** (
[Download](../master/userDefineLang/lazy/userDefineLang_AHK.xml) | [Preview](../master/userDefineLang/lazy/udl_lazy.png) )

---

## Auto-Completion
- Download `AutoHotkey.xml` (as raw)
- Save it to the right location:
  - 32-Bit `(C:\Program Files (x86)\Notepad++\autoCompletion\)`
  - 64-Bit `(C:\Program Files\Notepad++\autoCompletion\)`
- Start Notepad++ and click on Menu `Settings -> Preferences`
- Click on `Auto-Completion` and activate `Enable auto-completion on each input`
- (Recommendation: From 2th character, Function completion & Function parameters hint on input)

* **Autocompletion** (
[Download](../master/autocomplete/AutoHotkey.xml) | [Preview](../master/autocomplete/autocomplete.png) )

---

## Plugins
- Start Notepad++ and click on Menu `Plugins -> Plugins Admin...`
- Check the box for the plugins you want to install
- Click `Install`

Alternative:
- Download PlugIns
- Save it to the right location:
  - 32-Bit `(C:\Program Files (x86)\Notepad++\plugins)`
  - 64-Bit `(C:\Program Files\Notepad++\plugins\)`

Notepad++ loads plugins at startup. To load a new plugin, you can either close and restart Notepad++,  
or use the `Settings -> Import -> Import plugin(s)...` command.

**Useful Plugins**
* [AutoSave](https://sites.google.com/site/fstellari/nppplugins/) allows to automatically save the currently open files based on a timer schedule.
* [RunMe](https://sites.google.com/site/fstellari/nppplugins/) allows to execute the currently open file, based on its shell association.
* [TextFX](http://sourceforge.net/projects/npp-plugins/files/TextFX/) brings a number of useful features.

---

## Set Notepad++ as default Editor for AutoHotkey Scripts
(`Right Click -> Edit Script`)

##### With a *.reg File
```
Windows Registry Editor Version 5.00
 
[HKEY_CLASSES_ROOT\AutoHotkeyScript\Shell\Edit\Command]
@="C:\\Program Files (x86)\\Notepad++\\notepad++.exe %1"
```
##### With AutoHotkey (*.ahk)
```autohotkey
RegWrite REG_SZ, HKCR, AutoHotkeyScript\Shell\Edit\Command,, C:\Program Files (x86)\Notepad++\notepad++.exe `%1
```

---

## Downloads
* **[AutoHotkey](https://autohotkey.com/download/ "AutoHotkey Downloads")** (Current Version)
* **[Notepad++](https://notepad-plus-plus.org/download/ "Notepad++ - Current Version")** (Current Version)


## Donations
[Donations are appreciated if I could help you](https://www.paypal.me/smithz)
