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
`variable_name = gets` store input\
`variable_name = gets.chomp()` remove enter after input\

\*Array\
->you can input different data type in array
`variable_name = Array["cool","wow",1,true]`\
`variable_name = Array.new` when you don't know the size of array.\
`variable_name.reverse()`\
`variable_name.sort()`\

\*Hashes\
`variable_name = { "key1" => "value1", "key2" => "value2", "key3" =>"value3" }`\

```console
   variable_name = {
    :key1 => "value1",
    "key2" =>   "value2",
    "key3" =>"value3"}
```

\*Methods\

1. defining and calling

```console
def method_name
    puts "hello"
end
method_name
```

2. parameter

```console
  def method_name(name)
    puts ("hello "+name)
 end

 method_name("cool")
```

3. default value in function

```console
def method_name(name="others")
    puts ("hello "+name)
end

method_name
```

4. return function

```console
def method_name(num)
   return num*num*num
end

puts method_name(2)
```

5. output 8 24

```console
def method_name(num)
   return num*num*num,24
end

puts method_name(2)
```

6. output 24

```console
def method_name(num)
   return num*num*num,24
end

puts method_name(2)[1]
```

\*If\

```console
iscar=true
if iscar
    puts "car"
else
    puts"not car"
end
```

you can also use or

```console
iscar=true
istop=false
if iscar and istop
    puts "car"
else
    puts"not car"
end
```

`elsif statement`\

\*case expression\

```console
case day
 when "Mon"
    day_name="Monday"
 when "Tue"
    day_name="Tuesday"
 else
    day_name="invalid"
 end
```

\*while loop\

```console
while i<=5
    puts i
    i+=1
end
```

\*for loop\

```console
langs=["java","js","nodejs"]
for lang in langs
    puts lang
end
```

```console
langs=["java","js","nodejs"]
langs.each do |lang|
    puts lang
end
```

print 0,1,2,3,4,5

```console
for i in 0..5
    puts i
end
```

``

print 0,1,2,3,4,5

```console
6.times do |index|
    puts index
end
```

output 8\

```console
def pow(b,p)
   r=1
   p.times do
   r=r*b
   end
return r
end
puts pow(2,3)
```

\*file reading \

opening a file\

```console
File.open("cool.txt","r") do |a|
   puts a.read()
end
```

reads line by line one each time from file\

```console
File.open("cool.txt","r") do |a|
   puts a.readline()
end
```

` puts a.readlines()` returns an array of all line in the file\

always close file\

```console
file1=File.open("cool.txt","r")
puts file1.readlines()
file1.close()
```

\*writing file\

1. append/write to the end of file

```console
File.open("cool.txt","a") do |a|
   a.write("cool,tel")
end
```

1. overwrite the full file

```console
File.open("cool.txt","w") do |a|
   a.write("cool,tel")
end
```

\*exception \

1. first syntax

```console
begin
   num=10/0
rescue
   puts "zerdivisionerror"
end
```

1. specifying error in rescue

```console
begin
  array["0"]
rescue TypeError
   puts "TypeError"
rescue ZeroDivisionError
  puts "ZeroDivisionError"
end
```

3. third way

```console
begin
   array["a"]
rescue TypeError => exception
   puts exception
end
```

\*classes and objects \

1. making class i.e blueprint of object

```console
class Car
attr_accessor :name, :model, :price
end
```

2. making object i.e istance of class

```console
car1=Car.new()
car1.name="tesla"
car1.model="X"
```

`

\*initialize methods\
these are the methods which will called automaticaaly when we make objects\

```console
class Car
attr_accessor :name, :model, :price
 def initialize(name,model,price)
 @name=name
 @model=model
 @price=price
 end
end
car1=Car.new("tesla","x",22)
```

\*object methods\

has_price is a object method\

```console
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

puts car1.has_price
```

\*inheritance <\

```console
class Car
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
car2.run_diesel
```

\*Modules\
to organize methods in a sperate container\
same file\

```console
module Car
   def model(name)
      puts "model #{name}"
   end
   def year(year)
      puts "year #{year}"
   end
end

include Car
Car.model("electric")
```

`require_relative "hello.rb"` just use require in another\
