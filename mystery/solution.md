# searched for the clues in the
# crimescene folder

grep CLUE ./crimescene

# found out the perp is a tall male
# at least 6'. 
# Left wallet by killer loose change
# membership cards for AAA, Delta Skymiles
# the local library, museum of Bash History
# barista said woman left right before
# Annabel on her latte blond spiky
# hair. New Zealand accent

head -n 20 . /people 

# looked for Annabel needs to be more specifif

grep Annabel ./people

# found 4 people named Annabel
# one on 26 Hart Place line 40
# one on 38 Buckingham Place 179
# one on 37 Mattapan Street 173 
# one on 40 Haley Street 176

cd streets

cat Hart_Place

# wrong house. 

cat Buckingham_Place

# wrong house

cat Mattapan_Street

# wrong house again
# trying a new style after looking at some hints

head -n 40 Hart_Place | tail -n 1

# got interview  #47246024
# ran code for the other 3 addresses
# Buckinghamn = interview  #699607
# Mattapan = #9437737
# Haley = #871877

cd interviews

cat interview-47246024

# Ms. Sun is not from New Zealand
 cat interview-699607
# Ms Church saw a blue Honda license plate #starts with l337 and ends with a 9

cd ..

grep L337 ./vehicles
# returned 12 cars
# trying a search with multiple arguments next time

grep -A 5 "L337" ./vehicles

# this narrowed my search to find that Aron Pilhofer , Joe Germuska, Jeremy Bowers are the prime suspects that fit the description.
# now to find out who is a member to the cards that were found

cd memberships

# looking for who is a member of AAA, Delta_SkyMiles, and Museum_of_Bash_History

grep Aron ./AAA

# Not a member 

grep Joe ./AAA

# is a a member of AAA
grep Jeremy ./AAA
# also a member
grep Joe ./Delta_Skymiles
# Not a member of Delta
grep Jeremy ./Delta_SkyMiles
# Jeremy is a member of both. The only one of both.
grep Jeremy ./Museum_of_Bash_History
#And also the library 
#Jeremy Bowers is the shooter








