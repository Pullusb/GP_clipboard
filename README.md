# GP clipboard
Blender Addon (2.79) - Grease pencil clipboard to copy/cut/paste strokes across layers and blends

---

### Description:
The default copy/paste of grease pencil strokes does not allow to copy between layers, this one does and even between blend files.  
The cutting is also more user friendly.  
Button are localised in View3D > Toolbar > Grease Pencil > GP clipboard

GP clipboard use the paper clip of your OS to store grease pencil strokes.
This mean you can even paste your copied stroke in a text file for later re-use.
But be carefull not to overwrite you clipboard if you have a stroke you must not lose. (This will not happen if you're using a clipboard history manager [like Ditto (windows only)](https://ditto-cp.sourceforge.io/), wich I highly recommend ^^)

*Note for better workflow:*
If you want to assign a shortcut to be more efficient than the basic button clicking you can setup custom shortcuts :
 - In the user preference > inputs:
 - unfold the "3Dview" section (or "Window" section if you want the shortcut to be active in multiple editor)
 - scroll down and click the `add new`button
 - enter the keymap of your choice in the key field
 - In the text field enter one of the following IDname (corresponding to operator):  
 `gp.copy_strokes`, `gp.cut_strokes`, `gp.paste_strokes`
 

---

### Todo:

- Maybe let access to hardcoded filter/preference (as checkbox in the panel):
  - keep_empty = True (on cut) -> When all strokes are cutted the (key)frame is leaved empty (False : frame is deleted if no strokes left)
  - use_current_frame = True (on paste) -> when pasting use current (key)frame if exists (False: Create a new one at current time if needed)

- Maybe add a checkbox in preferences to setup shortcuts (this is ready, but difficult to choose a relevant keymap without conflict...)
