```ruby
# Arrays

# names = []
# number = []
# emails= []
accounts = []

#Hashes
temp_account = {}


# STRINGS

firstname = ""
lastname = ""
fullname = ""
email = ""
numbercurrent = ""
space=""

#INTEGERS

x= 0
issame = 0
i = 0
j = 0
studentsize = 0

# Ask how big the student size will be to know loop iterations
# if importing from a file, find the size of array and use that as variable for loop size

puts "How many students are you inputing?:"
studentsize = gets.chomp.to_i

studentsize.times do |x|

 y = x+1

# Asking for First name.

  print "\nEnter student ##{y}'s first name:"
  firstname = gets.chomp.upcase

# To catch if the first name has two words

  if firstname.slice(" ") != nil
    space = firstname.index(" ")
    space +=1
    spaceexists = 1
  end

# ask for last name

  print "Enter student ##{y}'s  last name:"
  lastname = gets.chomp.upcase

#Combining first and last name and saving into temp varible

  fullname = firstname +" "+ lastname

#Save temp variable into NAME hash in temp_account array


  temp_account = {name: fullname}
  accounts << temp_account

#find the size of the array to know if we need to check for duplicate IDs

  issame = 0
  size = accounts.length

# if size is more than zero, then array has at least one value. So the loop can begin  . if not, then a value is added to array

  if size > 0

    # puts "\n----GOES INTO IF----\n\n"
    # puts "Please enter 6 digit new ID:"

    # generates random ID

      numbercurrent = rand(111111...999999).to_s
      # numbercurrent = rand(111111...111113).to_s

      # numbercurrent = gets.chomp

      #loop and if statement goes through array to check if the new ID already exists in array

        i=0
        size.times do |i|


           if accounts[i][:ID] == numbercurrent
           issame +=1   # if ID exists, then variable issame increases by "1"
           end # ends if statement

        end # ends times loop to check through 'number' array


    #while the same number exists, the loop continues to find a new ID number that doesn't already exist.

      while issame > 0

      puts "Please enter new ID,that one is taken:"
      # numbercurrent = gets.chomp

      numbercurrent = rand(111111...999999).to_s
        # numbercurrent = rand(111111...111113).to_s

       issame = 0
        size.times do |j|

           if accounts[j][:ID] == numbercurrent
           issame += 1

           end # ends if statement

        end # ends times loop to check through 'number' array


     end # ends while loop which checks that the new ID does not already exist in 'number' array

    #exit 'while loop' because this ID is brand spanking new and save it into array

    # number << numbercurrent
     accounts[x][:ID] =  numbercurrent

  # goes into elseif, if the array is empty and you don't need to check if this id exists. Adds ID directly into array

  elsif size == 0

  # puts "\n GOES INTO ELSEIF---\n\n"
  # puts "please enter 6 digit ID:"
  # numbercurrent = gets.chomp

    numbercurrent = rand(111111...999999).to_s
    # numbercurrent = rand(111111...111113).to_s
     accounts[x][:ID] = numbercurrent


  end

  puts "\n" + fullname + "'s ID is...: #{numbercurrent}"

 #Generating temp email by combining components of LN, FN and ID
#if first name has two words, then initials of both words are added to email

if spaceexists == 1

    email = firstname[0] +firstname[space] + lastname + numbercurrent.slice(3,3) + "@adadevelopersacademy.org"
  else

# if first name has one word, then first name initial is only needed in email

  email = firstname[0] + lastname + numbercurrent.slice(3,3) + "@adadevelopersacademy.org"

end

#Save temp email into email array

  accounts[x][:email] = email
  puts fullname + "'s email address is :\n\n"+ email


end

puts "\n"

studentsize.times do |x|
  puts accounts[x]
  puts "\n"
end
```
