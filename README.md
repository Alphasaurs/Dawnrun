# Dawnrun

`irb` to use interactive ruby in command prompt\
`#`comments\
`=begin =end`multi comments\
`print "hello"` print at same line\
`puts "hello"` print at new line\
`puts ("hello"+ variable_name)` string concatenation variable should be string.\
`puts "hello #{variable_name}` String Interpolation any varible\

\*String methods\
`puts variable_name.upcase()`\
`puts variable_name.downcase()`\
`puts variable_name.strip()` to remove all whitespaces\
`puts variable_name.length()`\
`puts variable_name.include? "checking_word" ` to see checking_word is present in variable_name\
`puts variable_name[4,8]` print value fromt 4 to 8\
`puts variable_name.index("A")` find index of "A" in variable_name\
`variable_name.to_i`integer\
`variable_name.to_f`float\

\*Integer methods\
`puts ("ans is "+variable_name.to_s)` convert int to s\
`puts variable_name.abs()`\
`puts variable_name.round()`\
`puts variable_name.ceil()`\
`puts variable_name.floor()`\
`puts Math.sqrt(number)`\

\*input\
`variable_name = gets`\ store input
`variable_name = gets.chomp()` remove enter after input

\*Array\
->you can input different data type in array
`variable_name = Array["cool","wow",1,true]`\
`variable_name = Array.new` when you don't know the size of array.\
`variable_name.reverse()`\
`variable_name.sort()`\

\*Hashes\
`variable_name = { "key1" => "value1", "key2" => "value2", "key3" =>"value3" }`\
`variable_name = {
    :key1 => "value1",
    "key2" =>   "value2",
    "key3" =>"value3"
}`\

\*Methods\
<code>def method_name
    puts "hello"
end

method_name</code> defining and calling\
`def method_name(name)
    puts ("hello "+name)
end

method_name("cool")` parameter \

`def method_name(name="others")
    puts ("hello "+name)
end

method_name` default value in function\

`def method_name(num)
   return num*num*num
end

puts method_name(2)` return function\

`def method_name(num)
   return num*num*num,24
end

puts method_name(2)` output 8 24\

`def method_name(num)
   return num*num*num,24
end

puts method_name(2)[1]` output 24\



\*If\
`iscar=true
if iscar
    puts "car"
else
    puts"not car"
end`\

`
iscar=true
istop=false
if iscar and istop
    puts "car"
else
    puts"not car"
end` you can also use `or`\

`elsif statement`\

\*case expression\
` case day
 when "Mon"
    day_name="Monday"
 when "Tue"
    day_name="Tuesday"
 else
    day_name="invalid"
 end`\

\*while loop\
`while i<=5
    puts i
    i+=1
end`\

\*for loop\
`langs=["java","js","nodejs"]
for lang in langs
    puts lang
end`\

`langs=["java","js","nodejs"]
langs.each do |lang|
    puts lang
end`\

`for i in 0..5
    puts i
end` print 0,1,2,3,4,5\

`6.times do |index|
    puts index
end` print 0,1,2,3,4,5\

`def pow(b,p)
   r=1
   p.times do
   r=r*b   
   end
return r
end
puts pow(2,3)` output 8\

\*file reading \
`File.open("cool.txt","r") do |a|
   puts a.read()
end` opening a file\

`File.open("cool.txt","r") do |a|
   puts a.readline()
end` reads  line by line one each time from file\

` puts a.readlines()` returns an array of all line in the file\
`file1=File.open("cool.txt","r") 
puts file1.readlines()
file1.close()`always close file\

\*writing file\
`File.open("cool.txt","a") do |a|
   a.write("cool,tel")
end`append/write to the end of file\

`File.open("cool.txt","w") do |a|
   a.write("cool,tel")
end`overwrite the full file \



\*exception \
`begin
   num=10/0
rescue 
   puts "zerdivisionerror" 
end`first syntax\
`begin
  array["0"]
rescue TypeError
   puts "TypeError" 
rescue ZeroDivisionError
  puts "ZeroDivisionError"
end` specifying error in rescue\

`begin
   array["a"]
rescue TypeError => exception
   puts exception
end` third way\



\*classes and objects \
`class Car
attr_accessor :name, :model, :price
end
`making class i.e blueprint of object\
`car1=Car.new()
car1.name="tesla"
car1.model="X"
` making object i.e istance of class\


\*initialize methods\
these are the methods which will called automaticaaly when we make objects\
`class Car
attr_accessor :name, :model, :price
 def initialize(name,model,price)
 @name=name
 @model=model
 @price=price
 end
end
car1=Car.new("tesla","x",22)` \

\*object methods\
`
class Car
attr_accessor :name, :model, :price
 def initialize(name,model,price)
 @name=name
 @model=model
 @price=price
 end

 def has_price
   if @price>300
      return true
   end
   return false
  end
end

car1=Car.new("tesla","x",2200)

puts car1.has_price` has_price is a object method\


\*inheritance <\

`class Car
    def run_diesel
       puts "we run diesel"
    end
    def run_petrol
    puts "we run petrol"
    end
end

class SpecialCar < Car
end

car1=Car.new()
car1.run_petrol

car2=SpecialCar.new()
car2.run_diesel` \



\*Modules\
to organize methods in a sperate container\

`module Car
   def model(name)
      puts "model #{name}"
   end
   def year(year)
      puts "year #{year}"
   end
end

include Car
Car.model("electric")
`same file\

`require_relative "hello.rb"` just use require in another\
