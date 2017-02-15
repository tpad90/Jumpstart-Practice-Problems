```ruby
# Welcome statement. 

puts " Welcome to the Election Booth!
\n\nYour choice will determine who wins this Election.\n 
Choose wisely.\n\n"

#list all the candidates

puts " Candidates are: \n
       Harry Potter\n
       Khal Drogo\n
       Tyrion Lannister\n"
      
# Start a loop for i = 10 
 
 votes = [1,2,3,4,5,6,7,8,9,10]
 lists = Array.new(10,"empty")
 i=0
 harry = 0
 khal = 0 
 tyrion = 0 
 
10.times do |i|

# Ask to pick one . Give letter choices.  

 puts "\nPlease type H, K, or T for Harry, Khal and Tyrion respectively:\n>\n" 
 choice = gets.chomp.downcase

# if statements with tickers for each candidate #hp then increase hp

  if choice == "h"
    harry +=1
    choice = "Harry Potter"
    
    elsif choice == "k"
    khal +=1
    choice = "Khal Drogo"
    
    elsif choice == "t"
    tyrion +=1
    choice = "Tyrion Lannister" 
    
  end
  
  lists[i] = choice
  
# end loop  
 end
 
puts "\n\n
       Candidates are: \n
       Harry Potter\n
       Khal Drogo\n
       Tyrion Lannister\n"
 
num = 1
puts " \n "

lists.each do |name|
  puts "Vote #{num}: #{name}"
  num +=1
end

# print out total candidate votes
 
puts "\n\nRESULTS..\n\n"
if harry > 1 
puts "Harry: #{harry} votes"
else
puts "Harry: #{harry} vote" 
end

if khal > 1
puts "Khal Drogo: #{khal} votes"
else
puts "Khal Drogo: #{khal} vote"
end

if tyrion > 1
puts "Tyrion Lannister: #{tyrion} votes\n\n"
else
puts "Tyrion Lannister: #{tyrion} vote\n\n"
end

# use if statements for picking winner
# print out winner
if harry > khal && harry >tyrion
  puts "The winner is Harry Potter!"
  
elsif khal > harry && khal >tyrion
  puts "The winner is Khal Drogo!"
  
elsif tyrion > khal && tyrion > harry
  puts "The winner is Tyrion Lannister!"
  
elsif tyrion == harry && tyrion > khal
puts " Tyrion and Harry tie for First place!"

elsif tyrion == khal && tyrion > harry
puts " Tyrion and Khal tie for First place!"

elsif harry == khal && harry > tyrion
puts " Harry and Khal tie for First place!"

end

puts " \n\n "



```
