section 1:-

Problem - 1:

When we run the program, the output is:
Console.Log (Counter ()) => Output is 1
Console.Log (Counter ()) => Output 2 is
Console.Log (Counterb ()) => Output is 1

Both counters, counters and counters are independent of each other. Due to the closure, each counter maintains that it is our count variable that is called the function every time, thus makes them independent.



Problem - 2:

Code is output:

Hello, undefined! => Printed after 0 seconds
Hello, undefined! => Printed after 1 second
Hello, undefined! => Printed after 2 seconds

To work as expected, we can use "late" instead of "VAR", because "late" has the scope of blocks. SND for each recurrence, I have been awarded and the value is printed correctly.



Section - 2: -

Part - 1:

In JS, using the hoisting, variable announcements are taken to the top of the program. 
The scope of the mystery is the function, and since the value is not yet integrated and the variables declared using the "VAR" are hoisted to the top, and it returns unhappy.

When we use "late" or "cast" instead of "var" in the program, the variable is still hoisted on top, but it cannot be used without declaration. It is called as a temporal dead zone, which throws an error when accessed a variable before the announcement.



part 2:

1) In JS, "it" refers to the object that is calling the function. Since, the function inside the settimeout is not an object, it returns to be undefined.

2) The variable resolves the problem "it" in itself, as it never changes, and the user refers to the object.

3) In arrow functions, the value of "this" is inherited from the place they define. So here, in gumdelayed (), this.name user refers to the object correctly.
    
4) Using arrows
const userDelayed = {
    name: "Revan",
    greetUser: function() {
        setTimeout(() => { 
        console.log(`The highlord of NightCourt is: ${this.name}!`);
        }, 4000);
    }
    };

    userDelayed.greetUser(); 


Part - 3:

1) Yes, counters and counters are independent of each other, and separate count variables. Every time a new count variable is made due to the closure when it is called a sectuase (). 

2) ) 
    function createGreeting(greeting) {
        return function(name) {
            return `${greeting}, ${name}!`;
        };
    }
    const sayHello = createGreeting("Hello");
    console.log(sayHello("World"));

3)  4) 
    function createSecretHolder(secret) {
        return {
            getSecret: function() {
                return secret;
            },
            setSecret: function(newSecret) {
                secret = newSecret;
            }
        };
    }
    const holder = createSecretHolder("mySecret");
    console.log(holder.getSecret()); 
    holder.setSecret("newSecret");
    console.log(holder.getSecret()); 



Part - 4:

1) In JS, the remaining parameter allows you to accept an indefinite number. Argument as an array. Therefore, when you do not know accurately. Of arguments, we can use the rest parameter. If the parameters are less than the arguments, the undefined are returned to the missing people.

2) function function_name(a, b, c, ...rest){
    console.log("Value of a is: ",a);
    console.log("Value of rest is: ",rest);
,
function_name (5, 10, 15);

3)  function sumAll(...any) {
        return any.reduce((sum, n) => sum + n, 0);
    }
    console.log(sumAll(12, 34, 15)); 
    console.log(sumAll()); 
    

4) 
   function processArguments(primaryFunction, ...rest) {
        return primaryFunction(...rest);
    }
    function multiply(a, b) {
        return a * b;
    }
    console.log(processArguments(multiply, 123, 445)); 
