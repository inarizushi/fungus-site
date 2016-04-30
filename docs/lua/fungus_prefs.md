# PlayerPrefs

The Unity PlayerPrefs system stores and accesses player preferences between game sessions. The [PlayerPrefs documentation](http://docs.unity3d.com/ScriptReference/PlayerPrefs.html) describes how to use it.

Here's an example of using PlayerPrefs from Lua.

```python
-- Saving a value to preferences
playerprefs.SetInt("SaveName", 1)
playerprefs.Save()

-- Using a value from preferences
local v = playerprefs.GetInt("SaveName")
print(v) -- Will print out 1
```

# FungusPrefs

The FungusPrefs class is a wrapper around PlayerPrefs that adds support for save slots. Basically, if you just want to store values use PlayerPrefs, if you want to store values in multiple player profiles, use FungusPrefs.

```python
-- Deletes all saved values for all slots.
prefs.DeleteAll()

-- Removes key and its value from this save slot.
prefs.DeleteKey(slot, key)

-- Returns the float value associated with this key in this save slot, it it exists.
prefs.GetFloat(slot, key, defaultValue)

-- Returns the int value associated with this key in this save slot, it it exists.
prefs.GetInt(slot, key, defaultValue)

-- Returns the string value associated with this key in this save slot, it it exists.
prefs.GetString(slot, key, defaultValue)

-- Returns true if the key exists in this save slot.
prefs.HasKey(slot, key)

-- Writes all modified prefences to disk.
prefs.Save()

-- Sets the value of the preference identified by key for this save slot.
prefs.SetFloat(slot, key, value)

-- Sets the value of the preference identified by key for this save slot.
prefs.SetInt(slot, key, value)

-- Sets the value of the preference identified by key for this save slot.
prefs.SetString(slot, key, value)

-- Returns the combined key used to identify a key within a save slot.
prefs.GetSlotKey(slot, key)
```