## Arguments

```first, second, third = ARGV

puts "Your first variable is: #{first}"
puts "Your second variable is: #{second}"
puts "Your third variable is: #{third}"```

The ARGV is the "argument variable," a very standard name in programming that you will find used in many other languages. This variable holds the arguments you pass to your Ruby script when you run it.

Line 1 "unpacks" ARGV so that, rather than holding all the arguments, it gets assigned to three variables you can work with: first, second, and third.

Change your script to use $stdin.gets.chomp everywhere that you have gets.chomp. You should use $stdin.gets.chomp from now on since the action gets.chomp has problems with ARGV.