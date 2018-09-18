# Reading and writing files
```close``` -- Closes the file. Like File->Save.. in your editor.
```read``` -- Reads the contents of the file. You can assign the result to a variable.
```readline``` -- Reads just one line of a text file.
```truncate``` -- Empties the file. Watch out if you care about the file.
```write('stuff')``` -- Writes "stuff" to the file.
```seek(0)``` -- Move the read/write location to the beginning of the file.

### What does 'w' mean?
It's really just a string with a character in it for the kind of mode for the file. If you use 'w' then you're saying "open this file in 'write' mode," thus the 'w' character. There's also 'r' for "read," 'a' for append, and modifiers on these.