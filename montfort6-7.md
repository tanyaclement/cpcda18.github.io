Montfort, Text I and Text II.
Montfort didn't use Python3 when he wrote this book so there are a few things that you'll want to know as you go through Text I and Text II:

- First, remember that all `print` commands are `print()` (with the parentheses).
- Second, remember that if you are executing the code in your Jupyter notebook (which I recommend) that you have spun up through Docker, any files you want to incorporate have to be your /'sharedfolder'.
- Finally, there are some "errors":
  - on pg. 138, the code doesn't work as Montfort has it written. Instead of `"[^"]*\r\n\r\n` try `"[A-Za-z][^"]*\r\n\r\n` and use that as the basis for the rest of the exercises that call for this regex.
  - on pg. 140, try `print(quotes[:10])` to see it rendered without the new line characters and instead of `len(".join(quotes))` try `len('"'.join(quotes))` so that the doublequote mark appears between the two single quotes.
  - also on pg. 140, note that `len('"'.join(quotes))/(len(pride))` will give you the same result as `len('"'.join(quotes))/float(len(pride))` 
