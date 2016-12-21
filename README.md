# Setup Notepad++ for AutoHotkey
tested up to Notepad++ v6.9.1

## Syntax-Highlighting
1. Download `userDefineLang_AHK.xml` (as raw)
2. Save it to the right location `(C:\Program Files (x86)\Notepad++\userDefineLang_AHK.xml)`
3. Start Notepad++ and click on Menu `Language --> Define your language`
4. `Import` your userDefineLang
5. `Restart` Notepad++

* **Default Theme** (
[Download](../master/userDefineLang/default/userDefineLang_AHK.xml) | [Preview](https://raw.githubusercontent.com/jNizM/ahk_notepad-plus-plus/master/userDefineLang/default/udl_default.png) )  
* **Lazy Theme** (
[Download](../master/userDefineLang/lazy/userDefineLang_AHK.xml) | [Preview](https://raw.githubusercontent.com/jNizM/ahk_notepad-plus-plus/master/userDefineLang/lazy/udl_lazy.png) )

---

## Auto-Completion
1. Download `AutoHotkey.xml` (as raw)
2. Save it to the right location `(C:\Program Files (x86)\Notepad++\plugins\APIs\AutoHotkey.xml)`
3. Start Notepad++ and click on Menu `Settings --> Preferences`
4. Click on `Auto-Completion` and activate `Enable auto-completion on each input`
5. (Recommendation: From 2th character - Function completion - Function parameters hint on input)

* **Autocompletion** (
[Download](../master/autocomplete/AutoHotkey.xml) | [Preview](https://raw.githubusercontent.com/jNizM/ahk_notepad-plus-plus/master/autocomplete/autocomplete.png) )

---

## Plugins
1. Download PlugIns
2. Save it to the right location `Notepad++\plugins\`  
Notepad++ loads plugins at startup. To load a new plugin, you can either close and restart Notepad++,  
or use the `Settings --> Import --> Import plugin` command.

**Useful Plug-In's**
* [AutoSave](https://sites.google.com/site/fstellari/nppplugins/) allows to automatically save the currently open files based on a timer schedule.
* [RunMe](https://sites.google.com/site/fstellari/nppplugins/) allows to execute the currently open file, based on its shell association.
* [TextFX](http://sourceforge.net/projects/npp-plugins/files/TextFX/) brings a number of useful features.

---

## Set Notepad++ as default Editor for AutoHotkey Scripts
(`Right Click --> Edit Script`)

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