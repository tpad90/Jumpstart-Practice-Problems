```ruby
puts "Welcome to CandyLand!\n\n"
print "\nHow much money do you want to spend on a future filled with Dibeetus?\nPlease enter the dollar amount without the $ sign:"
money = gets.chomp.to_f

if money < 0.75
  puts "\n\nSorry! That isn't enough money to purchase candy from our machine."
else

  puts "\n\nOh! $ #{money} is perfect! Here are your options to a slow and painful.... life.\n\n"
  puts "Please select from the list of candies below" + "\n\n"

  puts "A. $4.00:  Toblerone"
  puts "B. $3.00:  Justins"
  puts "C. $2.50:  Cadbury with nuts and fruit."
  puts "D. $3.65:  Kinder Bueno"
  puts "E. $0.75:  Reeses Pieces"
  puts "F. $1.85:  Ferrero Rocher" + "\n\n"

  puts 'Please select a letter from A to F:.'
  candy = gets.chomp.downcase



  puts 'You have selected option' + "'" + candy.capitalize + "'"+ "\n\n"

  if candy == 'a' && money >= 4.00
    change = money - 4.00
    print "Thank you for your payment. Your change is: $#{change}" 
  elsif candy == 'a' && money < 4.00
  print " Oops! that isn't enough gold for the Toblerone!"
  end

  if candy == 'b' && money >= 3.00
    change = money - 3.00
     print "Thank you for your payment. Your change is: $#{change}" 
  elsif candy == 'b' && money < 3.00
  print " Oops! that isn't enough gold for the Justins!"
  end

  if candy == 'c' && money >= 2.50
    change = money - 2.50
     print "Thank you for your payment. Your change is: $#{change}" 
  elsif candy == 'c' && money < 2.50
  print " Oops! that isn't enough gold for the Cadbury!"
  end

  if candy == 'd' && money >= 3.65
    change = money - 3.65
      print "Thank you for your payment. Your change is: $#{change}" 
  elsif candy == 'd' && money < 3.65
  print " Oops! that isn't enough gold for the Kinder Bueno!"
  end

  if candy == 'e' && money >= 0.75
    change = money - 0.75
      print "Thank you for your payment. Your change is: $#{change}" 
  elsif candy == 'e' && money < 0.75
  print " Oops! that isn't enough gold for the Reeses Pieces!"
  end

  if candy == 'f' && money >= 1.85
    change = money - 1.85
      print "Thank you for your payment. Your change is: $#{change}" 
  elsif candy == 'f' && money < 1.85
  print " Oops! that isn't enough gold for the Ferrero Rocher!"
  end

end

```
