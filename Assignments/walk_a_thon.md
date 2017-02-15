``` ruby
puts "Welcome to the Walk a Thon!"

print "Please enter the earning goal for this event:"
goal = gets.chomp.to_f

print "\nPlease enter the following info\n"
puts "------------------------------------------------------"
puts "------------------------------------------------------"

i = 0
total = 0
accounts = []
earned_array =[]
temp_hash={}
round_money= 0.0


5.times do |i|
  
  
  j = i + 1
  print "Walker #{j}"
  player = j 
  
  print "\nEnter the amount earned per lap in dollars:"
  round_money = gets.chomp.to_f
  
  print "Laps: "
  laps = gets.chomp.to_f

  earned = laps * round_money
  print "Earned: $#{sprintf '%.2f',earned}"
  
  puts "\n------------------------------------------------------\n\n"
  # puts "\n______________________________________________________\n\n"

   
  temp_hash = {player: j,  laps: laps, earned: earned, perlap: round_money} 
  accounts << temp_hash
  earned_array << earned
  
  total += earned 
  
end

puts "Total earned: $#{sprintf '%.2f',total}\n\n"

if total > goal 
  met = total - goal 
  puts "Yay! We exceeded our goal by $#{sprintf '%.2f',met}!\nThank you everybody."
elsif total < goal 
  missed = goal - total
  puts  "We did not reach our goal.\nWe missed it by $#{sprintf '%.2f', missed}\nYou guys are awesome for participating anyway!"

else
  puts "Yay! We met our goal!\nThank you everybody."
end


most = earned_array.max
k=0
l=0
most_index = []

5.times do |k|
  if earned_array[k] == most
    l= k+1
  most_index << l
  end
end

size_most = most_index.length 
h = 0

if size_most > 1
 
  puts "\nCongratulations to:"
  size_most.times do |h|
    puts "   Walker #{most_index[h]}"
  end
  puts "for bringing in the mostest!"
  
else
  puts "\nCongratulations to Walker #{most_index[0]} for bringing in the mostest! "
end

```
