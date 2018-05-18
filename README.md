# `self` Discussion Questions

## Instructions

Take 30 minutes and answer the following questions together. Take turns playing around with the code provided in Pry or IRB.

1 .
```ruby
class FunnyBots
  attr_accessor :name, :quotes

  @@bots = []

  def initialize(name, quotes)
    @name = name
    @quotes = quotes
    @@bots << self
  end

  def random_quote
    self.quotes.sample
  end

  def self.bots
    @@bots
  end
end

Archer = FunnyBots.new("Archer", ["Danger Zone!", "Read a book", "The cumulative hangover would literally kill me"] )
```

A. What is **self** in this line ```@@bots << self``` ?
B. What is **self** in this line ```self.quotes.sample```?
C. What kind of **method** is this & what is **self**? ```  def self.bots
    @@bots end ```
D. Will this work ```Archer.bots```? If not, why?

2 .

```ruby
class Bicycle
  attr_reader :tire

  def initialize(tire, gears, style)
    @tire = tire
    @gears = gears
    @style = style
  end

  def tire_size
    self.tire
  end

  def self.gears
    @gears
  end
end

mongoose = Bicycle.new(4, 10, "BMX")
```

  For what reasons will each of the following method calls fail:

```ruby
  mongoose.tire_size = 5
  mongoose.gears
  Bicycle.bikes
  Bicycle.style
```

  Restructure the `Bicycle` class to fix each issues.

3 . We have a **method** called are #**are_we_there_yet**?. This method prints out "are we there yet?" four times every time the method is called. Use your experience with Rspec thus far to write a test that validates this method does what it is intended to do.
