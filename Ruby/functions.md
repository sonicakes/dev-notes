# Functions
```
# this is like your scripts with ARGV
def print_two(*args)
    arg1, arg2 = args
    puts "arg1: #{arg1}, arg2: #{arg2}"
end
```
this was unpacking method

### What does the * in *args do?
That tells Ruby to take all the arguments to the function and then put them in args as a list. It's like argv that you've been using but for functions. It's not normally used too often unless specifically needed.