# Fungus Advanced - Narrative Parser Tokens Reference

The following tokens can be used within Story Text to do things such as change the styling of text or clear the contents of a dialog area on input and much more.

* {b} - Bold start
* {/b} - Bold end
* {i} - Italic start
* {/i} - Italic end
* {color=red} - Color start
* {/color} - Color end
* {w} - Wait
* {w=0.5} - Wait for a certain amount of time
* {wi} - Wait for input, but do not clear the dialog area
* {wc} - Wait for input, clear the dialog area after input
* {wp} - Wait on punctutation start
* {wp=0.5} - Wait on punctutation (after a certain amount of time) start
* {/wp} - Wait on punctuation end
* {c} - Clear the dialog area
* {s} - Speed start
* {s=60} - Speed (with speed setting) start
* {/s} - Speed end
* {x} - Exit
* {m=MessageName} - Send a message with `MessageName`
* {vpunch=0.5} - Vertical punch
* {hpunch=0.5} - Horizontal punch
* {shake=0.5} - Shake
* {shiver=0.5} - Shiver
* {flash=0.5} - Flash
* {audio=Sound} - Audio start for `Sound`
* {audioloop=Sound} - Audio loop for `Sound`
* {audiopause=Sound} - Audio pause for `Sound`
* {audiostop=Sound} - Audio stop for `Sound`

Examples:

```
This is a line of dialog.
{wc}
This is another line of dialog with some {b}bold{/b} styling.
This is another line of dialog with some {color=blue}blue{/b} text.
```
