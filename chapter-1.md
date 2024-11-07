# our-great-book

## Introduction to Template Literals.

String manipulation is a very common task in programming, especially when building interactive web applications. If you've ever spent time working with JavaScript, then you've likely had to put some variables into strings.
In older versions of JavaScript, this meant using the `+` operator to join strings together through a process called **string concatenation**. However, with the introduction of **template literals** in the JavaScript ES6(2015) update. We now have a cleaner way to insert variables into strings, called **string interpolation**.

### What are Template Literals?

Template literals allow us to manipulate strings easier. They are enclosed in backticks (`` ` ``) rather than (`'`) or (`"`), and they support string interpolation by using the (`${}`) syntax to place variables, or function calls directly into a string.

Here’s an example of how template literals simplify string interpolation.

```javascript
const name = "John"
const age = 24

// Old method using concatenation
const greeting = "Hello, " + name + "! You are " + age + " years old."

// New method using template literals
const greetingWithTemplateLiteral = `Hello, ${name}! You are ${age} years old.`

console.log(greetingWithTemplateLiteral) // Outputs: Hello, John! You are 24 years old.
```

### Benefits of Using Template Literals
#### 1. **Improved Readability**

When using string concatenation, it was easy to get lost in a bunch of `+` signs, especially when working with longer strings. Template literals avoid this by letting you write strings in a way that is easier to follow.

```javascript
const product = "laptop"
const price = 1400

console.log(`The price of the ${product} is $${price}`)
// Outputs: The price of the laptop is $1400
```

#### 2. **Multi-line Strings**

Before template literals, you had to use escape characters like `\n` to make multi-line strings. Now you can write them inside backticks(`` ` ``).

```javascript
// Old method
const multiLineString1 = "This is the first line" + "\n" + "This is the second line" + "\n" + "This is the third line"

// New method
const multiLineString2 = `This is the first line
This is the second line
This is the third line`

console.log(multiLineString1)
console.log(multiLineString2)
/* Both output:
This is the first line
This is the second line
This is the third line
*/
```

#### 3. **Expression Evaluation**

You can also perform calculations, call functions, or manipulate data inside strings.

```javascript
const a = 1
const b = 10

console.log(`The sum of a and b is ${a + b}`) 
// Outputs: The sum of a and b is 11

const upperCaseName = (name) => name.toUpperCase()
console.log(`Your name in uppercase is ${upperCaseName("John")}`)
// Outputs: Your name in uppercase is JOHN
```

### Common Use Cases in JavaScript

#### 1. **HTML Generation**

Instead of building HTML strings with concatenation, you can put variables directly into the string with interpolation.

```javascript
const name = "John"
const htmlContent = `
  <h1>Hello, ${name}!</h1>
  <p>Welcome to the site.</p>
`
```

#### 2. **Logging Messages**

You can also insert variables directly into log messages without the need for concatenation.

```javascript
const user = "John"
const action = "logged in"

console.log(`User ${user} just ${action}`)
// Outputs: User John just logged in
```

#### 3. **Creating URLs**

Template literals make it easier to construct URLs as well.

```javascript
const userId = 123
const apiUrl = `https://api.example.com/user/${userId}/details`

console.log(apiUrl)
// Outputs: https://api.example.com/user/123/details
```

#### 4. **Conditional Logic**
Another great use case is **Conditional logic**. With template literals you can give strings simple conditions using the ternary operator (`? :`), which is a shorthand for an if-else condition.
Logical operators like `&&` (and) or `||` (or) can also be used to add conditional parts to a string. This removes the need for extra if-else statements or the need for concatenation.

```javascript
const isMember = true
console.log(`User is ${isMember ? 'a member' : 'not a member'}`) 
// Outputs: User is a member
```
You can also add more complex expressions inside template literals.

```javascript
/* In this example, the condition age >= 18 is evaluated
the result is either “an adult” or “a minor” based on the value of age*/
const age = 24

const message = `You are ${age >= 18 ? 'an adult' : 'a minor'}`

console.log(message) 
// Outputs: You are an adult

/*In this, if isLoggedIn is true and username exists
username is displayed or else, it defaults to “Guest” */
const isLoggedIn = true
const username = "John"

const greeting = `Welcome ${isLoggedIn && username ? username : 'Guest'}`

console.log(greeting)
// Outputs: Welcome John
```

### Conclusion

Template literals in JavaScript offer a cleaner, and more efficient way to handle string interpolation. Between building web content, logging messages, or creating more readable code, this method provides the flexibility you need.

Next time your dealing with variables and strings, try using template literals. You'll quickly see why it's my go-to method for working with JavaScript.

#### Resources

1. MDN Web Docs - [Template Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
2. GitHub - [Phase 1 Review Strings Lab](https://github.com/learn-co-curriculum/phase-1-review-strings-lab/blob/master/README.md)
3. W3 Schools - [JavaScript Template Strings](https://www.w3schools.com/js/js_string_templates.asp)