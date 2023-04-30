---
aliases: 
tags: 
- public
- knowledge
- tool
date created: "2022-04-13T12:53:19"
date modified: "2022-04-13T01:19:46"
title: Swift
---

# Swift

![[Pasted image 20220413005336.png]]

## Constants and Variables

- The key word var is used to define a variable. Variables’ values can be changed.
- The key word let is used to define a constant. Constants’ values cannot be changed.

Example:

```swift
var mutable = ["alpha", "bravo", "charlie"]
mutable.append("delta")

let immutable = ["alpha", "bravo", "charlie"]
// immutable.append("delta") Error, because immutable is constant
```

## Optionals

In the following code, city is non-optional and cannot be nil. The variables ‘name’ and ‘job’ are optional. But while ‘job’ can be used in the same way as a non-optional variable, there are some difference in the syntax when working with the question-mark-optional.

```swift
var name: String?
var job: String!
var city: String
```

For example, if `name` is printed out the normal way it would look something like this: `Optional(“value of name”)`

If you want to only print the value out it must be forced. But if this is done while the variable is set to `nil`, it would get an error. Because of this, you must first check if the value is `nil` or not:

```swift
if name != nil {
	println("name is \(name!)")
} else {
	println("name is nil")
}
```

The following example will give `finalName` the value of name if it is not nil an will set the value to `no name` if it is nil. This works with `job` the same way:

```swift
let finalName = (name ?? "no name")
let finalJob = (job ?? "no job")
```

## Reference Types

In Swift there are 2 Reference Types. Those are classes and functions. They don’t get copied but pointed at by their instances.

### Classes and Objects

The following piece of code is a typical class. The attributes can be variables or constants. The constructor is marked with `init`. A class can have multiple constructors, as long as there are different sets of parameter needed. Methods are normal functions and class methods are functions that are marked with `class func`.

```swift

	class Person {
	var firstName: String
	var lastName: String

	init(firstName: String, lastName: String) {
		self.firstName = firstName
		self.lastName = lastName
	}

	func say(phrase: String){
		println("\(firstName) \(lastName) says '\(phrase)'")
	}

	class func say(phrase: String){
		println("...and the people all say '\(phrase)'")
	}
}

let p1 = Person(firstName: "Andrea", lastName: "Schaller")
p1.say("let's write some Swift!")

Person.say("lets get tacos")
```

### Functions

There are different ways to set the parameters in a function in swift. You can make that the caller needs to use the argument name when he calls the function and you can make the internal argument name different from the external argument name.

Function in which the caller does’t need to use the argument names:

```swift
func say(phrase: String, times: Int){
	for i in 0...times {
		say(phrase)
		}
}

say("Hello there!", 10)
```

Function in which the external and the internal names are the same and need to be used for calling:

```swift
func say(#phrase: String, #times: Int){
	for i in 0...times {
		say(phrase)
	}
}

say (phrase: "Hello there!", times: 10)
```

Function in which the external an internal names are different and needed for calling the function:

```swift
func say(phrase str: String, times n: Int){
	for i in 0...n {
		say(str)
	}
}

say(phrase: "Hello there!", times: 10)
```

Function with return value:

```swift
func say(phrase: String, times Int) -> Bool {...
```

### Closures

There are different ways to write and shorten closures.

In full length a closure is written like this:

```swift
names.filter() {(name: String) -> Bool in
	return name.hasPrefix("L")
}
