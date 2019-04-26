# Ruby Hashes

## Learning Goals

- Define a Ruby hash
- Define hash keys
- Define hash values
- Create a Hash using its implicit ("Hash-Literal") form
- Create a Hash with `Hash.new`

## Introduction

Up until this point, we've stored our data in a list form using arrays. An
array is like a numbered list. It stores a group of items which are accessible
via their location, or index number, in the list. A `Hash`, in comparison is a
"lookup table" like a dictionary.

Imagine a grocery list: you need to go to the store and buy milk, eggs and
bread. You could store your list like this:

```ruby
groceries = ["milk", "eggs", "bread"]
```

But now let's say we wanted to "look up" the prices of these items. We could
write:

```ruby
prices = [3.00, 2.15, 2.35] # milk, eggs, bread prices
```

But wait, why not write this as:

```ruby
prices = [2.35, 3.00, 2.15]  # bread, milk, eggs prices
```

Well, that's perfectly _legal_ as well to Ruby. But what we want is a way to
associate the word `"milk"` to the price `3.00`. A code comment isn't a strong
enough bond between the `String` (grocery item) and the `Float` (price). When
you need to associate a value with a lookup "_key_", you want a `Hash`.

Hashes allow us to store named, or associated, data. Think of a dictionary or
an address book. This allows us to store more complex collections of
information than the arrays we've seen so far. With a hash, we can associate
item names to prices.

## Define a Ruby Hash

A _hash_ is a collection of data that is separated into pairs of keys and
values. Each key/value pair makes up one unit in the hash. The entire collection
of key/value pairs, which are comma separated, is enclosed in curly braces `{}`:

```ruby
{"key" => "value", "another_key" => "another value"}
```

As with Hashes, you can use white space to make it more friendly for humans to
read:

```ruby
{
  "key" => "value",
  "another_key" => "another value"
}
```

Remember just a moment ago we were asking how to associate a grocery item to a
price? Here's how a `Hash` allows us to do that:

```ruby
prices = {
"bread" => 2.35,
"milk" =>  3.00,
"eggs" =>  2.15
}
```

The relationship between a _key_ (or lookup name) and its associated value is
indicated by using the `=>` symbol (sometimes lovingly referred to as a
"hash-rocket").

## Define Hash Keys

_Keys_ are the things we look up by, in our grocery prices example these are
the `String`s `"bread"`, `"milk"`, and `"eggs"`.

Hash keys can be any type of data but most of the time we use [strings][] (as
seen in the grocery / prices example) or [symbols][]:

```ruby
{:name => "John Henry", :occupation => "Steel-driving man"}
```

Most of the time, Rubyists prefer symbols (there are performance reasons that
we'll cover elsewhere).

## Define Hash Values

Hash values are the bits of data that are returned when we give a `Hash` a
_key_ to use to do a look up. The values in the grocery / prices example are:
`2.35`, `3.00`, and `2.15`.

_Keys_ are the things we look up by, in our grocery example these are the
`String`s `"bread"`, `"milk"`, and `"eggs"`.

Hash values don't need to contain values of all the same type. You can have
`String`s, other scalar data, or even other `Array`s or `Hash`es!

```ruby
{:item => "banana", :price => 0.89, :quantity => 6, :description => "a delicious fruit"}
```

## Create a Hash using its implicit ("Hash-Literal") form

The easiest way to create a `Hash` is to write it out as we've seen in the
examples so far.

```ruby
new_hash = {
  :created => Time.now,
  :message => "Hello world!"
}
#=> {:created=>2019-04-10 14:05:33 -0400, :message=>"Hello world!"}
```

This is what is referred to as the _implicit_ or "`Hash` literal" form. When
assigning a variable, Ruby will interpret the curly braces on the left hand
side as a Hash.

Once created, we can access this hash with our `new_hash` variable:

```ruby
new_hash
#=> {:created=>2019-04-10 13:42:27 -0400, :message=>"Hello world!"}
```

## Create a Hash with `Hash.new`

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
they might be useful. With hashes, we can use hash keys as a way of _naming_
individual pieces of data. Including multiple key/value pairs allows us to
_associate_ different bits of data, bundling them all up into one object.

Now that we can create hashes and store data as key/value pairs, in the next
lesson, we'll look at how we can access, update, and even delete those "pairs."

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
