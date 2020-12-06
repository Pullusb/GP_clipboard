# GP clipboard
Blender Addon - Grease pencil clipboard to copy/cut/paste strokes across layers and blends

**[Download latest](https://github.com/Pullusb/GP_clipboard/archive/master.zip)** 

**[Download old (2.79)](https://github.com/Pullusb/GP_clipboard/raw/master/GP_clipboard279.py)** (right click, save Target as) 

---

### Description:
The default copy/paste of grease pencil strokes copy strokes using the coordinate relative to the object.
In some cases it's usefull to copy "In place" (using world coordinate of strokes)   
The cutting is also more user friendly.  

Cut and Copy works accross multiple layers, Paste is only made on active layer.

You can also copy entires layers>frames (bake the stroke position if object is animated).

Button are localised in View3D > Toolbar > GPencil > GP clipboard

GP clipboard use the paper clip of your OS to store grease pencil strokes.
This mean you can even paste your copied stroke in another blend or in a text file for later re-use.
But be carefull not to overwrite you clipboard if you have a stroke you must not lose. (This will not happen if you're using a clipboard history manager [like Ditto (windows only)](https://ditto-cp.sourceforge.io/), wich I highly recommend ^^)

Thanks to [Mathieu Chaptel](https://vimeo.com/user1760436) for the discussions on core features.

---

**Note for workflow**
Cut/Copy/Paste are automatically keymapped on `ctrl + shift + X/C/V`  

If you want to assign another shortcut :
 - In the user preference > inputs:
 - unfold the "3Dview" section (or "Window" section if you want the shortcut to be active in multiple editor)
 - scroll down and click the `add new`button
 - enter the keymap of your choice in the key field
 - In the text field enter one of the following IDname (corresponding to operator):  
 `gp.copy_strokes`, `gp.cut_strokes`, `gp.paste_strokes`
  
 - to map multi layers copy-paste use `gp.copy_multi_strokes` and `gp.paste_multi_strokes`
 
---

### Todo:

- Maybe let access to hardcoded filter/preference (as checkbox in the panel):
  - keep_empty = True (on cut) -> When all strokes are cutted the (key)frame is leaved empty (False : frame is deleted if no strokes left)
  - use_current_frame = True (on paste) -> when pasting use current (key)frame if exists (False: Create a new one at current time if needed)

- Maybe add a checkbox in preferences to disable auto-shortcut

---

### Changelog:


1.3.2:

- fix: attribute error (cyclic attribute name changed in 2.92: `draw_cyclic` -> `use_cyclic`)
  - Supposed to be still compatible with 2.91 and before (untested).

1.3.1:

- fix: Bug in keymap register that could affect other addon's keymap

1.3.0:

- Feat: addon prefs, option to change the tab name

1.2.0:

- Feat: copy a selection of layers with object transform baking

1.1.0:

- Big bugfix, Paste in place now working for normal and parented layers

1.0.0:

- First working update for 2.83