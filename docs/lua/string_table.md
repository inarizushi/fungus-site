# String Table

LuaUtils provides support for simple text localisation. Define your language strings in a JSON file, add a LuaEnvironment to your scene, and set the String Table property to reference the JSON file. You can then use the {$StringKey} syntax anywhere that variable subsitution is supported (e.g. in Say or Menu command text in a Flowchart), and the localised version of StringKey will be substituted.

# JSON Format

This is an example of the JSON format for the string table. To use this localised string, you would use the {$hello} tag.

```python
{
    "hello" : {
        "en" : "Hi there",
        "fr" : "Bonjour"
    }
    ... more string entries
}
```

# Lua Functions

These Lua functions are available for working with the string table.

```python
-- Set active language for string table
setlanguage(languagecode)

-- Get a named string from the string table
getstring(key)

-- Substitutes variables and localisation strings into a piece of text
-- e.g. v = 10, "Subbed value is [$v]" => "Subbed value is 10"
sub(text)
```

