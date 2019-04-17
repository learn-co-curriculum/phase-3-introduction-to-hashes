# Ruby Hashes

## Learning Goals

- Define a Ruby hash
- Define hash keys and values
- Create a hash using its implicit form
- Create a hash with `Hash.new`

## Introduction

Up until this point, we've stored our data in list-form using arrays. An array
is like a numbered list. It stores a group of items which are accessible via
their location, or index number, in the list.

Imagine a grocery list: you need to go to the store and buy milk, eggs and
bread. You could store your list like this:

```ruby
groceries = ["milk", "eggs", "bread"]
```

What happens when your list expands to include your other errands? Let's say you
need to go the grocery store, the pharmacy, and the stationery store (you've
been using up a lot of paper as you take copious notes on learning to code).

We could make one giant array that contains all of the items you need to buy:

```ruby
stuff_i_need = ["milk", "eggs", "bread", "toothpaste", "band-aids", "paper", "pens", "highlighter"]
```

This isn't very organized though. There is no way to distinguish the different
categories of items.

This is where hashes come in. Hashes allow us to store named, or associated,
data. Think of a dictionary or an address book. This allows us to store more
complex collections of information than the arrays we've seen so far. With a
hash, we can group our data into the necessary categories of "grocery",
"pharmacy", and "stationery".

## Define a Ruby Hash

A _hash_ is a collection of data that is separated into pairs of keys and values.
Each key/value pair makes up one unit in the hash. The entire collection of
key/value pairs, which are comma separated, is enclosed in curly braces `{}`:

```ruby
{"key" => "value", "another_key" => "another value"}
```

## Define Hash Keys and Values

In earlier lessons, we discussed variable assignment:

```ruby
apple = "a delicious fruit"
garlic = "an herb used for flavoring in many cuisines"
cheese = "a dairy product derived from the coagulation of milk protein"
```

Variables are great for storing single bits of data so that we can _look up_ the
data later. Key value pairs are similar. The key is the reference point, set
equal to a value. Using a hash key, we can _look up_ the associated value
later.

Using a hash, we could represent the same values from above like so:

```ruby
{
  "apple" => "a delicious fruit",
  "garlic" => "an herb used for flavoring in many cuisines",
  "cheese" => "a dairy product derived from the coagulation of milk protein"
}
```

The above hash has three key/value pairs. The first key of this hash is
`"apple"`. `"apple"` is set to a value, `"a delicious fruit"`. This relationship
is indicated by using the `=>` symbol (sometimes lovingly referred to as a
"hash-rocket").

Although we can store the same values in a set of variables, by including them
together in a hash, we are _associating_ them through the structure of our code.

Hash keys can be any type of data but most of the time we use [strings][]
(as seen in the above example) or [symbols][]:

```ruby
{:name => "John Henry", :occupation => "Steel-driving man"}
```

Hash values can also be any type of data, including arrays and even other
hashes!

```ruby
{:item => "banana", :price => 0.89, :quantity => 6, :description => "a delicious fruit"}
```

## Create a Hash

The easiest way to create a hash is to write it out as we've seen in the
examples so far.

```ruby
new_hash = {
  :created => Time.now,
  :message => "Hello world!"
}
#=> {:created=>2019-04-10 14:05:33 -0400, :message=>"Hello world!"}
```

This is what is referred to as the _implicit_ form. When assigning a variable
Ruby will interpret the curly braces on the left hand side as a hash.

Once created, we can access this hash with our `new_hash` variable:

```ruby
new_hash
#=> {:created=>2019-04-10 13:42:27 -0400, :message=>"Hello world!"}
```

Alternatively, we can use `Hash.new` to create a new hash:

```ruby
second_new_hash = Hash.new
#=> {}
```

This is the same as writing:

```ruby
second_new_hash = {}
#=> {}
```

## Conclusion

We're just getting started with hashes, but hopefully you can already see why
they might be useful. With hashes, we can use hash keys as a way of
_naming_ individual pieces of data. Including multiple key/value pairs allows us
to _associate_ different bits of data, bundling them all up into one object.

Now that we can create hashes and store data as key/value pairs, in the next
lesson, we'll look at how we can access that data. Given a dictionary and a
particular word, we can look up the definition of that word. Similarly, given
a hash and a key in that hash, we can look up the value assigned to that key.

## Resources

- [Intro to Hashes Video][video]
- [Ruby Hash Class][hashes]

[video]: https://www.youtube.com/embed/0JSsFQGYaeA
[hashes]: https://ruby-doc.org/core-2.5.0/Hash.html
[symbols]: https://ruby-doc.org/core-2.5.0/Symbol.html
[strings]: https://ruby-doc.org/core-2.5.0/String.html
[integers]: https://ruby-doc.org/core-2.5.0/Integer.html
[histograms]: https://en.wikipedia.org/wiki/Histogram#Examples
[melville]: https://en.wikipedia.org/wiki/Herman_Melville
