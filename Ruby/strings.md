## Should I use %{} or #{} for formatting?
You will almost always use #{} to format your strings, but there are times when you want to apply the same format to multiple values. That's when %{} comes in handy.

## Quote 
```puts %q{
There's something going on here.
With this weird quote
We'll be able to type as much as we like.
Even 4 lines if we want, or 5, or 6.
}
```

## Newline character
the characters \n (backslash n) between the names of the months. These two characters put a new line character into the string at that point.

## Backlash

Lets you escape the symbols, like in JS

## Asking for input

There are two methods happening with gets.chomp (gets and chomp). If you call gets, ruby will wait for the user to input text in our case via the keyboard. When you press enter, this is returned. In your code when your enter your name, it sets the variable name to whatever your type in.

When you use just "gets" and press enter/return. You are actually adding a newline (\n) to the end of your string, ruby is actually literally taking the enter and adding it to the end of your input.

As for the chomp, this is a method that can be called on a string. Keep in mind when you input your name, it's input as text. Text can accept the chomp method, which will strip your text of any newlines, or carrige returns at the end..
