# `self` Discussion Questions

## Instructions

Take 30 minutes and answer the following questions together with your group. Take turns playing around with the code provided in Pry or IRB.

1 .   

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

  A. What is **self** in this line ```@@bots << self``` ?  
  B. What is **self** in this line ```self.quotes.sample```?  
  C. What kind of **method** is this & what is **self**? ```  def self.bots  
      @@bots end ```  
  D. Will this work ```Archer.bots```? If not, why? 
  

2 .

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

  For what reasons will the following method calls fail :```mongoose.tire_size = 5```, ```mongoose.gears```, ```Bicycle.bikes```, ```Bicycle.style```? Restructure the class to fix the issues.

3 . You have created a command line application that requires the user of your app to use the `HTTParty`, `NokoGiri`, and `RMMagix ~> 2.15.1` **gems**. How would you **programmatically** handle these dependencies in your application? How would you make sure the user has the gems on their machine, and if they did not, how would you make sure you could install the gems for them?

4 . We have a **method** called are #**are_we_there_yet**?. This method prints out "are we there yet?" four times every time the method is called.
Write a Rspec test that validates that this method does what it is intended to do.

<p class='util--hide'>View <a href='https://learn.co/lessons/week-1-day-5-discussion'>Week 1 Day 5 Discussion</a> on Learn.co and start learning to code for free.</p>
