```ruby
puts ' Welcome to the MAD-LIB fortune telling program,'
puts "where you will discover what the future has in hold for you\n\n"

#story
# You are _____ down a ____ and suddenly, a ____ appears.
# They tell you, Hello, _____, you have ____ choices to make. Pick one.
# Ah, so you have chosen choice number ___ .
# You will _____ a ____ ______ on _____. they will bring you ________. "

puts "1. verb ending in -ing: "
alley_verb = gets.chomp

puts "2. Noun: "
alley = gets.chomp

puts  "3. job title: "
surprise_noun = gets.chomp

puts "4. Your name: "
name = gets.chomp

puts "5. A number: "
digit = gets.chomp

puts "6. A number less than or equal to previous number: "
dig2= gets.chomp

puts "7. verb: "
verb = gets.chomp

puts "8. adjective: "
adj = gets.chomp

puts "9. noun: "
noun2 = gets.chomp

puts "10. Day of the week: "
day = gets.chomp

puts "11. noun: "
gift = gets.chomp

print "You are " + alley_verb + " down a " + alley + " alley and suddenly, a " + surprise_noun + " appears."
print "They say to you, Hello, " + name + " , you have " + digit +  " choices to make. Pick one."

print " Ah, so you have chosen choice number " + dig2 + "."
print  " You will " + verb + " a " + adj + " " + noun2 + " on " + day + "."
print " They will bring you a " + gift + "."

```
